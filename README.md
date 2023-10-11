# audio_course
## The Hugging Face Audio Course
https://huggingface.co/learn/audio-course/chapter0/introduction


## [Unit 1](https://huggingface.co/learn/audio-course/chapter1/audio_data)
### Notes:
1. A common sampling rate used in training speech models is 16,000 Hz or 16 kHz.
1. If you plan to use custom audio data to fine-tune a pre-trained model, the sampling rate of your data should match the sampling rate of the data the model was pre-trained on. 
1. Transformer models that solve audio tasks treat examples as sequences and rely on attention mechanisms to learn audio or multimodal representation. Since sequences are different for audio examples at different sampling rates, it will be challenging for models to generalize between sampling rates.
1. A waveform is the representation of sound over time. AKA time domain representation of sound.
1. A way to visualize audio data is to plot the frequency spectrum of an audio signal, also known as the frequency domain representation.
1. The spectrum is computed using the discrete Fourier transform or DFT. It describes the individual frequencies that make up the signal and how strong they are.
1. Power Spectrum measures energy rather than amplitude; this is simply a spectrum with the amplitude values squared.
1. A spectrogram plots the frequency content of an audio signal as it changes over time. It allows you to see time, frequency, and amplitude all on one graph. The algorithm that performs this computation is the STFT or Short Time Fourier Transform.
1. Creating a mel spectrogram is a lossy operation as it involves filtering the signal. Converting a mel spectrogram back into a waveform is more difficult than doing this for a regular spectrogram, as it requires estimating the frequencies that were thrown away. 
1. A mel spectrogram is a popular choice in tasks such as speech recognition, speaker identification, and music genre classification.

### Questions:
1. What are transformers?
1. What is the Nyquist limit?
1. What is the units of Amplitude?
1. How to convert from time domain to frequency domain?
1. What does this line mean: 
"The angle between the real and imaginary components provides the so-called phase spectrum, but this is often discarded in machine learning applications."
1. What is fourier series transformation and laplace series transformation?
1. What is Short Time Fourier Trandform?
1. What is a vocoder?
1. What is example implementation of HiFiGAN?

### Terminology:
1. Waveform
1. Sampling Rate is the process of measuring the value of a continuous signal at fixed time steps. The sampled waveform is discrete, since it contains a finite number of signal values at uniform intervals. The sampling rate (also called sampling frequency) is the number of samples taken in one second and is measured in hertz (Hz). To give you a point of reference, CD-quality audio has a sampling rate of 44,100 Hz, meaning samples are taken 44,100 times per second. For comparison, high-resolution audio has a sampling rate of 192,000 Hz or 192 kHz. A common sampling rate used in training speech models is 16,000 Hz or 16 kHz.
1. Spectrogram


References:
1. [Background in transformers](https://huggingface.co/learn/nlp-course/chapter1/1)
