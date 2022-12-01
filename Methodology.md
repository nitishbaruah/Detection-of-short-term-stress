> # Methodology
> ## Data Collection
Our study involves 42 participants (Female: 16, Male: 26, Mean age:21.5 years), the age of the subjects ranges from 18 to 25. The experiment was conducted by performing various tasks such stroop color word test, identification of symmetric images, solving arithmetic questions, And a state of relaxation. 

The individual task was performed for 25 sec and 3 trials for each task were carried. Continuous EEG data has been recorded throughout the experiment.
Initially, subjects were asked to relax for 25 sec and relaxing music was played to lighten the subject. In the next phase, instructions were given for the Stroop color-word. Later, the subjects were asked to respond to the stroop colour test. Subjects, then asked to relax for 5 sec and instructions for the next task is given for next 10 sec. In the next phase, different images were shown to the subjects and asked to identify symmetric images and asymmetric images by showing gestures of thumbs and thumbs down. After then, The subjects were asked to relax again for another 5 sec and instructions for the next task were displayed for 10 sec. In the last phase of the arithmetic test, where an arithmetic problem is shown on the display and the subjects were asked to respond whether it is correct or not by showing a gesture of thumbs up and thumbs down again. The arithmetic test was also carried out for 25 sec. After the finishing of all the trials, the subjects were asked to rate the experiencing of the stress level for each test on a scale of 1 to 10, where 1 indicates that the stress experienced is the lowest and 10 indicates the highest stress.

<img width="750" height="150" alt="hello" src="https://user-images.githubusercontent.com/40658745/204989130-1247bc0e-2eb4-40bc-a17d-408589f69fbd.png">


The Stroop color-word test is a neuropsychological test. It assesses the ability of cognitive interference, which occurs when processing multiple stimuli [3]. In our present work, there were two conditions 1) Congruent, where the color name presented matches exactly with the color ink that is used 2) non-Congruent, where the color name presented doesn't match with the color of ink. 

<img width="600" alt="hello2" src="https://user-images.githubusercontent.com/40658745/204988894-fd7d1992-35f5-4c1b-877d-f0dd5a9fc41d.png">

Arithmetic test is a response test, which induces stress when the subject goes through solving arithmetic problems and rapid decision making. The subjects are also taught to reply with thumbs up and down movements based on whether the result displayed on the screen is a correct solution for the arithmetic issue or not in the arithmetic task. 

<img width="600" alt="hello3" src="https://user-images.githubusercontent.com/40658745/204988848-ef8b7db7-1053-41ee-a5e4-f07cb601485c.png">

Image symmetry test, Test was designed to induce stress, A few puzzle type shapes are drawn, and filled with color in some cases to check if two images are mirror image of each other or not, that is, symmetric or asymmetric.

<img width="600" alt="hello4" src="https://user-images.githubusercontent.com/40658745/204988811-519b7acf-3378-4ca3-9a49-bd948b354a3c.png">

The stress rating of subjects after eachtrial.

<img width="650" alt="hello5" src="https://user-images.githubusercontent.com/40658745/204989615-5d5d68b8-776a-45a5-867b-554c9e5a5886.png">

<img width="650" alt="h6" src="https://user-images.githubusercontent.com/40658745/204989816-26bf4283-870d-4aca-b544-d4fe3dcfe705.png">

> # Data Preprocessing
In this study, the data were collected by instructing subjects to solve tasks within a specified time to increase the stress levels. The EGG data were recorded using the Emotiv Epoc Flex gel kit at a sampling frequency of 128Hz. The Data were recorded from 32 channels, channels that were considered for EGG recording were Cz, Fz, FP1, F7, F3, FC1, C3, FC5, FT9, T7, CP5, CP1, P3, P7, PO9, O1, Pz, Oz, O2, PO10, P8, P4, CP2, CP6, T8, FT10, FC6, C4, FC2, F4, F8, and, FP2. 
	
  The collected Data containing Artifacts caused by muscle movement and eye movement were removed using a combined model of Savitzky-Golay filter and wavelet thresholding. The SavitzkyGolay filter is created with a frame length of 127 and an order of 5. The SavitzkyGolay smoothing filter is used to generate a reference signal, which is subtracted from the EEG data to remove the average trend in the EEG data. After that, wavelet thresholding is used to eliminate the amplitudes which have higher values than thresholding in different scales. The signal is split into four levels, with the mother wavelet being ‘db2' (Daubechies 2). Thresholding is done using a threshold of 0.8 times the standard deviation of the detailed coefficient at the third level of decomposition. The thresholding process removes any leftover components that were not removed after the average trend was subtracted from the EEG.
  
> # Feature Extraction
 
For short term, a total number of 12 features were selectedandcalculated using MATLAB R2021a. Average power is being calculated for different
frequency bands and with Sampling frequency of 128 Hz for each channel. Thefrequency bands which were taken under consideration, Delta(0-4Hz), Theta(4-8Hz), Alpha(8-16Hz), Beta(16-32Hz) and Gamma(32-64Hz). The alpha Asymmetryiscalculated by log(absolute power of Fp2)-log(absolute power of Fp1)[52]. Sixmorefeatures were taken for classification which are Standard deviation, Peak to peak, Kurtosis, Hjorth parameters (Complexity and Mobility) and Renyi entropy.

> # CLassification
For Classification, the following 4 classifiers have been used:
a) Support vector machine(SVM): The statistical learning theory based onthenotion of structural risk minimization is used by a support vector machine. According to the labels provided, an SVM selects a hyper-plane that dividesthe feature space into control and stress groups. The SVMis a very effectiveclassifier that is utilized in a variety of applications. The usage of SVMdecreases the possibility of data over-fitting while also providing goodgeneralization results.

b) Naive Bayes: The Bayes theorem is used to create a probabilistic classifier
called Naive Bayes. It makes use of statistics' maximum posterior hypothesisand performs well with high-dimensional input data. It's a nonlinear classifier
that performs well in real-world situations. Furthermore, the Naive Bayesclassifier necessitates a small amount of training data in order to estimatestatistical parameters. 

c) K-nearest Neighbor (KNN): KNN is an instance-based learning classifier that
saves training instances in their original state. To forecast the class, a distancefunction is used to determine which member of the training set is closest toa
test example. If the attributes are numeric, determining the distance functionissimple. For distance calculation, most instance-based classifiers use Euclideandistance. The distance between an instance with attribute values a1, a2, ..., an(where n is the number of attributes) and b1, b2, ..., bn is defined as,

<img width="167" alt="dd" src="https://user-images.githubusercontent.com/40658745/205036722-045cbf99-fdf7-4f7e-b629-06e0ffae762a.png">


d) Decision Tree: In the shape of a tree structure, a decision tree constructsclassification or regression models. It incrementally cuts down a dataset intosmaller and smaller sections while also developing an associated decisiontree. A tree with decision nodes and leaf nodes is the end result. There are twoor
more branches in a decision node. A classifier or conclusion is representedbyaleaf node. The root node is the topmost decision node in a tree that correspondsto the best predictor. Both category and numerical data can be handledbydecision trees.
