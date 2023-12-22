## Causal Inference Notes

### Key Concepts

* **Causation:**
    * **ATE (Average Treatment Effect):** E[Y1 - Y0]
    * **ATT (Average Treatment Effect on the Treated):** E[Y1 - Y0 | T=1]
    * **Counterfactuals:** Hypothetical outcomes an individual would experience under different treatment conditions (Y0 for untreated, Y1 for treated).
* **Association:** E[Y | T=1] - E[Y | T=0]
* **Bias:** Difference between association and the true causal effect (ATT or ATE)

### Randomized Controlled Trials (RCTs)

* Gold standard for causal inference due to random assignment of treatment
* Key properties:
    * (Y_0, Y_1) | T
    * Treatment is the only difference between the groups
    * Knowing the treatment assignment doesn't provide information about the counterfactuals
* Simplest analysis: Difference in means: E[Y | T=1] - E[Y | T=0]

### Observational Data and Challenges

* Challenges:
    * **Confounding:** Variables influence both treatment assignment and outcome
    * **Selection bias:** Factors influence both likelihood of receiving treatment and outcome
    * **Unobserved confounders:** Unmeasured variables that affect both treatment and outcome

### Methods for Causal Inference with Observational Data

* **Regression:** Used to control for confounding variables and estimate the ACE
    * OLS regression can be biased if confounders are omitted
    * Propensity score matching and weighting
    * Instrumental variables (IVs)
* **Matching:** Identifies pairs of treated and untreated units with similar characteristics
    * K-nearest neighbors (KNN) and other matching algorithms
* **Difference-in-differences (DID):** Exploits panel data and compares change in outcome for treated and untreated groups before and after the treatment
    * Assumes parallel trends in the absence of treatment
* **Synthetic control:** Creates a synthetic control group from other units in the data to mimic the treated group before the treatment
* **Regression discontinuity designs (RDDs):** Exploits the discontinuity in the treatment assignment rule at a specific threshold of a running variable
    * Provides local estimates of the causal effect for individuals close to the threshold
* **Machine learning methods:** Various techniques like meta-learners and targeted causal inference models

### Heterogeneous Treatment Effects (CATE)

* CATE aims to estimate the treatment effect for different subpopulations or individuals
* Methods include:
    * Regression models with interaction terms
    * Quantile treatment effects
    * Machine learning models for CATE estimation

### Evaluating Causal Inference Models

* Sensitivity analysis
* Cumulative sensitivity analysis

### Use Cases and Considerations

* Causal inference helps inform decision-making by understanding the true impact of interventions
* Limitations like unobserved confounders and model dependence necessitate careful interpretation and sensitivity analysis
