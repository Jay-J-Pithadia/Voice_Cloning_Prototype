# **Voice Cloning Prototype**

**Voice Cloning Prototype - Approach and Explanation**

The voice cloning prototype aims to clone the voice of a selected speaker from the VCTK Corpus dataset using the "Tortoise TTS" library. Below is the step-by-step explanation of the approach used in the voice cloning prototype:

**1. Data Preparation:**
- The Kaggle API credentials are set up to download the VCTK Corpus dataset from Kaggle.
- The "speaker-info.txt" file is read to obtain information about the speakers, including their IDs, age, gender, accents, and regions.
- A sample of 10 speakers is randomly selected from the dataset for building the voice cloning model.

**2. Text and Audio Selection:**
- The prototype selects a specific speaker (in this case, speaker with ID 'p248') to clone her voice.
- A random sample of audio files is displayed for the selected speaker to get an idea of the original voice.

**3. Data Preprocessing:**
- The audio files of the selected speaker are converted to a common sample rate (22050 Hz) for compatibility with the Tortoise TTS library.

**4. Define Text and Preset Option:**
- A sample text is defined, which will be synthesized to generate the cloned voice.
- A preset option is selected to determine the quality of the generated speech. Available options are "ultra_fast," "fast," "standard," and "high_quality." The "standard" preset is chosen for good quality speech synthesis.

**5. Generating Cloned Voice:**
- The voice samples and conditioning latents of the selected speaker are loaded.
- The text is passed to the TTS (Text-to-Speech) model along with the voice samples and conditioning latents to generate the cloned voice.
- The generated speech is saved as a WAV file.

**6. Evaluating the Cloned Voice:**
- The generated speech (cloned voice) is evaluated using the PESQ (Perceptual Evaluation of Speech Quality) metric to measure the similarity between the original and cloned voices.
- PESQ is calculated using the `pesq` library, which requires both the original and cloned audio files.
- The PESQ score is printed as the evaluation result, indicating the similarity between the original and cloned voices. A higher PESQ score indicates better similarity.

**Summary:**
The voice cloning prototype uses the Tortoise TTS library to clone the voice of a selected speaker from the VCTK Corpus dataset. After selecting a speaker, the prototype preprocesses the audio data, defines the text to be synthesized, and generates the cloned voice using the TTS model. Finally, the similarity between the original and cloned voices is evaluated using the PESQ metric. The prototype demonstrates the process of voice cloning and offers a foundation for building more sophisticated voice cloning systems.
