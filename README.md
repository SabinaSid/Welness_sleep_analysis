# Wellness sleep analysis: how stress, occupation, and sleep disorders impact sleep duration and subjective sleep quality. 

## Overview
This project investigate the relationships between stress levels, heart rate, sleep duration, sleep quality, and demographic factors (such as occupation and age). Using exploratory data analysis (EDA), the main goal was to test hypotheses about physiological impact of stress and compensatory sleep duration. 

---
## Hypotheses and key findings

## Hypothesis #1: Physiological impact of stress (confirmed)

Stress directly decreases the sleep quality by making it harder to fall asleep, due to high heart rate and anxiety.

Our analysis supports the first hypothesis about the physiological link between stress and heart rate:
* The higher the stress levels, the higher the heart rate.
* Higher heart rate and stress level associated with lower sleep quality and shorter sleep duration.
* Sleep disorders (insomnia, sleep apnea) don't directly correlate with stress levels. Instead, sleep disorders are clustered around specific occupations
* There is no strong relationship between physical activity levels and stress levels in this dataset.

---

## Hypothesis #2: Compensatory sleep duration vs. sleep quality (inconclusive)

Stress degrades sleep quality (the sleep becomes superficial), while  the sleep quantity may remain unchanged or even increase, because the body tries to compensate for fatigue by staying in bed longer.

Our second hypothesis assumed that individuals under high stress might maintain or even increase their sleep duration to compensate for poor sleep quality:
* The data shows that high stress levels (7–8) generally correspond to both lower sleep quality and reduced sleep duration (dropping to ~6.0–6.5 hours).
* The available metrics only track total sleep duration and do not measure sleep stages (e.g., time spent in light vs. deep sleep) or time spent in bed trying to fall asleep.
* Based on the current dataset, we can't fully confirm if the body attempts to compensate for poor sleep quality by staying in bed longer. The evidence leans toward high stress reducing both sleep quality and quantity at the same time.

---

## Demographic factors (occupation and age)

Initial observations showed unexplained spikes in sleep disorders at specific stress levels:
* Insomnia spikes: levels 4 and 7
* Sleep apnea spikes: levels 3 and 8

Breakdown by profession resolved these anomalies:
* Insomnia: mostly concentrated in teachers (~73% have insomnia out of all teachers in the dataset) and salespersons (~91% have insomnia out of all salespersons in the dataset).
* Sleep apnea: mostly concentrated in nurses (~83% of nurses in the dataset).
* Healthy baselines: doctors and engineers consistently report low rates of sleep disorders across various stress levels.

Age factor:
* Older people are most likely to experience less stress.

We observe the associations between stress levels and professions:
* Stress level 3 (low stress): the most concentrated nurse, who likely has a sleep apnea (that explains the spikes in apnea at level 3), and engineer occupation, who likely doesn't have any sleep disorders.
* Stress level 4 (low stress): the most concentrated accountant and teacher occupation. The teachers more likely have an insomnia, so that's why we observed the spikes in insomnia at stress level 4.
* Stress level 5 (medium stress): the most concentrated occupation is a lawyer, over 40 people.
* Stress level 6 (medium stress): the most concentrated occupation is a doctor, over 30 people.
* Stress level 7 (high stress): the most concentrated occupation is a salesperson, over 30 people. The salespersons are more likely to have an insomnia, so that's why we observed the spikes in insomnia at stress level 7.
* Stress level 8 (high stress): the most concentrated occupations are a doctor (who likely doesn't have any sleep disorders) and a nurse. Here again, the nurses are more likely to have an apnea, so that's why we observed the spikes in apnea at stress level 8. Interestingly, we observe the concentration of nurses at both stress levels 4 and 8.

## Key visualizations

### Stress level by disorder
![Stress level by disorder](../Images/disorder_vs_stress.png)

### Sleep disorders by occupation
![Sleep disorders by occupation](../Images/occupation_vs_disorder.png)

### Stress level by occupation
![Stress level by occupation](../Images/occupation_vs_stress.png)

### Heart rate vs sleep duration & sleep quality
![Heart rate vs sleep duration & sleep quality](../Images/heartrate_vs_sleep_duration&quality.png)


### Stress level vs heart rate & sleep quality
![Stress vs heart rate](../Images/heartrate_vs_stress.png)

### Average sleep quality by duration and stress level
![Quality vs duration and stress level](../Images/quality_by_duration&stress.png)


## Tech stack
* **Language:** Python
* **Data Processing:** Pandas
* **Visualization:** Seaborn, Matplotlib

## Project structure
* `eda_sleep_analysis.ipynb`: main jupyter notebook containing data cleaning, visualizations, and hypothesis testing.
* `Data/`: csv file with sleep health and lifestyle dataset.
* `Images/`: exported plots used in this report.
* `requirements.txt`: python dependencies.

## How to run
1. Clone the repo:
   ```bash
   git clone [https://github.com/SabinaSid/Wellness_sleep_analysis](https://github.com/SabinaSid/Wellness_sleep_analysis)