# Muscle Strain Index Calculation with Exercise Type Factors

---

## **Equation**

\[
\text{Muscle Strain Index} = \left( \frac{\sum_{n=1}^{5} (T_n \times W_n)}{\text{Duration} \times W_{\text{max}}} \right) \times \text{Recovery Factor} \times \text{Fitness Level Adjustment} \times \text{Exercise Type Factor} \times 100
\]

---

## **Variables and Definitions**

- **\( T_n \)**: Time in heart rate Zone \( n \) (minutes)
- **\( W_n \)**: Weight of Zone \( n \)
  - **Zone Weights**:
    - Zone 1 (50–60% HRmax): \( W_1 = 1 \)
    - Zone 2 (60–70% HRmax): \( W_2 = 2 \)
    - Zone 3 (70–80% HRmax): \( W_3 = 3 \)
    - Zone 4 (80–90% HRmax): \( W_4 = 4 \)
    - Zone 5 (90–100% HRmax): \( W_5 = 5 \)
- **\( \text{Duration} \)**: Total exercise time (minutes)
- **\( W_{\text{max}} = 5 \)**: Maximum zone weight
- **\( \text{Recovery Factor} \)**:
  \[
  \text{Recovery Factor} = \text{Cap}\left( \frac{\text{Current HRV}}{\text{Average HRV}},\, 0.8,\, 1.2 \right)
  \]
- **\( \text{Fitness Level Adjustment} \)**:
  \[
  \text{Fitness Level Adjustment} = \text{Cap}\left( \frac{\text{Median VO₂ Max}}{\text{Your VO₂ Max}},\, 0.8,\, 1.2 \right)
  \]
- **\( \text{Exercise Type Factor} \)**:
  - **Low Impact Aerobic**: 0.9
  - **Moderate Impact Cardio**: 1.0
  - **High Impact Cardio**: 1.1
  - **Strength Training**: 1.2
  - **HIIT/Plyometrics**: 1.3
- **\( \times 100 \)**: Scales the index to be out of 100

---

## **Calculation Steps**

1. **Calculate Total Weighted Zone Time**:
   \[
   \text{Total Weighted Zone Time} = \sum_{n=1}^{5} (T_n \times W_n)
   \]

2. **Calculate Maximum Possible Zone Strain**:
   \[
   \text{Maximum Possible Zone Strain} = \text{Duration} \times W_{\text{max}}
   \]

3. **Calculate Normalized Zone Strain**:
   \[
   \text{Normalized Zone Strain} = \frac{\text{Total Weighted Zone Time}}{\text{Maximum Possible Zone Strain}}
   \]

4. **Calculate Recovery Factor**:
   \[
   \text{Recovery Factor} = \text{Cap}\left( \frac{\text{Current HRV}}{\text{Average HRV}},\, 0.8,\, 1.2 \right)
   \]

5. **Calculate Fitness Level Adjustment**:
   \[
   \text{Fitness Level Adjustment} = \text{Cap}\left( \frac{\text{Median VO₂ Max}}{\text{Your VO₂ Max}},\, 0.8,\, 1.2 \right)
   \]

6. **Compute Muscle Strain Index**:
   \[
   \text{Muscle Strain Index} = \text{Normalized Zone Strain} \times \text{Recovery Factor} \times \text{Fitness Level Adjustment} \times \text{Exercise Type Factor} \times 100
   \]

---

## **Example**

### **Given**:

- **Exercise Type**: HIIT/Plyometrics (Factor: **1.3**)
- **Duration**: 45 minutes
- **Time in Zones**:
  - \( T_1 = 5 \) min
  - \( T_2 = 10 \) min
  - \( T_3 = 15 \) min
  - \( T_4 = 10 \) min
  - \( T_5 = 5 \) min
- **Current HRV**: 40 ms
- **Average HRV**: 50 ms
- **Your VO₂ Max**: 48 ml/kg/min
- **Median VO₂ Max**: 45 ml/kg/min

### **Calculations**:

1. **Total Weighted Zone Time**:
   \[
   \text{Total Weighted Zone Time} = (5 \times 1) + (10 \times 2) + (15 \times 3) + (10 \times 4) + (5 \times 5) = 135
   \]

2. **Maximum Possible Zone Strain**:
   \[
   \text{Maximum Possible Zone Strain} = 45 \times 5 = 225
   \]

3. **Normalized Zone Strain**:
   \[
   \text{Normalized Zone Strain} = \frac{135}{225} = 0.6
   \]

4. **Recovery Factor**:
   \[
   \text{Recovery Factor} = \text{Cap}\left( \frac{40}{50},\, 0.8,\, 1.2 \right) = 0.8
   \]

5. **Fitness Level Adjustment**:
   \[
   \text{Fitness Level Adjustment} = \text{Cap}\left( \frac{45}{48},\, 0.8,\, 1.2 \right) = 0.9375
   \]

6. **Muscle Strain Index**:
   \[
   \begin{align*}
   \text{Muscle Strain Index} &= 0.6 \times 0.8 \times 0.9375 \times 1.3 \times 100 \\
   &= 58.5
   \end{align*}
   \]

---

## **Interpretation**

- **Muscle Strain Index**: **58.5 out of 100**
  - Reflects a high level of strain, appropriate for a HIIT workout.
- **Lower Recovery Factor**:
  - Suggests you are less recovered; consider additional rest.
- **Fitness Level Adjustment**:
  - Slight reduction due to higher than median VO₂ max.

---

**Note**: Always ensure that measurements are accurate and factors are chosen appropriately to maintain the reliability of the Muscle Strain Index.

---

Let me know if you have any questions or need further assistance!


