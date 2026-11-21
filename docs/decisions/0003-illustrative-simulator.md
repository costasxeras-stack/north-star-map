# 0003: Rebuild the growth model with illustrative rates

**Status:** accepted, 0.1.0

## Context

Duolingo published the structure of its model and its result, but not the rates.

## Decision

Rebuild the seven-state model in the browser with my own assumed rates, put a warning above it, and let the visitor change every rate. The finding text changes when the ranking changes.

## Tradeoff

- The size of each effect is not meaningful, only the mechanism
- A one-off 2% improvement measured after a year is simpler than Duolingo's monthly compounding, and avoids rates above 100%
