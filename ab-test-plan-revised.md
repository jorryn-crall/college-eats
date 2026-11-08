# A/B Test Plan --- College Eats

**Plan version:** Revised treatment\
**Plan date:** November 8, 2026\
**Website:** https://jorryn-crall.github.io/college-eats/\
**Test page:** Cheap Meals page

## 1. Revision history and pre-commitment

The initial Version B treatment changed the page headline. After
reviewing it, the instructor determined that the headline change was too
similar to Version A to represent a sufficiently meaningful experiment.
The revised treatment changes the information displayed in the recipe
cards instead.

The instructor approved the revised treatment and approved reusing the
50 Version A observations already collected. The original 50
observations for the first Version B headline treatment will be retained
as pilot data but **excluded from the final A/B comparison**. A new set
of 50 Version B observations will be collected using the revised
treatment below.

**Commit this revised plan to the GitHub repository before running any
of the new revised Version B trials.** The final report will disclose
that Version A and revised Version B observations were collected in
separate batches on different dates, and that the instructor approved
reuse of the Version A observations.

## 2. Versions and experimental treatment

-   **Version A (control):** The current Cheap Meals page, with
    estimated cost-per-serving amounts displayed for each of the four
    recipes.
-   **Version B (treatment):** The same Cheap Meals page, with the four
    estimated cost-per-serving amounts removed from the recipe cards.

The intended experimental difference is the presence versus absence of
the recipe cost-per-serving displays. Recipe names, ingredients,
directions, serving sizes, preparation times, page structure, and other
page content are intended to remain the same.

Version B will be published separately at `cheap-meals-b.html`. It will
include a `noindex` robots directive and will not be included in the
sitemap. The B page will not be linked from the site's normal
navigation. These are technical search-indexing protections, not part of
the visitor-facing experimental treatment.

## 3. Hypothesis and rationale

**Hypothesis:** AI visitors who see estimated cost-per-serving amounts
(Version A) will be more likely to say they would make at least one
featured recipe within the next week than AI visitors who see the same
recipes without those amounts (Version B).

**Rationale:** College students with limited food budgets may use
per-serving cost information to judge whether a recipe fits their
budget. Showing the estimated cost may therefore make the recipes feel
more practical and actionable. The hypothesis is falsifiable: the
Version A "Yes" rate may be no higher than, or may be lower than, the
Version B "Yes" rate.

## 4. AI visitor procedure and exact prompt

Only AI visitors will be used. No human participants will be recruited.

Each trial will use a fresh conversation with memory disabled. The model
and settings will be kept consistent across trials. The visitor persona,
prompt wording, outcome question, and page-delivery method will remain
the same for both versions. The complete text of the assigned page will
be inserted into the prompt.

-   **Model:** GPT-6
-   **Memory:** Off
-   **Conversation procedure:** One trial per fresh conversation
-   **Page-delivery method:** Full page text pasted into the prompt

**Exact prompt for every trial:**

> You are a college student with a limited food budget who is looking
> for affordable meals to make. Read the webpage below as if you are
> deciding what to cook during the next week. Based only on the
> information on the page, would you choose to make at least one of the
> recipes featured on this page within the next week?\
> Answer with exactly one of these choices: Yes, No, or Maybe. Then
> provide one sentence explaining your answer.\
> Webpage: \[Insert complete page text for assigned version here.\]

Only the complete webpage text will differ between A and B trials.

## 5. Assignment, sample size, and stopping rule

The final comparison will include:

-   **Version A:** 50 previously collected observations, retained with
    the instructor's approval.
-   **Revised Version B:** 50 new observations, collected after this
    revised plan is committed.
-   **Total final analysis sample:** 100 observations.

The original 50 Version B observations from the headline pilot will not
be included in the final analysis.

The new Version B batch will stop when 50 trial responses have been
collected. Do not analyze results or change the procedure before
reaching 50 new Version B observations. Retain all trial outputs,
including responses that do not follow the requested format; document
any exclusion or recoding rather than silently discarding responses.

Because the previously collected Version A observations are being reused
and revised Version B observations will be collected later, the two
final groups are not contemporaneous. The instructor approved reuse of
Version A, but the difference in collection timing will be reported as a
limitation. Do not describe the combined final sample as if a new
randomized A/B assignment sequence was conducted across all 100 trials.

Record the trial number, version, date, model, prompt, and raw response
for each new B trial. Document the assignment and collection procedure
in the data file and appendix.

## 6. Outcome measure and coding

The primary outcome is the AI visitor's answer to the fixed question
asking whether it would make at least one recipe within the next week.

  Response     Outcome code
  ---------- --------------
  Yes                     1
  No                      0
  Maybe                   0

The primary metric is the percentage of trials coded 1 ("Yes") in each
version. Retain the explanatory sentence for qualitative context, but do
not use it to change the primary outcome coding.

## 7. Analysis plan

After all 50 revised Version B trials are complete:

1.  Calculate the number and percentage of "Yes" responses for Version A
    and Version B.
2.  Calculate the difference in "Yes" rates (Version A percentage minus
    Version B percentage).
3.  Compare the two proportions using a two-sided test of proportions at
    a 0.05 significance level. If the observed cell counts make that
    test inappropriate, use Fisher's exact test instead.
4.  Report group counts, percentages, the difference, statistical test,
    p-value, and an appropriate confidence interval where available.
5.  Interpret the result in relation to the hypothesis. A result that
    does not meet the significance threshold will be described as
    inconclusive or not statistically significant, not as proof that the
    versions are equivalent.

The analysis describes responses from AI visitors only. It is not direct
evidence of how real college students would behave.

## 8. Records to preserve

The repository and report appendix will preserve:

-   This revised plan and its Git commit history, showing it was
    committed before the new Version B trials.
-   The addresses or commit references for Version A and Version B.
-   Screenshots of both page versions.
-   The exact prompt and model/settings used.
-   Dates and trial numbers for all observations.
-   Screenshots of the AI conversations and full raw outputs, including
    non-fitting responses.
-   A spreadsheet or CSV with one row per trial, including version,
    trial number, date, raw response, and coded outcome.
-   Analysis calculations and statistical test.
-   A dated log of problems, deviations, or exclusions.

## 9. Interpretation and limitations

This experiment tests whether the presence of estimated cost-per-serving
amounts changes the responses of AI visitors using the specified prompt
and model. It does not establish that real students will make the same
choices. The sample is limited to 50 observations per version, and the
two groups were collected in separate batches on different dates. Model
variability and the artificial nature of the AI visitor persona are
additional limitations. Consider these limitations when interpreting the
results and deciding whether to retain or revise the cost displays.
