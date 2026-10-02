---
name: residential-interior-estimate
description: Builds a room-by-room estimate and bid summary for residential and light commercial interior work, including bathroom remodels, kitchen updates, whole-house refreshes, drywall, paint, flooring, trim, and tile. Use this skill whenever a contractor asks to price, bid, estimate, or quote an interior job, gives room dimensions and asks what a job will cost, or asks to check an existing interior bid for mistakes or missing items, even if they never say the word "estimate."
---

# Residential Interior Estimate

This skill walks a contractor from room dimensions to a finished bid summary. It is built for small and mid-size remodel work: baths, kitchens, bedrooms, living areas, and whole-house interior refreshes.

The goal is an estimate the contractor can defend line by line. Most small-job losses come from three places: quantities that are too low, items that were never priced, and markup math that does not produce the margin the contractor thinks it does. Every step below is aimed at one of those three.

## Ground rules

- Never invent local prices. Material costs and labor rates change by city and by month. If the contractor has not given a rate, ask for it. If they want to move ahead without it, list the line as "Rate needed" in the output instead of filling in a number.
- Show the math. A contractor needs to see how each quantity was reached so they can correct it.
- State every assumption in plain words in the Assumptions section of the output.
- Use plain, field language. Write for a working contractor, not an accountant.

## Step 1: Gather the job information

Ask for whatever is missing from this list. Ask in one short batch, not one question at a time. If the contractor gave a partial answer, work with what they gave and ask only for the gaps.

1. Job location (city and state). Needed for sales tax and code notes.
2. Room list with length, width, and ceiling height for each room.
3. Number and size of doors and windows in each room. If unknown, use 3 ft x 6 ft 8 in for doors and 3 ft x 5 ft for windows and say so.
4. Scope for each room: demolition, drywall (new or patch), paint (walls, ceiling, trim), flooring type, base and casing trim, tile, fixtures, and anything else.
5. Finish level: builder grade, mid-grade, or high-end.
6. Labor: the contractor's own crew rates, sub quotes, or unit labor prices.
7. Material prices the contractor already has.
8. Overhead percentage and target profit. Ask whether the profit number is a markup on cost or a margin on the selling price.
9. How sales tax applies on their jobs. Rules differ by state and by contract type, so do not assume. If the contractor does not know, state the method used and flag it for them to confirm with their accountant.
10. Year the house was built, if any painting, sanding, or demolition is in scope.

## Step 2: Calculate quantities room by room

Use these formulas. Show each one with the numbers filled in.

| Item | Formula |
|---|---|
| Floor area (SF) | Length x Width |
| Ceiling area (SF) | Same as floor area for flat ceilings |
| Perimeter (LF) | 2 x (Length + Width) |
| Gross wall area (SF) | Perimeter x Ceiling height |
| Net wall area (SF) | Gross wall area minus door and window openings |
| Drywall sheets | Net area to be covered divided by 32 for 4x8 sheets or 48 for 4x12 sheets, then add waste and round up |
| Paint gallons | Area x number of coats, divided by coverage per gallon from the product data, then round up |
| Base trim (LF) | Perimeter minus door widths, then add waste |
| Flooring (SF) | Floor area plus waste |
| Wall tile (SF) | Tiled wall area minus openings, plus waste |

Starting waste factors, which the contractor can change:

| Material | Starting waste |
|---|---|
| Drywall | 10 to 15 percent |
| LVP and laminate | 7 to 10 percent |
| Tile on a straight lay | 10 percent |
| Tile on a diagonal or pattern lay | 15 to 20 percent |
| Trim | 10 percent |
| Carpet | 10 percent, more for seams and pattern match |

Explain to the contractor that these are common starting points, not fixed rules. Room shape, layout, and crew habits change the real number.

## Step 3: Price labor and materials

For each room, build lines with: item, quantity, unit, material unit cost, material total, labor unit cost or hours, labor total, and line total.

Keep material and labor in separate columns. The contractor needs to see each one, and sales tax often applies to only one of them.

## Step 4: Run the missing-items check

Before adding markup, check the estimate against this list. Flag anything in scope that has no line, and ask whether it belongs in the bid or in the exclusions.

- Building permit and inspection fees
- Dumpster or haul-off and disposal fees
- Floor, dust, and furniture protection
- Demolition labor
- Material delivery charges
- Small tools, blades, fasteners, adhesives, caulk, and other consumables
- Supervision and project management time
- Plumbing and electrical sub work for fixture moves or new circuits
- Owner-selected fixtures and finishes (price as an allowance with a stated dollar amount)
- Hidden-condition contingency for rot, mold, or subfloor repair, especially in baths
- Lead-safe work practices if the house was built before 1978 and the work disturbs paint
- Final cleaning
- Punch list and return trip

## Step 5: Add overhead, profit, and tax

Apply them in this order, and show each line:

1. Direct cost subtotal (materials plus labor plus subs plus other direct costs)
2. Overhead
3. Profit
4. Sales tax, applied the way the contractor confirmed in Step 1

Check the markup math every time. A markup on cost and a margin on price are not the same number. For example, a 20 percent markup on $10,000 of cost gives a $12,000 price, which is only a 16.7 percent margin. If the contractor stated a margin target, convert it with this formula and show the result:

Price = Cost divided by (1 minus target margin)

If the stated markup will not deliver the margin the contractor expects, point it out plainly before finishing the bid.

## Step 6: Deliver the output

Use this structure every time:

1. **Bid total**, stated first in one line.
2. **Bid summary table**: direct cost, overhead, profit, sales tax, and total.
3. **Room-by-room breakdown table** with the quantity math.
4. **Assumptions**: every default or assumption used.
5. **Rates needed**: any line priced as "Rate needed."
6. **Missing-items flags** from Step 4.
7. **Exclusions**: items the contractor confirmed are not in the bid, written so they can go straight into a proposal.

## Checking an existing bid

When a contractor shares a bid and asks for a review, do not rebuild it from scratch. Instead:

1. Recheck the quantity math against the dimensions given.
2. Run the Step 4 missing-items check.
3. Check the markup and margin math from Step 5.
4. Report the problems first, largest dollar impact at the top, with the corrected number beside each one.

## Examples

**Example 1**
Input: "Price a 5x8 hall bath gut and rebuild, mid-grade finishes, New Orleans."
Response approach: Ask for ceiling height, tub or shower type, tile height and areas, fixture allowances, crew rates, overhead, profit, and the year the house was built. Then run Steps 2 through 6.

**Example 2**
Input: "Estimate paint and LVP flooring for three bedrooms: 12x12, 11x10, and 10x10, 8 ft ceilings."
Response approach: Calculate wall, ceiling, and floor areas for each room, apply waste, then ask for paint coats, coverage, and labor and material rates before pricing.

**Example 3**
Input: "Check my kitchen bid for missing items before I send it."
Response approach: Follow the "Checking an existing bid" section and report problems by dollar impact.
