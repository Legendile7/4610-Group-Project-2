# 4610-Group-Project-2

Team Members: 

Evelyn Merchant: @evelynjmerch



## Dataset Description
## Questions and Justification
1. How did the surge in daily new cases correlate with the demand for ICU beds and ventilators across U.S. states between October 2020 and March 2021, and was there a specific 'tipping point' where a jump in new cases shows that an uptake in ventilator use was coming?

Justification:
This examines the critical "lag" between community viral spread and the resulting strain on hospital infrastructure. By identifying a predictive relationship between case counts and ventilator demand, it allows healthcare administrators to forecast resource needs (such as specialized staffing and respiratory equipment) roughly 10–14 days in advance, rather than reacting to a crisis as it happens. It highlights the periods where healthcare systems reached their breaking points, illustrating the human cost of the pandemic when life-saving resources were most scarce.

This is a non-trivial question because it requires a complex join between two distinct data providers—the New York Times and The COVID Tracking Project. In addition, it tracks the surge over time across many different variables.

Tables and Columns:

NYT_US_COVID19 
   DATE: This was used to create the timeline portion.
  STATE: To ensure geographical alignment with the join. Can also filter by state.
  CASES_SINCE_PREV_DAY: to track daily surge in new infections.
CT_US_COVID_TESTS
  PROVINCE_STATE: Used as the join key with the NYT table.
  DATE: Used as the join key to align daily reports.
  INICUCURRENTLY: To track the daily count of patients in intensive care.
  ONVENTILATORCURRENTLY: To measure the peak demand for critical respiratory support.

2. 
## Data Manipulations
## Analysis and Results
1.
<img width="1211" height="386" alt="Screenshot 2026-04-26 at 5 03 02 PM" src="https://github.com/user-attachments/assets/580542bf-331a-491c-8945-b3569930fc70" />

<img width="1193" height="376" alt="Screenshot 2026-04-26 at 5 03 49 PM" src="https://github.com/user-attachments/assets/ef999c4e-c695-4083-ab62-540ccd9e16cf" />

  Our dashboard utilizes a multi-chart approach to distinguish between community transmission 'flow' and hospital resource 'inventory.' This separation is critical for answering our analytical question, as it highlights a significant correlation between new cases and hospital resources and lag that may follow. 
We discovered that while both metrics reached a statistical peak on January 4, 2021 (the tipping point), the data reveals a fundamental difference in their operational behavior. The 'New Cases' peak on Jan 4 was a sharp, isolated event—likely exacerbated by holiday reporting delays—followed by an immediate and rapid decline. Conversely, the demand for Ventilators and ICU beds on that same date represented the culmination of a two-month build-up. On the Ventilator Patients chart, after Jan 4, there is a slight declining slope following the point, illustrating the remaining strain caused by the new cases and shows the lingering effect or lag that it has caused. 
To conclude, this confirms that while the worst day for testing may have been Jan 4, the worst period for hospital resource strain persisted much longer continuing into March, proving that critical care demand is a lagging, more persistent indicator of a healthcare crisis.

## Streamlit App
