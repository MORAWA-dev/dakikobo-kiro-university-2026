# Grounded answer safety design

## Components

`app.py` handles standalone greetings before cache lookup or RAG execution.
`core/retrieval.py` owns the pre-generation evidence filter. The filter uses the
same normalized concept aliases as citation grading and admits weed guidance
only when the chunk text or title contains a weed-related concept.

`core/answer_safety.py` includes retrieval policy code in the safety revision
digest. This makes the existing answer-cache key invalidate earlier grounded
answers after a policy deployment.

## Data flow

1. Normalize and resolve the user query.
2. Route a standalone greeting to a static source-free response.
3. Retrieve and apply the similarity threshold for agricultural questions.
4. Apply topic evidence eligibility before model generation.
5. Generate only when eligible documents remain; otherwise refuse
   deterministically.
6. Grade citations, construct the response, and cache it under the current
   safety revision.

## Correctness properties

- Greeting normalization never creates a citation or advice case.
- Crop overlap alone never satisfies the weed evidence rule.
- Filtering can remove evidence but cannot manufacture or rewrite a chunk.
- Empty eligible evidence never invokes the language model.
