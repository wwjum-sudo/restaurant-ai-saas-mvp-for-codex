# Rules v1

Implement deterministic issue detection before model-based language generation.

## Rule 1: revenue decline
**Condition:** weekly revenue drops >= 10% vs previous week
**Issue:** revenue significantly declined
**Suggested template:** inspect dine-in vs delivery decline and prioritize the weakest side

## Rule 2: average ticket decline
**Condition:** average ticket drops >= 8% vs previous week
**Issue:** average ticket weakening
**Suggested template:** optimize combo structure and high-margin recommendations

## Rule 3: marketing inefficiency
**Condition:** marketing_cost increases while revenue stays flat or declines
**Issue:** low ROI promotion / marketing spend
**Suggested template:** reduce ineffective spend and adjust campaign/store execution first

## Rule 4: high food cost ratio
**Condition:** food_cost / revenue exceeds threshold or rises sharply vs previous week
**Issue:** food cost ratio abnormal
**Suggested template:** check purchase spikes, waste, and high-consumption ingredients

## Rule 5: high labor cost ratio
**Condition:** labor_cost / revenue exceeds threshold
**Issue:** labor pressure too high
**Suggested template:** review staffing schedule against real demand

## Rule 6: underperforming store vs peers
**Condition:** a store significantly underperforms peer stores in the same period
**Issue:** store performance lagging peers
**Suggested template:** compare execution and local action differences with similar stores

## Rule 7: revenue mix imbalance
**Condition:** delivery share is very high and dine-in revenue weakens continuously
**Issue:** unhealthy revenue mix
**Suggested template:** assess dine-in conversion and avoid over-dependence on low-margin channels

## Rule 8: menu structure issue
**Condition:** too many slow items or overly concentrated top sellers
**Issue:** menu structure unhealthy
**Suggested template:** remove low-efficiency items and reinforce stable high-margin items
