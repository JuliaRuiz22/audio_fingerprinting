## Audio Fingerprinting

## Overview:

This project is an integral part of the Advanced Algorithms and Data Structures course. The aim is to understand the concept of audio fingerprinting as well as the algorithms and code behind it.

## Introduction to Audio Fingerprinting

Every audio is made of a combination of characteristics such as its tone, amplitude or wavelength that makes it identifiable and unique. By recognizing this unique combination of attributes, entire audio recordings can be identified from just a short sample. Audio fingerprinting has various applications such as, pattern matching, multimedia (music) information retrieval, and cryptography.

## Scientific explanation of how it works:

When an audio clip (short audio less than 30 seconds) is inputted, it undergoes a process where it's transformed from its raw waveform representation into a condensed digital signature, wich is also called a fingerprint. In order to undergo this transformation we use spectral analysis and feature extraction.
  - **Spectral Analysis**: breaks down the audio signal into its frequencies, revealing information about the tone and pitch of the sound.
   - **Feature extraction**: identifies key characteristics such as amplitude variations, temporal patterns, and frequency distributions within the signal.
These extracted features are then used to create a compact representation of the audio, which can be efficiently stored and compared with other fingerprints in a database. By matching these fingerprints, the system can quickly identify and retrieve similar or identical audio recordings, enabling applications such as music identification, content recognition, and event detection.

## Applications

Audio fingerprinting has several practical applications:

- **Pattern Matching**: Allows matching of an audio snippet with its corresponding full-length recording.
- **Multimedia (Music) Information Retrieval**: Aids in the categorization and organization of audio content in digital libraries.
- **Cryptography**: Utilizes hashing to securely store audio fingerprints for authentication and verification purposes.

## Real-life Examples

One of the most well-known applications of audio fingerprinting is Shazam. Shazam creates a fingerprint of audio snippets and compares them with the entries of a database contained stored fingerprints from various songs. This process enables users to quickly identify songs they are listening to. More information about Shazam [here](https://www.youtube.com/watch?v=h8fYOd3Dzac). 

## Other examples not related to music:

- **Security**:  audio fingerprinting can be used to detect specific events like breaking glass, gunshots, or alarms. By matching these audio fingerprints with those stored in a database, security personnel can quickly respond to potential threats or incidents captured by surveillance cameras in shopping centers, streets, or buildings.
- **Transportation**: in traffic management systems, audio fingerprinting can be utilized to identify specific sounds associated with traffic congestion, accidents, or emergency vehicle sirens. By analyzing the audio data collected from traffic cameras or sensors, authorities can monitor traffic conditions more effectively and respond promptly to incidents on the road.

## Problems:
  
- **Noise and Variability**: Audio fingerprinting algorithms can be sensitive to background noise, variations in recording quality, and other environmental factors. This can lead to inaccuracies in fingerprint generation and matching.
- **Robustness**: Fingerprinting systems may struggle to accurately identify audio in the presence of distortions, such as compression artifacts or signal processing effects. Ensuring robustness across different audio formats and recording conditions is a significant challenge.
-  **Adversarial Attacks**: Like other machine learning-based systems, audio fingerprinting algorithms may be vulnerable to adversarial attacks. Malicious actors could potentially manipulate audio signals to evade detection or generate false positives.
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
