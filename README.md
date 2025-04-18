# DISH 
**DISH (Deep Intelligence for Source Handling)** is a hybrid deep learning pipeline designed for source finding and handling of neutral atomic hydrogen (HI) gas in galaxies. The pipeline combines supervised learning and unsupervised learning models to detect and characterize HI emission in data cubes from the Looking At the Distant Universe with the MeerKAT Array (LADUMA) survey.

The name DISH is inspired by the "dishes" (parabolic antenna) found on radio telescopes used in radio astronomy, highlighting the project's connection to radio observations of HI gas.
# Background
Neutral atomic hydrogen (HI) is of particular interest to astronomers due to its role as a fundamental tracer of galactic structure and evolution. The 21-cm emission line from HI allows astronomers to better map the distribution of gas within and around galaxies, offering critical insights into various processes such as star formation, gas accretion, and galaxy interactions throughout cosmic time. 
# Objective
The LADUMA survey is the deepest HI survey to date, aiming to observe HI in galaxies out to redshifts greater than 1. A key challenge arises when observing galaxies at higher redshifts, as HI emission becomes increasingly faint and difficult to detect due to factors such as cosmological redshift, decreased signal-to-noise ratios, and the intrinsic dimming of HI brightness with distance. DISH is designed to address this problem by leveraging deep learning techniques to enhance the detection and classification of HI sources in noisy observational data.
# Methodology
To address the key challenge of detecting HI emission in higher redshift galaxies, DISH utilizes a hybrid deep learning approach consisting of two key components:

1. Supervised Learning: A Convolutional Neural Network (CNN) based model is trained to classify regions in the data cubes as either HI signal or noise. **SoFiA-2**, a source-finding application, is used to generate the ground truth labels for the supervised model. This ensures the labeled dataset accurately reflects regions of HI emission, enabling precise training of the model for source detection.
2. Unsupervised Learning: Anomaly detection techniques, such as autoencoders, are employed to identify deviations in the noise pattern. **SoFiA-2** is also used to identify regions with minimal or no HI emission, which are treated as noise for the unsupervised learning task. The autoencoder is then trained to learn the noise distribution and flag any deviations that may correspond to potential HI sources.

These two learning models complement and enhance each other within the DISH pipeline. While the supervised learning model provides precise detection of HI sources by learning from labeled data, the unsupervised model works in tandem by identifying subtle anomalies or deviations from the expected noise patterns. The outputs of both models are then combined, with the supervised model focusing on high-confidence signal classification and the unsupervised model enhancing the detection of potential HI sources by identifying outliers in noise patterns.

# Current Status
DISH is currently in the research and development phase. The methodology outlined represents the planned approach for source finding and handling of HI emission data. Model implementation, training, and evaluation are in progress.
