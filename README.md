## Problem Statement: 
India witnesses over 4.6 lakh road accidents every year, leading to significant fatalities due to delayed emergency response. Traditional systems rely on human intervention, manual reporting, and are reactive instead of being predictive. Emergency response delays due to lack of real-time accident detection and severity estimation. No integrated platform is present that combines vehicle data, video, audio, and crowd-aid to trigger timely interventions.

## Current Issues:
1. Lack of real-time, automated accident detection mechanisms. 
2. No predictive estimation of accident severity or victim conditions.
3. Delayed ambulance dispatch and poor routing decisions cause avoidable deaths.
4. Absence of unified integrated systems integrating visual, audio, and sensor-based accident evidence. 
5. Need for a scalable, intelligent, city-wide system that reduces response time and improves post-accident outcomes.

## Proposed Solution:
VITALIS is a real-time accident detection and emergency response system based on multi-source inputs: 
1. Visual Detection (YOLOv8): Detect crashes, vehicle rollovers, smoke, fire, and fallen pedestrians from CCTV/ dashcams’ feeds.
2. Audio Analysis (YAMNet): Screeching tires, crashes—detectable even in low-visibility conditions. 
3. ML-Based Severity Prediction: Force of impact, number of victims, presence of flames, victim condition to predict severity.
4. Emergency Dispatch Engine: Auto-routes ambulance using Google Maps API and notifies hospitals based on severity. 
5. Crowd-Aid Module: Sends alerts to nearby verified users for immediate on-ground support before EMS arrives.

## Predictive Output:
1. Accident Detection: Real-time classification of accident vs. non-accident frames on basis of CCTV footage, sound etc.
2. Severity Estimation: Score on 1–10 scale for triage prioritization. 
3. Victim Count Estimation: Human pose detection and blood presence. 
4. Live Emergency Alerts: Exact GPS location and Severity level 
5. Suggested optimal ambulance route: On basis of time to reach/ traffic. 
6. Crowd-Aid Prompt: Instant notification to nearby civilians willing to help (Also for people planning to travel via same route.

## Steps to run:
Follow these steps to run the code on your local system:

1. Clone the repository:
   ```bash
   git clone https://github.com/harshitsaxenaa/VITALIS_PROJECT.git

2. Change directory:
   ```bash
   cd VITALIS_PROJECT

3. Create virtual environment:
   ```bash
   python -m venv venv

4. Activate virtual environment:
   ```bash
   venv\Scripts\activate

5. Install dependencies:
   ```bash
   pip install -r requirements.txt

6. Run scripts:
   ```bash
   python main.py

7. open dashboards:
   ```bash
   streamlit run streamlit_app.py
   streamlit run ambulance_dashboard.py
   streamlit run nearby_help_page.py
   streamlit run 3_Accident_Alert_and_Hospitals.py
