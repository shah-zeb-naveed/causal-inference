# Causal Inference

## Graphical Causal Models
- **Causal Bayesian Network**
- **Functional Causal Model**
  - Introduces the concept of noise

## Elicitation vs Causal Discovery
- **Elicitation**: Learning causal diagrams from experts
- **Causal Discovery**: Learning models from data

## Regression vs Causation
- **Regression**:
  - Purely correlational (variables X and Y can be switched)
- **Causation**:
  - Supported by theory
  - The direction of the relationship is crucial

## Randomized Controlled Trials (RCTs)
- Effective for establishing causation
- Sometimes impractical or impossible (e.g., retrospective analysis)

## Packages
- `What If`: Counterfactuals

## Confounding Variables
- Cause both treatment and response
  - **Positive bias**: Intelligence -> Education -> Wage, Intelligence -> Wage
  - **Negative bias**: Crime -> Police -> Violence, Crime -> Violence

## Mediator Variables
- Mediate the effect of treatment on the response (e.g., Education -> White Collar Job -> Wage)
- Conditioning biases depend on the study objective
- Close paths

## Regression Coefficient
- Regress on other variables, then use residuals to calculate coefficients
- Difference when all variables are included together may be negligible

## Interaction Term in Regression
- Effect modification
- Heterogeneous treatment effect
