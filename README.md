# Vanilla-Steel-Data-Analyst-Case-Assessment

Hi Tahir and the Vanilla Steel Team!

I'm excited that you've taken the time to review my GitHub and Data Analyst Assessment Test. Below is an overview of my approach across the three tasks.

---

## Task 1: Data Cleaning & Preparation

1. **Data Cleaning:**  
   - Cleaned the dataset by removing potential hidden spaces, symbols, etc., from column names.

2. **Datetime Standardization:**  
   - Standardized the datetime format for `supplier_data_2` to `%Y-%m-%d %H:%M`.

3. **Material Name Extraction:**  
   - Extracted the material name from `defect_notes` in `supplier_data_2`.

4. **Product Type Cleaning:**  
   - Cleaned up the `product_type` field in `supplier_data_2`.

5. **Material Standard Number Dictionary:**  
   - Leveraged my engineering background and co-authorship in the *International Scientific Journal of Engineering and Material Science* to create a bidirectional dictionary mapping material names to their standard steel numbers.

6. **Common Field Identification:**  
   - Discovered a hidden common key (`breite`) between the two datasets.

7. **Data Merge:**  
   - Merged `supplier_data_1` and `supplier_data_2` on the `breite` field using a LEFT join.  
   - **Rationale:** I prioritized preserving fields like `product_type`, `material_name`, and `material_number` over others such as `werkgute` and `bestellgutetext`.

8. **Length-based Classification:**  
   - Implemented logic to classify records: if `length_mm` is null, the record is a 'Coil_strip'; otherwise, it's a 'Sheet'.

9. **Dataset Enhancements:**  
   - Downloaded the final dataset and made minor additions to `defect_note` and `material_quality_norm`.

10. **Conclusion:**  
    - These steps complete the data cleaning and preparation phase.

---

## Task 2: Reporting

- **Google Looker Studio Report:**  
  [View Report](https://lookerstudio.google.com/u/0/reporting/53a5e9e4-2db6-4a56-a3bb-85e8b1d2ace7/page/p_i86gwnb9pd)  
  *Note: I have already shared access; please let me know if you experience any issues.*

---

## Task 3: Database Integration & BigQuery

1. **Dataset Merge:**  
   - Joined `supplier_data1` and `supplier_data2` into a consolidated dataset called `task3_supplier_data`.

2. **BigQuery Implementation:**  
   - Employed BigQuery as the database platform.  
   - [Access BigQuery Console](https://console.cloud.google.com/bigquery?hl=ru&inv=1&invt=AbrAnw&organizationId=0&project=zeta-tracer-452317-u6&ws=!1m19!1m4!16m3!1m1!1szeta-tracer-452317-u6!3e12!1m6!12m5!1m3!1szeta-tracer-452317-u6!2seurope-west3!3s0aa90d6f-8f30-4911-aad8-6d343a7c32dd!2e1m6!12m5!1m3!1szeta-tracer-452317-u6!2seurope-west3!3s2df8c92f-5de4-4255-a348-e8986eb4ccdf!2e1)

3. **Materialized View:**  
   - Created a materialized view named `recommendations_mv` to ensure data is refreshed automatically when source tables (`buyer_preferences` or `task3_supplier_data`) are updated.

4. **Data Merging Logic:**  
   - Merged datasets on the `Finish` field and applied a filter on `Gross_weight` (i.e., `Gross_weight >= weight`) after thorough analysis to determine the best merging approach.

---

## Final Thoughts

I truly enjoyed working on this test and learning more about Vanilla Steel's operations. I would love the opportunity to learn more about your work and discuss any feedback you might have.

Thank you for considering my application and code :)

Best regards,  
Milana
