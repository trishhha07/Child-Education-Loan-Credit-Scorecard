# Credit Scoring & Loan Decisioning Engine

A regulatory-compliant credit scoring system for a child education loan portfolio, 
built following the industry-standard five-stage scorecard development process used 
by retail banks.

## What this does
Takes raw applicant and bureau data and outputs automated approve/decline decisions 
via a Basel-aligned points-based scorecard calibrated at 600 base points (1:19 odds, 
20 PDO), with an approval cutoff at 580 points.

## Technical approach
- Merged 307K applicant records with 1.7M bureau entries aggregated to customer level
- Applied WoE/IV binning with enforced monotonicity per Basel II/III requirements
- Retained 13 interpretable predictors after IV screening (0.02 to 0.18)
- Built with regulatory compliance in mind: gender excluded per fair lending rules, 
  missing bureau data treated as a risk signal rather than imputed

## Stack
Python · scorecardpy · optbinning · scikit-learn · pandas · NumPy
