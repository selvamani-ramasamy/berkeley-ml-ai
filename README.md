[Link to Notebook - Click Me!](https://github.com/hsoffos/berkeley-ml-ai/blob/main/assignment_5_1_start/prompt.ipynb)


### Will a Customer Accept the Coupon?

**Context**

Imagine driving through town and a coupon is delivered to your cell phone for a restaraunt near where you are driving. Would you accept that coupon and take a short detour to the restaraunt? Would you accept the coupon but use it on a sunbsequent trip? Would you ignore the coupon entirely? What if the coupon was for a bar instead of a restaraunt? What about a coffee house? Would you accept a bar coupon with a minor passenger in the car? What about if it was just you and your partner in the car? Would weather impact the rate of acceptance? What about the time of day?

Obviously, proximity to the business is a factor on whether the coupon is delivered to the driver or not, but what are the factors that determine whether a driver accepts the coupon once it is delivered to them? How would you determine whether a driver is likely to accept a coupon?

**Overview**

The goal of this project is to use what you know about visualizations and probability distributions to distinguish between customers who accepted a driving coupon versus those that did not.

**Data**

This data comes to us from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios including the destination, current time, weather, passenger, etc., and then ask the person whether he will accept the coupon if he is the driver. Answers that the user will drive there ‘right away’ or ‘later before the coupon expires’ are labeled as ‘Y = 1’ and answers ‘no, I do not want the coupon’ are labeled as ‘Y = 0’.  There are five different types of coupons -- less expensive restaurants (under \\$20), coffee houses, carry out & take away, bar, and more expensive restaurants (\\$20 - \\$50). 

**Deliverables**

Your final product should be a brief report that highlights the differences between customers who did and did not accept the coupons.  To explore the data you will utilize your knowledge of plotting, statistical summaries, and visualization using Python. You will publish your findings in a public facing github repository as your first portfolio piece. 

7.  Based on these observations, what do you hypothesize about drivers who accepted the bar coupons?


# Response to #7

## Insights
`Bar` coupons were:
- offered `fourth-most` (second-least) frequently
- offered `most frequently` on warm `(80F)` days
- accepted `most frequently` on warm `(80F)` days
- accepted `less frequently (41.2%)` than the `aggregate (56.9%)`
- accepted by `frequent bar-goers` more frequently `(76.2%)` compared to the rest of the `Bar` coupon population `(37.3%)`
- accepted more frequently by regular bar-goers over 25 years old `(69.0%)` compared to the rest of the `Bar` coupon population `(38.8%)`
- accepted more frequently by regular bar-goers driving without children and who don't work in FF&F occupations `(70.9%)` compared to the rest of the `Bar` coupon population `(33.3%)`
- visiting bars more than once per month seems to be a good indicator of acceptance
      - `Bar Visits Per Month > 1` combined with `Age > 25` or with `Age < 30` has nearly identical acceptance `(69.0% vs 72.0%)`
- the `Cheap Resto > 4 per month and Income < 50k` population is not strongly indicative of acceptance `(45.6% vs 39.6%)`
- the `Cheap Resto > 4 per month and Income < 50k` population accepts coupons slightly more frequently than the overall `Bar` population `(45.6% vs 41.2%)`
## Summary
`What do you hypothesize about drivers who accepted the bar coupons?`

# Independent Investigation - Coupon Choice: Coffee House
## Insights
`Coffee House` coupons were:
- offered `most` frequently
- offered `most frequently` on warm `(80F)` days
- accepted `most frequently` on warm `(80F)` days
- accepted `less frequently (50.3%)` than the `aggregate (56.9%)`
- accepted by `frequent coffeehouse-goers` more frequently `(67.3%)` compared to the rest of the `CoffeeHouse` coupon population `(44.6%)`
- accepted more frequently by regular coffeehouse-goers over 25 years old `(64.0%)` compared to the rest of the `CoffeeHouse` coupon population `(34.9%)`
- the population of regular coffeehouse-goers driving without children and who don't work in FF&F occupations does not appear indicative of acceptance `(66.0% vs 66.7%)`
- visiting coffeehouses more than 3 times per month appears to be a good indicator of acceptance
      - while still useful, visiting coffeehouses 1-3 times per month does not produce as strong a positive indication as the `>3 visits` population
- age appears to be a good indicator of acceptance
      - individuals over age 31 generally accept coffeehouse coupons less frequently
- the `Cheap Resto > 4 per month and Income < 50k` population appears mildly indicative of acceptance `(54.7% vs 44.7%)`
- the `Cheap Resto > 4 per month and Income < 50k` population accepts coupons slightly more frequently than the overall `CoffeeHouse` population `(54.7% vs 50.3%)`
## Summary
`What do you hypothesize about drivers who accepted the coffee house coupons?`

Drivers who vist coffee houses greater than 3 times per month were more likely to accept coupons for coffee houses `(67.3%)`. Drivers visiting coffee houses 1-3 times per month also accepted  more frequently `(64.8%)` than the aggregate CoffeeHouse coupon population. Warm weather (80F) appears to be slightly indicative of accepting a coupon in the aggregate population, and likewise appears to be an indicator for CoffeeHouse coupons specifically. Based on this preliminary analysis, it appears Amazon should focus marketing efforts for CoffeeHouse coupons on those individuals visiting a coffee house once per month or more. Amazon may prefer to prioritize a younger population and warmer weather. Occupation also appears to be a very strong indicator of both whether an individual receives a coupon and whether the individual accepts the coupon.

Drivers who vist bars greater than 3 times per month were much more likely to accept coupons for bars `(76.2%)`. Drivers visiting bars 1-3 times per month also accepted much more frequently `(64.6%)` than the aggregate Bar coupon population. Warm weather (80F) appears to be slightly indicative of accepting a coupon in the aggregate population, but it appears to be a relatively weak indicator for Bar coupons specifically. Cool weather (55F) appears to be over-represented in the Bar coupon population compared to the aggregate population, which is dominated by Warm weather (80F). Based on this preliminary analysis, it appears Amazon should focus marketing efforts for Bar coupons on those individuals visiting a bar once per month or more.


