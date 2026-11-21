# Case study: North Star Map

## The question

A North Star metric is only useful if a team can see what moves it. Most metric trees in PM portfolios are diagrams with made-up numbers. I wanted one built on a real company, with real public numbers, an honest label on everything the company does not disclose, and a working model of how the input metrics drive the North Star. Duolingo is a good case: it publishes daily active users every quarter and has written openly about the growth model behind them.

## Approach

I read Duolingo's last two shareholder letters, its 10-K and its own writing on the growth model. I took the North Star from what the company reports and steers by, then built five branches with three metrics each. For every metric I wrote a definition, the levers that move it, and a guardrail that stops it being gamed. I only show a value when it is reported or can be derived from reported figures. I then rebuilt the published seven-state growth model as a simulator so a reader can see why retention of current users matters most.

## Findings

### 1. Users are growing faster than payers (confirmed, derived from reported figures)

DAUs rose 29% from Q3 2025 to Q3 2026 while paid subscribers rose 14%. Paid subscribers per DAU fell from 22.8% to 20.2%, and bookings per DAU from $5.58 to $4.87 a quarter. Duolingo says this is a deliberate choice in its Q4 2025 letter: it is giving up bookings in 2026 to improve the free experience and grow users.

### 2. More of the monthly base shows up daily (confirmed, derived from reported figures)

DAU/MAU rose from 37.3% to 42.4%. Engagement is deepening, not only reach.

### 3. Current user retention is the biggest lever in a mature habit app (hypothesis, illustrative model)

In my simulator, with my own assumed rates, a 2% improvement in CURR adds about 15% to DAUs after a year, around ten times the next lever. This matches what Duolingo reported from its own model and A/B tests. The rates are mine, not Duolingo's, so the size of the effect is not a finding. The ranking changes when current users are a small share of the base, which the simulator lets you test.

## Decisions

### DAUs as the North Star, with a monetisation counter-metric

I could pick DAUs, paid subscribers or bookings as the North Star. Duolingo itself steers by DAUs and has said so publicly.

**Decision:** Keep DAUs as the North Star and put monetisation beside the tree as a counter-metric branch, with paid subscribers per DAU as the main check.

Full record: [decisions/0001-dau-as-north-star.md](decisions/0001-dau-as-north-star.md)

### Label every value as reported, derived or not disclosed

Most of the useful input metrics (NURR, CURR, lessons per DAU) are not public. Filling them with estimates would look better and be dishonest.

**Decision:** Show 'Not disclosed' with a proposed definition and guardrail. Derived ratios get their own label. Metrics I propose that Duolingo has not named publicly say so in the sources line.

Full record: [decisions/0002-label-every-number.md](decisions/0002-label-every-number.md)

### Rebuild the growth model with illustrative rates

Duolingo published the structure of its model and its result, but not the rates.

**Decision:** Rebuild the seven-state model in the browser with my own assumed rates, put a warning above it, and let the visitor change every rate. The finding text changes when the ranking changes.

Full record: [decisions/0003-illustrative-simulator.md](decisions/0003-illustrative-simulator.md)

## What I learned as a PM

- A metrics tree is most useful where the company is silent. Writing definitions and guardrails for undisclosed metrics was more work than reporting the public ones
- A counter-metric belongs beside the North Star, not under it. Duolingo's 2026 numbers make the case
- Models built on assumed rates are good for explaining mechanisms and bad for sizing effects, so the page says which is which

## Limits

- Most input metrics are not disclosed publicly, so the tree shows definitions rather than values for them
- The simulator's rates are my assumptions
- Public data stops at Q3 2026

## What I would do next

1. Add a second company (for example a marketplace) to show how the tree changes with the business model
2. Add quarterly history for DAUs, MAUs and paid subscribers as small charts
3. Let visitors build their own tree for their own product and export it

## My role

I framed the problem, made the product calls, checked every number and wrote the conclusions. Claude (Anthropic) wrote the code with me. 
