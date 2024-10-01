
# Strain Calculation Overview

This document outlines the process of calculating muscle strain based on body weight, heart rate, calories burned, and exercise duration. Additionally, it incorporates concepts like heart rate variability (HRV), fitness level based on VO2 max, and heart rate zones for a more comprehensive strain calculation.

## Overall Strain Equation

```math
Refined Muscle Strain Index = \left(\frac{\text{Heart Rate}}{\text{MHR}}\right) \times \text{Body Weight} \times \frac{\text{Calories Burned}}{\text{Duration (min)}} \times \text{Recovery Factor} \times \text{Exercise Type Factor} \times \text{Zone Strain Factor} \times \text{Fitness Level Adjustment}
```

### Variables in the Equation:

1. **Heart Rate**: Measured in beats per minute (bpm) during exercise.
   - Maximum Heart Rate (MHR) = 220 - Age

2. **Body Weight**: Weight in kilograms (kg).

3. **Calories Burned**: Total calories burned during the exercise session.

4. **Duration**: Duration of the exercise session in minutes.

5. **Recovery Factor**: Based on HRV (Heart Rate Variability), calculated as:
   ```math
   Recovery Factor = \frac{	ext{Current HRV}}{	ext{6-Month Average HRV}}
   ```
   - HRV data can be found in the Apple Health app.

6. **Exercise Type Factor**: Adjustment for exercise modality.
   - Suggested values: 
     - Strength Training: 1.2
     - Endurance/Running: 0.9

7. **Zone Strain Factor**: Adjustment based on heart rate zones.
   - Zone 1 (50-60% MHR): 0.8
   - Zone 2 (60-70% MHR): 1.0
   - Zone 3 (70-80% MHR): 1.2 (+0.2 increase from Zone 2)
   - Zone 4 (80-90% MHR): 1.4 (+0.2 increase from Zone 3)

   You can calculate a weighted average Zone Strain Factor if multiple zones are involved during the workout.

8. **Fitness Level Adjustment**: Based on VO2 max.
   - Median VO2 max for "Fair" category is calculated by averaging the upper and lower bounds of the VO2 max range for your age group and gender.
   ```math
   Fitness Level Adjustment = \frac{\text{Your VO2 max}}{\text{Median VO2 max for Fair level}}
   ```

   - Example: If your VO2 max is 42 ml/kg/min and the median VO2 max for your age group is 37.75 ml/kg/min, your fitness factor would be:
     ```math
     Fitness Level Adjustment = \frac{42}{37.75} \approx 1.11
     ```

## Additional Concepts Discussed

1. **Heart Rate Zones**:
   - Zone 1: Low intensity, warm-up or recovery.
   - Zone 2: Aerobic endurance, fat-burning zone, low strain.
   - Zone 3: Moderate intensity, more muscular and cardiovascular strain.
   - Zone 4: High intensity, significant muscular and cardiovascular strain.

2. **Recovery Factor**:
   - Your **6-month average HRV** serves as the baseline.
   - The **Current HRV** is used to calculate how well your body is recovered from previous strain.

3. **Fitness Level Based on VO2 Max**:
   - VO2 max data can be obtained from the Apple Watch or other fitness trackers.
   - The **median VO2 max** from a chart provides the baseline for comparing your fitness level.

4. **Zone Strain Factor** Adjustments:
   - A **0.2 increase** is applied respectively for each higher heart rate zone starting from Zone 2.

This approach provides a well-rounded calculation of strain, adjusting for various factors like intensity, fitness level, and recovery status.

## Recovery Calculation

After calculating strain post-workout, you can check your recovery status by calculating the **Recovery Factor** and **Recovery Percentage**. These metrics help you understand how well your body has recovered from previous strain.

### 1. **Recovery Factor**

The **Recovery Factor** is calculated based on your **HRV (Heart Rate Variability)**. It shows how well your body has recovered compared to your long-term average.

```math
Recovery Factor = \frac{Current HRV}{6-Month Average HRV}
```

- A **Recovery Factor > 1** means your current HRV is higher than your baseline, indicating good recovery.
- A **Recovery Factor < 1** suggests that your body hasn't fully recovered.

### 2. **Recovery Percentage**

You can also calculate a **Recovery Percentage** to track your progress:

\`\`\`
Recovery Percentage = \left( 1 - rac{Current Strain Score}{Previous Strain Score} 
ight) 	imes 100
\`\`\`

This will give you a readable percentage, where:
- **Positive Percentage**: You've recovered compared to the previous day.
- **Negative Percentage**: Your current strain is higher, suggesting more recovery is needed.

#### Example:

If your **previous strain score** was **10** and your **current strain score** is **7**:

```math
Recovery Percentage = \left( 1 - \frac{7}{10} \right) \times 100 = 30\%
```


This means you've recovered 30% from the previous day.

### Summary of Recovery Calculations:

- **Recovery Factor** uses HRV to measure recovery status.
- **Recovery Percentage** compares current strain to previous strain, giving you an easy-to-understand percentage.

## Zone Strain Factor: Averaging Zones

If you spend time in multiple heart rate zones during your workout, you can calculate the **Zone Strain Factor** by averaging the strain factors for each zone based on the time spent in them.

### 1. **Simple Average for Equal Time Spent**
If you spend equal time in two or more zones, you can calculate the simple average of the strain factors.

#### Example:
- Zone 2 Strain Factor: **1.0**
- Zone 3 Strain Factor: **1.2**

If equal time is spent in both zones, the average Zone Strain Factor is:
```math
Zone Strain Factor = \frac{1.0 + 1.2}{2} = 1.1
```

### 2. **Weighted Average for Unequal Time Spent**
If the time spent in each zone is not equal, you can calculate a **weighted average** based on the percentage of time spent in each zone.

#### Example:
- 40% of time in **Zone 2** (Strain Factor = 1.0)
- 60% of time in **Zone 3** (Strain Factor = 1.2)

To calculate the weighted average:
```math
Zone Strain Factor = (0.4 	imes 1.0) + (0.6 	imes 1.2) = 1.12
```

### 3. **Calculating Percentage of Time Spent in Each Zone**
To calculate the percentage of time spent in each zone, divide the decimal value of time spent in the zone by the decimal value of the total time spent exercising.

```math
Percentage of Time in Zone = \frac{Time Spent in Zone}{Total Exercise Time}
```

#### Example:
If you spent 12 minutes in Zone 2 during a 30-minute workout:
```math
Percentage of Time in Zone 2 = \frac{12}{30} = 0.4 = 40\%
```

This percentage can then be used to calculate the weighted Zone Strain Factor.