> # **Results**

The experiment was performed on the EEG data obtained from 42 subjects of university. For Short Term Stress.
Parallel plot Fig. 4.1, suggests nature of stress and Non stressdata respectively with considered features. 
Through parallel plot, it can be noticed that in the features alpha power, delta power, peak to peak and Hjorth mobility, there’s asignificant difference between Stress and Non stress EEG data. Most of the stress datacan be observed in the higher region for the features Alpha power, peak to peak, Deltapower where in Hjorth mobility, stress data can be distinguished on the lower region.

<img width="800" height="500" alt="Screenshot 2022-11-29 003430" src="https://user-images.githubusercontent.com/40658745/204359942-dc9e0062-4bf6-4def-acbd-86cc77ee322b.png">

For plotting boxplots, a particular feature from each channel of every subject wereconcatenated. Average value of Hjorth mobility, Gamma band power, Alpha bandpower, Alpha asymmetry is greater in Stress subject in comparison with Non stress. Average value for Hjorth complexity and peak to peak is greater in Non stress Subjects


<img width="800" height="350" alt="Screenshot 2022-11-29 003854" src="https://user-images.githubusercontent.com/40658745/204360796-8fd63c64-c7bb-4285-ad66-2478286a7a32.png">

<img width="800" height="350" alt="Screenshot 2022-11-29 003918" src="https://user-images.githubusercontent.com/40658745/204360900-4c0a2adf-cda7-48fb-995a-48e3d0d80a7d.png">

<img width="800" height="350" alt="Screenshot 2022-11-29 003947" src="https://user-images.githubusercontent.com/40658745/204360916-d411d2ab-6579-4c92-9c70-bf964cced563.png">

For classification, 70% of our data set was used for training and the rest 30%for the test
model. Classification when considering all the subjects, the accuracy rate that was foundrespective to individual features, Delta power gave the most accurate result
comparatively. Alpha power, Alpha asymmetry, peak to peak also gave good accuracyAfter delta power.

<img width="600" alt="Screenshot 2022-11-29 004935" src="https://user-images.githubusercontent.com/40658745/204362718-b2394697-9f36-4e5f-b08b-b8ad085582ab.png">


When the best features which includes Delta power, Alpha power, Alpha Asymmetry, Hjorth Mobility, peak to peak and theta power were used, very high classificationaccuracy is obtained. SVM Classifier gave the most accurate results.

<img width="600" alt="image" src="https://user-images.githubusercontent.com/40658745/204362820-11987643-5052-4d2d-9e29-528a0deba5d7.png">
