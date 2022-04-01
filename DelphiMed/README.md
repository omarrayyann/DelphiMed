# DelphiMed

<img src="https://user-images.githubusercontent.com/77675540/161239871-ec92dc9e-6c51-4d02-badd-fc994becf16c.png" width="300">

This document was created during the **10th Annual NYUAD Hackathon** as a Quantum Computer Solution for Social Good.
The solution is to assign patients to hospitals based on their characteristics. The decision is influenced by many factors, including the distance between the patient's location and each hospital, the number of beds available at that hospital and the severity of the patient's condition.

The values in the list of equipment E can be calculated based on the following levels medical need and severity:
- Primary care hospital:
    - Basic Live support (BLS)
    - Basic Live support (BLS) emergency
- Secondary referral hospital
    - Advanced life support (ALS) level one 
    - Advanced life support (ALS) level one emergency 
    - Advanced life support (ALS) level two
- Tertiary referral hospital
    - Specialty care transport 
    - Paramedic Intercept
The different levels have to be normalized and added to the list of alpha values.

<img src="https://user-images.githubusercontent.com/77675540/161242979-53a4b457-b108-4930-a6d2-c77ff5f077f9.png" width="300">

## Members 
- Farai Mazhandu (Mentor)
- Ken Tanaka (Mentor)
- Cyril Karam
- Saimon Tsegai
- Nadeen Tarek
- Qasem Ahmad
- Omar Rayyan
- Edgar Palomino
- Dhurba Tripathi

## Solution
Under the hood, the program is minimzing the cost function below so that an optimal hosptital can be matched for the patient in an emergency case:
/
<img src="https://user-images.githubusercontent.com/77675540/161243001-dd55ec93-3927-47fa-b168-d37a9851344a.png" width="300">

Using classical computers, it is not feasible to minimize the cost function for a large number of patients given multiple different parameters. Our approach uses quantum annealing algorithm to minimize the cost function to find betas (matching) given the alphas: (calculated from various paramters like distance to hospital, equipment availability score and so on). A typical runflow interface looks like the following: 
<img src="https://user-images.githubusercontent.com/30380639/161259922-ef8f074e-09f1-477c-866e-099e234b590b.PNG" width="400">
/
After the program finishes running, the assignments are shown as below:
/
<img src="https://user-images.githubusercontent.com/30380639/161260095-c353ba02-4a16-4850-b770-a9846d9dfcb9.png" width="600">


