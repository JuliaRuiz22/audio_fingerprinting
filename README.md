## Audio Fingerprinting

## Overview:

This project is an integral part of the Advanced Algorithms and Data Structures course. The aim is to understand the concept of audio fingerprinting as well as the algorithms and code behind it.

## Introduction to Audio Fingerprinting

Every audio is made of a combination of characteristics such as its tone, amplitude or wavelength, that makes it identifiable and unique. By recognizing this unique combination of attributes, entire audio recordings can be identified from just a short sample. Audio fingerprinting has various applications such as, pattern matching, multimedia (music) information retrieval, and cryptography.

<img src="https://github.com/JuliaRuiz22/audio_fingerprinting/assets/152634583/2b9360aa-772b-4a6e-a7f2-5d1b13454e93" width="200" height="200">


## Scientific explanation of how it works:

When an audio clip (short audio less than 30 seconds) is inputted, it undergoes a process where it's transformed from its raw waveform representation into a digital signature/fingerprint. In order for this transformation to ocurr, we use spectral analysis and feature extraction.
  - **Spectral Analysis**: breaks down the audio signal into its frequencies, revealing information about the tone and pitch of the sound. It is similar to the experiment of using a triangular prism to decompose a ray of light into its colour components.
  - 
     ![image](https://github.com/JuliaRuiz22/audio_fingerprinting/assets/152634583/6c0765a3-d4d3-4c48-a557-b1c91c4050fe)
   - **Feature extraction**: identifies key characteristics of our audio sample such as  amplitude and loudness variations, patterns, and frequency distribution (this are called features). We want to focus on the special and representative things that our  audio sample has.
These extracted features are then used to create the fingerprint, which can be efficiently stored and then compared with other fingerprints that are stored in a database (we will see an example of this later in the README - Shazam).

## Applications

Audio fingerprinting has several applications such as:

- **Pattern Matching**: Allows matching of an audio snippet with its corresponding full-length recording.
- **Multimedia (Music) Information Retrieval**: Aids in the categorization and organization of audio content in digital libraries.
- **Cryptography**: Utilizes hashing to securely store audio fingerprints for authentication and verification purposes. If you want to further understand the concept of hashing, click [here](https://www.techtarget.com/searchdatamanagement/definition/hashing)

## Real-life Examples

One of the most well-known and popular applications that uses audio fingerprinting is Shazam. Shazam creates a fingerprint from the audio by analysing its sound wave and then compares it with the entries of a database that has stored fingerprints from millions songs. So, it is a simple comparison process between the fingerprint that has just been created with the ones registered in a dataset, and, when a match is found, it returns the corresponding song and artist. This process enables users to quickly identify songs they are listening to. More information about Shazam [here](https://www.youtube.com/watch?v=h8fYOd3Dzac). 

## Other examples not related to music:

- **Security**:  having the audio fingerprint of a breaking glass, alarms, or gunshots is extremely useful in the security field since by matching these audio fingerprints with those stored in a database, security personnel can quickly respond to potential threats such as robberies.
- **Traffic**: audio fingerprinting can be used to identify specific sounds associated with traffic congestion, accidents, or emergency vehicle sirens. By analyzing the audio data collected from traffic cameras or sensors, authorities can monitor traffic conditions more effectively and respond promptly to incidents on the road.

## Problems:
  
- **Noise and Variability**: Audio fingerprinting algorithms can be sensitive to background noise, variations in recording quality, and other environmental factors. This can lead to inaccuracies in fingerprint generation and matching.
- **Robustness**: Fingerprinting systems may struggle to accurately identify audio when there are some sort of distortions such as compression or signal problems. Ensuring robustness across different audio formats and recording conditions is a significant challenge.
-  **Adversarial Attacks**: audio fingerprinting algorithms may be vulnerable to attacks. Malicious actors could potentially manipulate audio signals to evade detection or generate false positives (FP).
- **Legal and Ethical Considerations**: The use of audio fingerprinting technology raises legal and ethical questions, particularly concerning privacy, intellectual property rights, and surveillance. Adherence to relevant regulations and ethical guidelines is critical to mitigate potential risks and ensure responsible use.

## CODE TEMPLATE:

```
# Import necessary libraries
import numpy as np
import librosa
# Add any other libraries you may need for signal processing and feature extraction

# Define function to extract audio features and create fingerprint
def create_audio_fingerprint(audio_file):
    """
    Function to create an audio fingerprint from an audio file.
    
    Parameters:
    - audio_file: path to the audio file
    
    Returns:
    - fingerprint: a unique identifier for the audio file
    """
    # Step 1: Load audio file
    # Use librosa to load the audio file
    audio_data, sample_rate = librosa.load(audio_file)
    
    # Step 2: Preprocess audio data
    # Perform any preprocessing steps such as normalization, resampling, etc.
    
    # Step 3: Extract audio features
    # Use signal processing techniques to extract relevant features
    # Common features include spectral features, temporal features, etc.
    # You may use functions from librosa or other libraries for feature extraction
    
    # Step 4: Create fingerprint
    # Combine the extracted features into a unique fingerprint
    # This could involve hashing the features or using machine learning techniques
    
    # Step 5: Return fingerprint
    return fingerprint

# Example usage
if __name__ == "__main__":
    # Replace 'audio_file_path' with the path to your audio file
    audio_file_path = "example_audio.wav"
    
    # Call the function to create the audio fingerprint
    fingerprint = create_audio_fingerprint(audio_file_path)
    
    # Print or use the generated fingerprint
    print("Audio fingerprint:", fingerprint)

```

## INSTRUCTIONS:

For those interested in understanding and exploring the algorithms used, the complete version of the code is found in the 'CODE' folder inside this repository. This code is done using Python, therefore it is advised to open it using a Python environment program such as Pycharm. To install Pycharm click on [Download](https://www.jetbrains.com/es-es/pycharm/). 

Then, open it in your device, create a new project and give it a name, for example 'PycharmProject'. 

<img width="200" alt="image" src="https://github.com/emilyedgars/ADS-Project/assets/152634583/3c4dd310-1cc3-4582-8164-c51fb025cb70">

After, download the datasets, and open your documents foulder on your device. You have to move the datasets from Downloads to your new 'PycharmProjects' foulder.

<img width="60" alt="image" src="https://github.com/emilyedgars/ADS-Project/assets/152634583/61110ccb-ffe9-420e-99ad-d3ad9dc27e26">  <img width="277" alt="image" src="https://github.com/emilyedgars/ADS-Project/assets/152634583/328ec29c-e69e-4e72-91be-a9967f2697a3">

Now, when you enter Pycharm, you will see the datasets appear here:
<img width="200" alt="image" src="https://github.com/emilyedgars/ADS-Project/assets/152634583/f32cea42-d201-4d4e-9311-b45311be4127">

Then, copy the code into your new project and run it. The pycharm console will pop up and show if there are any errors, or in case it runs correctly,  show the questions for the user.
<img width="200" alt="image" src="https://github.com/emilyedgars/ADS-Project/assets/152634583/3c776bc9-4120-434d-a352-1440051acecc">

## CONTACT US:

For further information or help please contact:
jruiz.ieu2022@student.ie.edu

This README file will constantly be updated by the developers of the project: Julia, Álvaro, Darío and Mateo.
