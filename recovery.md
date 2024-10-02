# Recovery Score and Estimated Days to Recover Equations

Below are the equations for calculating your **Recovery Score** and estimating the **number of days needed for recovery**, based on key physiological parameters. The temperature parameter has been removed as per your request.

---

## **Recovery Score Equation (Without Temperature)**

### **Variables:**

- **\( RHR \)**: Resting Heart Rate
- **\( HRV \)**: Heart Rate Variability
- **\( RR \)**: Respiratory Rate
- **\( SpO_2 \)**: Blood Oxygen Saturation

### **Baseline (Normal) Values:**

- **\( RHR_{\text{normal}} \)**
- **\( HRV_{\text{normal}} \)**
- **\( RR_{\text{normal}} \)**
- **\( SpO_{2\text{normal}} \)**

### **Weights (\( w_i \)):**

- **\( w_1 = 0.35 \)** (RHR)
- **\( w_2 = 0.35 \)** (HRV)
- **\( w_3 = 0.20 \)** (RR)
- **\( w_4 = 0.10 \)** (SpO₂)

### **Equation:**

\[
\text{Recovery Score} = \left[ \left( \frac{RHR_{\text{normal}} - RHR}{RHR_{\text{normal}}} \times w_1 \right) + \left( \frac{HRV - HRV_{\text{normal}}}{HRV_{\text{normal}}} \times w_2 \right) + \left( \frac{RR_{\text{normal}} - RR}{RR_{\text{normal}}} \times w_3 \right) + \left( \frac{SpO_2 - SpO_{2\text{normal}}}{SpO_{2\text{normal}}} \times w_4 \right) + 1 \right] \times 50
\]

---

### **Explanation:**

- **Deviation Calculations:**
  - Each physiological parameter is compared to your personal baseline to calculate a **deviation**.
  - **Positive Deviation**: Current value indicates better recovery than normal.
  - **Negative Deviation**: Current value indicates worse recovery than normal.

- **Weights (\( w_i \)):**
  - Assign the **relative importance** of each parameter.
  - **Sum to 1** to maintain proper scaling.
  - In this equation:
    - **RHR and HRV** are most significant (**35%** each).
    - **RR** is moderately significant (**20%**).
    - **SpO₂** is less significant (**10%**).

- **Scaling:**
  - **Adding 1** centers the baseline recovery score at 50 when deviations are zero.
  - **Multiplying by 50** scales the score to range between **0 and 100**.

- **Interpretation:**
  - **Recovery Score of 50**: Average recovery.
  - **Score above 50**: Better than average recovery.
  - **Score below 50**: Below average recovery.

---

## **Estimated Days to Recover Equation**

### **Equation:**

\[
\text{Estimated Days to Recover} = 2 \times \left(1 - \frac{\text{Recovery Score}}{100}\right)
\]

### **Explanation:**

- **Parameters:**
  - **\( D_{\text{max}} = 2 \)** days: Maximum recovery time when the recovery score is zero.
  - The recovery score ranges from **0 to 100**.

- **How It Works:**
  - **Recovery Score = 100**:
    - \( \text{Estimated Days} = 2 \times (1 - 1) = 0 \) days (fully recovered).
  - **Recovery Score = 50**:
    - \( \text{Estimated Days} = 2 \times (1 - 0.5) = 1 \) day.
  - **Recovery Score = 0**:
    - \( \text{Estimated Days} = 2 \times (1 - 0) = 2 \) days (maximum recovery time).

- **Interpretation:**
  - **Scores above 50**: Estimated recovery time is **less than 1 day**.
  - **Scores below 50**: Estimated recovery time is **more than 1 day**.

---

## **How It Works**

1. **Calculate Deviations for Each Parameter:**

   - **Resting Heart Rate (RHR):**
     \[
     \text{Deviation}_{\text{RHR}} = \frac{RHR_{\text{normal}} - RHR}{RHR_{\text{normal}}}
     \]
     
   - **Heart Rate Variability (HRV):**
     \[
     \text{Deviation}_{\text{HRV}} = \frac{HRV - HRV_{\text{normal}}}{HRV_{\text{normal}}}
     \]
     
   - **Respiratory Rate (RR):**
     \[
     \text{Deviation}_{\text{RR}} = \frac{RR_{\text{normal}} - RR}{RR_{\text{normal}}}
     \]
     
   - **Blood Oxygen Saturation (SpO₂):**
     \[
     \text{Deviation}_{\text{SpO₂}} = \frac{SpO_2 - SpO_{2\text{normal}}}{SpO_{2\text{normal}}}
     \]

2. **Apply Weights to Each Deviation:**

   - Multiply each deviation by its corresponding weight (\( w_i \)).

3. **Sum the Weighted Deviations and Scale:**

   - **Total Weighted Deviation:**
     \[
     \text{Total Deviation} = \sum_{i=1}^{4} (\text{Deviation}_i \times w_i)
     \]
     
   - **Add 1** to center around the baseline.
   
   - **Multiply by 50** to scale the recovery score between **0 and 100**:
     \[
     \text{Recovery Score} = (\text{Total Deviation} + 1) \times 50
     \]

4. **Estimate Days to Recover:**

   - Plug the recovery score into the equation:
     \[
     \text{Estimated Days to Recover} = 2 \times \left(1 - \frac{\text{Recovery Score}}{100}\right)
     \]

---

## **Example Calculation**

### **Baseline Values:**

- **\( RHR_{\text{normal}} = 60 \) bpm**
- **\( HRV_{\text{normal}} = 50 \) ms**
- **\( RR_{\text{normal}} = 12 \) breaths/min**
- **\( SpO_{2\text{normal}} = 98\% \)**

### **Current Measurements:**

- **\( RHR = 58 \) bpm**
- **\( HRV = 55 \) ms**
- **\( RR = 13 \) breaths/min**
- **\( SpO_2 = 97\% \)**

### **Calculation Steps:**

#### **1. Calculate Deviations:**

- **RHR Deviation:**
  \[
  \frac{60 - 58}{60} = 0.0333
  \]

- **HRV Deviation:**
  \[
  \frac{55 - 50}{50} = 0.10
  \]

- **RR Deviation:**
  \[
  \frac{12 - 13}{12} = -0.0833
  \]

- **SpO₂ Deviation:**
  \[
  \frac{97 - 98}{98} = -0.0102
  \]

#### **2. Apply Weights:**

- **Weighted RHR Deviation:**
  \[
  0.0333 \times 0.35 = 0.01166
  \]

- **Weighted HRV Deviation:**
  \[
  0.10 \times 0.35 = 0.035
  \]

- **Weighted RR Deviation:**
  \[
  -0.0833 \times 0.20 = -0.01666
  \]

- **Weighted SpO₂ Deviation:**
  \[
  -0.0102 \times 0.10 = -0.00102
  \]

#### **3. Sum and Scale:**

- **Total Weighted Deviation:**
  \[
  0.01166 + 0.035 - 0.01666 - 0.00102 = 0.02898
  \]

- **Add 1:**
  \[
  0.02898 + 1 = 1.02898
  \]

- **Calculate Recovery Score:**
  \[
  \text{Recovery Score} = 1.02898 \times 50 = 51.45
  \]

#### **4. Estimate Days to Recover:**

- **Using the Estimated Days to Recover equation:**
  \[
  \text{Estimated Days to Recover} = 2 \times \left(1 - \frac{51.45}{100}\right) = 2 \times (1 - 0.5145) = 2 \times 0.4855 = 0.971 \text{ days}
  \]

---

### **Interpretation:**

- **Recovery Score: 51.45**
  - Slightly above average recovery.
  - Indicates you're recovering well but may still need some rest.

- **Estimated Days to Recover: 0.971 days**
  - Approximately **23 hours and 20 minutes** until full recovery.
  - Suggests you might be ready for moderate activity soon.

---

## **Summary of How It Works**

1. **Collect Data:**
   - Measure your current physiological parameters.
   - Know your baseline (normal) values for each parameter.

2. **Calculate Deviations:**
   - Determine how much each current value deviates from your normal.

3. **Apply Weights:**
   - Assign importance to each parameter through weights.

4. **Compute Recovery Score:**
   - Sum the weighted deviations, add 1, and scale to get a score between 0 and 100.

5. **Estimate Recovery Time:**
   - Use the recovery score to calculate the estimated days to recover.

6. **Interpret Results:**
   - Higher recovery scores mean less recovery time needed.
   - Use this information to plan your activities and rest periods.

---

**Note:** Adjust the **weights (\( w_i \))** based on personal preference or professional advice to reflect which parameters are most indicative of your recovery. The **maximum recovery time (\( D_{\text{max}} \))** in the Estimated Days to Recover equation can also be modified to better fit your individual recovery patterns.

---

Let me know if you have any questions or need further clarification!

