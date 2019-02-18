# SenseMS
*****Private GitHub only available to C. Light*****

Since this work was part of a private Insight fellowship project, the model structure and training code could not be open-sourced.

Eye-tracking data follows the movement of the eye: <br />
![Eye-tracking](https://media.giphy.com/media/blle4NCmxmMne/giphy.gif)

I downsampled the eyetraces from 480 Hz down to 8 Hz to create new datasets on which to train:
![Model](img/downsampling.gif)

This repository contains results from deep-dive into the classification accuracy of the current model; inference can be run on GPU using the frozen graph.

`logistic_tests.py`, `RF_tests.py`, and `GB_tests.py` take an input WAV file, applies an FFT to produce an 80-band
mel spectrogram, then uses the spectrogram to generate 16 kHz audio with a
frozen WaveRNN model.

`build_datasets.py` take...

`cudnn_gru.ipynb` demonstrates usage of the NN model as well as basic results from simpler ML models. These results also contain work verifying suspicions of data leakage in the pre-existing NN architecture.


## Setup
Create a virtualenv, activate then run
```
pip install -r requirements.txt
```


## Test
- Include instructions for how to run all tests after the software is installed
```
# Example

# Step 1
# Step 2
```


## Run
If you have a GPU, select sample input data and a simple model to replicate the process I used to create downsampled datasets.
```
python run_wavernn.py samples/LJ016-0277.wav
```


## Analysis
- Include some form of EDA (exploratory data analysis)
- And/or include benchmarking of the model and results
```
# Example

# Step 1
# Step 2
```
