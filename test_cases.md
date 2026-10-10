# Test Cases – Home Credit LAP Qualification Voice Agent

## Objective
To verify that the Retell AI voice agent handles customer identification, preliminary eligibility checks, disqualification conditions, and senior loan expert handoff correctly.

## Test Scenarios

| Test ID | Scenario | Expected Result |
|---|---|---|
| TC-01 | Customer passes all seven eligibility checks | Agent provides the preliminary qualification message and senior expert handoff |
| TC-02 | Customer has agricultural property | Agent explains that agricultural property is ineligible and ends the call |
| TC-03 | Customer receives income in cash | Agent explains the eligibility restriction and ends the call |
| TC-04 | Original property documents are unavailable | Agent explains that originals are mandatory and ends the call |
| TC-05 | Customer requests a tenure below 3 years | Agent explains the minimum tenure requirement and ends the call |
| TC-06 | Customer requests a tenure above 15 years | Agent explains the maximum tenure requirement and ends the call |
| TC-07 | Customer requests more than ₹75 lakh | Agent explains the ₹75 lakh cap and asks whether the customer accepts it |
| TC-08 | Customer accepts the ₹75 lakh cap | Agent continues qualification using ₹75 lakh as the qualifying amount |
| TC-09 | Customer declines the ₹75 lakh cap | Agent explains the offer limit and ends the call |
| TC-10 | Customer has an existing loan or requests EMI reduction | Agent routes the customer to the loan-transfer specialist branch |
| TC-11 | Customer provides several eligibility answers together | Agent records all clear answers and asks only for missing information |
| TC-12 | Customer corrects an earlier answer | Agent updates the answer and re-evaluates eligibility |
| TC-13 | Customer is busy | Agent asks for a preferred callback time and ends the call politely |
| TC-14 | Customer gives an unclear answer | Agent asks a clarification question rather than guessing |

## Test Results
The developer reported that the test scenarios were completed successfully in Retell AI. The results should be confirmed against the available call history, transcripts, and recordings before final submission.

## Key Validation Rules
- Eligible property types: Residential, Commercial, and Industrial.
- Sole and Joint ownership are eligible.
- Original property documents are mandatory.
- Maximum loan amount: ₹75 lakh.
- Eligible occupations: Salaried and Self-employed.
- Bank income is eligible; cash income is ineligible.
- No minimum property market value is specified in the assignment rules.
- Eligible tenure: 3–15 years inclusive.
- Senior expert handoff occurs only after all seven eligibility items are answered and valid.
- The agent must not claim final loan approval or invent interest rates.
