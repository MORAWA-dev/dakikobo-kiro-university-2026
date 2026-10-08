# Grounded answer safety requirements

## User story

As a farmer, I want DakiKobo to distinguish conversation from agricultural
advice and refuse unsupported field guidance so that I do not act on invented
information.

## Acceptance criteria

1. WHEN a user sends a standalone greeting, THE SYSTEM SHALL return a French
   conversational response without sources or an agricultural advice case.
2. WHEN a weed question retrieves chunks that mention only the crop or a public
   programme, THE SYSTEM SHALL withhold those chunks from model generation.
3. WHEN no eligible chunk remains, THE SYSTEM SHALL return the deterministic
   unavailable-information response with `Faible` confidence and no sources.
4. WHEN a grounding-policy implementation changes, THE SYSTEM SHALL change the
   answer-cache safety revision so answers created under the earlier policy are
   not reused.
5. FOR ANY spelling, capitalization, punctuation, or surrounding whitespace in
   a supported standalone greeting, normalization SHALL preserve the
   conversation route without raising an exception.
6. FOR ANY retrieved institutional chunk that lacks a weed, adventice, or
   désherbage concept, a weed query SHALL NOT pass that chunk to generation.
