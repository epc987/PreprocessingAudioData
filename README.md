# PreprocessingAudioData

Objectives:

Understand how to preprocess audio data and extract features.
 Train an RNN to classify audio frames as speech or noise.
 Evaluate the RNN model and apply noise suppression.
 Reconstruct denoised audio and evaluate the results.
Data preparation

 Use clean and noisy audio signals:
   - Clean: Speech-only recordings.
   - Noisy: Mix of speech and background noise.
 Preprocessing:
   - Normalize signals.
   - Ensure clean and noisy audio are of equal length.
Feature extraction:
Extract MFCCs (Mel-Frequency Cepstral Coefficients):
   - Compact representation of speech signal.
 MFCC Process:
   1. Framing and windowing the signal.
   2. Converting to frequency domain using FFT.
   3. Applying Mel scale and logarithmic scaling.
   4. Compressing using DCT.
RNN Model Training
 Define an RNN Model:
   - Input: MFCC features.
   - GRU/LSTM layers for sequence modeling.
   - Fully connected layer for binary classification.
 Train the model:
   - Use Binary Crossentropy loss.
   - Monitor training and validation loss
Noise suppression
Predict noise and speech frames:
   - Use the trained RNN model.
   - Generate a binary mask to separate speech from noise.
 Suppress noise:
   - Apply the binary mask to noisy MFCC features.
 Reconstruct audio:
   - Convert denoised MFCCs back to audio using inverse transformation.
Deliverables
Full report containing: 
Visualizations:
  - Clean vs noisy audio signals.
 - MFCC plots for clean and noisy audio.
 Training Results:
   - Loss curves for training and validation.
   - Accuracy of noise detection.
 Reconstructed Audio:
   - Save the denoised audio file.
   - Evaluate the quality of noise suppression.
