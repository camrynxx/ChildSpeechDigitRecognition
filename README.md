# ChildSpeechDigitRecognition
This repository contains the evaluation code for a low-resource automatic speech recognition (ASR) system that recognises spoken digits from children, as outlined in my skripsie report.
It includes all the functions used to evaluate and compare the accuracy of different methods, namely: different feature extraction types (MFCCs and WavLM), template types (adult, child, and voice-converted adult-to-child), and the tuning and evaluation of prediction methods (minimum cost, k-NN, r-NN, and entropy-based confidence). Lastly, a Monte Carlo subsampling approach has been used to determine how much training data is required to achieve reasonable accuracy. 

This repository also contains all the results shown in the report.

**Note**: The training, validation, and testing data are not included in this repository due to size and privacy constraints.



---

## File Descriptions
Below is an overview of the files included in this repository.

- **PreProcessing.ipynb** – Includes code for preprocessing audio files (i.e., resampling and trimming silence), extracting features, and saving features.
- **FeatureExtractionAndTemplatePerformance.ipynb** – Includes the code that evaluates feature extraction types (WavLM and MFCCs), template performance (child, adult, voice-converted adult), and evaluates different WavLM models and their prediction times.
- **HyperparameterTuning.ipyn**b – Includes the code that outputs the results of the hyperparameter tuning (k-NN, r-NN, and entropy-based confidence), as well as evaluuates the performance of all prediction methods - including the final selected method on English and Afrikaans.
- **MonteCarlo.ipynb** – Includes the code that runs the Monte Carlo subsampling simulation for answering "How much data do we need for the model to work well?"
- **WhisperBaseline.ipynb** – Evaluates Whisper on the English and Afrikaans child testing data.

--- 
## Side Notes
All code has been originally run using Python 3.9.6.
