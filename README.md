# CRM Validation Toolkit
Toolkit to validate credit risk models.

Steps to run
- Ensure Python is installed on your system
- Ensure requirements are on your system (Run `pip install -r requirements.txt`)
- Run Streamlit UI using
    `python -m streamlit run app.py`

Implemented
- CCF
    - [x] CCF assignment process statistics
    - [x] Facilities covered by an EAD approach
    - [x] CCF back-testing
    - [x] EAD back-testing
    - [ ] Discriminatory power
    - [x] Assignment process (portfolio level)
    - [ ] CCF portfolio distribution
    - [x] EAD portfolio distribution

Data requirements
- CCF
    - `estimated_CCF_cohort` : float\
        Estimated CCF value in the beginnning of observation period.
    - `estimated_CCF_fixed_horizon` : float\
        Estimated CCF value 1 year before default.
    - `realised_CCF` : float\
        Realised CCF value at the end of the observation period.
    - `estimated_EAD` : float\
        Estimate of EAD value.
    - `exposure_at_beginning` : float\
        Exposure at the beginning of the observation period.
    - `exposure_at_end` : float\
        Exposure at the end of the observation period.
    - `drawn_amount` : float\
        Drawn amount at default.
    - `default` : 0 | 1\
        Flag to denote if the facility defaulted.
    - `marked` : "outlier" | "process_deficiency" | "ead_covered" | "ccf_covered"\
        This column specifies the facility type, to be able to assign data.
    - `facility_grade` : str | float\
        Facility grade level for each facility.
