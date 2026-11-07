# A/B Test Plan: Cheap Meals Page Headline

**Course:** MKTG:4400 Digital Marketing\
**Project:** Deliverable 3\
**Plan prepared:** November 7, 2026\
**Page:** College Eats --- Cheap Meals

## 1. Page and element being tested

This experiment tests whether changing the main page headline (H1)
affects whether an AI visitor says they would make at least one recipe
from the page within the next week.

Only the H1 headline will change. All other page content, layout,
recipes, prices, images, links, and instructions will remain the same
between versions.

-   **Version A (current):**
    `Cheap College Meals: 4 Affordable Recipes for Students`
-   **Version B (proposed):**
    `Cheap College Meals: Budget-Friendly Recipes You Can Make in College`

**Version A page:**\
https://jorryn-crall.github.io/college-eats/cheap-meals.html

Version B will be a separate test page in the same GitHub repository. It
will differ from Version A only in the H1 headline. Version B will have
a `noindex` directive (or a canonical tag pointing to Version A) and
will be excluded from the sitemap so it does not compete with Version A
in search results.

## 2. Hypothesis and rationale

**Hypothesis:** AI visitors shown Version B will be more likely to
answer "Yes" than AI visitors shown Version A when asked whether they
would make at least one recipe from the page within the next week.

Version B keeps the target phrase "Cheap College Meals" at the beginning
while making the practical benefit to college students more explicit.
This may make the page's relevance and usefulness clearer to its
intended audience.

The hypothesis and primary outcome will not be changed after data
collection begins.

## 3. AI visitors, model, settings, and exact prompt

Each trial will use GPT-6 acting as a college student with a limited
food budget. Every trial will take place in a fresh conversation. Memory
will be off for every trial, and no conversation will be reused.

-   **Model:** GPT-6
-   **Memory setting:** Off
-   **Other settings:** Keep the same settings for every trial. Record
    any available settings that affect model behavior and do not change
    them during the experiment.

The same model, settings, persona, and instructions will be used for all
100 trials. The only difference between trials will be whether the AI
visitor is shown Version A or Version B.

### Exact prompt

Use the following prompt word for word in every trial. Replace only the
bracketed webpage material with the complete page text for the assigned
version. Present both versions in the same format.

> You are a college student with a limited food budget who is looking
> for affordable meals to make. Read the webpage below as if you are
> deciding what to cook during the next week. Based only on the
> information on the page, would you choose to make at least one of the
> recipes featured on this page within the next week?
>
> Answer with exactly one of these choices: **Yes**, **No**, or
> **Maybe**. Then provide one sentence explaining your answer.
>
> **Webpage:**
>
> \[Insert the complete page text for the assigned version here.\]

The complete page text shown in each trial will be retained with the
experiment records so the material presented to the AI visitor can be
verified.

## 4. Assignment procedure and sample size

The experiment will include **100 trials total: 50 assigned to Version A
and 50 assigned to Version B**.

Before running the trials, create 50 A assignments and 50 B assignments
in a spreadsheet. Randomly shuffle the 100 assignments, then save the
randomized order as fixed values so it cannot change. Follow that order
and record the assigned version for every trial.

Each trial will use a fresh conversation with memory off. No
conversation will be reused. Complete all 100 assigned trials; do not
stop early based on interim results.

**Planned stopping point:** Complete all 100 trials, with 50 for each
version, by November 17, 2026. Record the actual dates and batches in
the experiment log.

## 5. Primary outcome and measurement

The one primary outcome is whether the AI visitor says it would make at
least one recipe from the page within the next week.

Code responses as follows:

  AI visitor answer     Outcome
  ------------------- ---------
  Yes                         1
  No                          0
  Maybe                       0

The raw-data spreadsheet will contain one row per trial and record the
trial number, assigned version, answer, numeric outcome, full AI output,
date, and model. Retain every full output, including unexpected or
nonconforming responses. Flag and document unclear responses rather than
silently removing them.

Screenshots of the AI experiment conversations will also be saved for
the appendix, as instructed by the professor. Label each screenshot with
its corresponding trial number.

## 6. Comparison and decision rule

For each version, calculate the number and percentage of Yes responses:

**Yes percentage = number of Yes responses ÷ 50 × 100**

The primary comparison is:

**Difference = Version B Yes percentage − Version A Yes percentage**

A positive difference means Version B received a higher percentage of
Yes responses; a negative difference means Version A received a higher
percentage.

Compare the two groups using a two-sided test of proportions at a 0.05
significance level. Report the Yes count and percentage for each
version, the percentage-point difference, and the p-value. If the
assumptions for the planned test are not met, use an appropriate exact
test and explain that choice.

The hypothesis will be considered supported if Version B has a higher
Yes percentage than Version A and the difference is statistically
significant at the 0.05 level. Report the results honestly regardless of
the outcome.

## 7. Documentation and recordkeeping

The experiment files will include:

-   This plan and its GitHub commit link.
-   Screenshots of Version A and Version B, plus their page addresses or
    repository commits.
-   The exact prompt, model name, memory setting, other settings, and
    dates of each trial batch.
-   The full output from every AI visitor trial.
-   The raw-data spreadsheet or CSV with one row per trial.
-   A screenshot of each AI conversation, labeled by trial number, as
    additionally instructed by the professor.
-   The analysis showing each version's outcome, the difference, and the
    statistical test.
-   An experiment log documenting errors, unexpected responses,
    interruptions, or deviations, with dates.

Do not omit a trial because its response is inconvenient or does not
support the hypothesis. Record any deviation from this plan with its
date and reason.

## 8. Limitations

This experiment measures responses from AI models acting as members of a
target audience. It does not measure actual college students' behavior,
actual recipe preparation, or real-world customer conversion. AI
responses may not predict how real visitors would behave. The sample of
100 AI trials is limited, so a result that is not statistically
significant does not establish that the headlines have exactly the same
effect.

------------------------------------------------------------------------

**Before starting the trials:** Commit this plan first. Then create
Version B as a separate page in the same repository, verify that only
the H1 differs, protect Version B from search indexing and exclude it
from the sitemap, and create and save the randomized 50/50 assignment
order.
