The PART 1 of DATA Preparation :

  1. Acquisition and Conversion of Audio File Format:_____________________________________________

To ensure consistency and compatibility across the dataset, all
collected audio files, regardless of their initial format, are converted to the “.WAV” format.

  2. Extraction of Vocal Features :_______________________________________________________________

extracting meaningful acoustic features from each audio file, 
isolating characteristics that most indicate gender differences in speech. 
 
we focused on Mel-frequency Cepstral Coefficients (MFCCs) and pitch as the primary
features.

        2.1. MFCC Coefficients Extraction :

        resampling the audio to 8 kHz, focusing on frequencies essential for speech analysis.
        then we adjust the length of the audio samples to a uniform 40000 samples.

        Using the librosa.feature.mfcc() function from the librosa library, 
        we compute a set of 10 Mel-frequency Cepstral Coefficients (MFCCs).

        The result of the MFCC extraction is a comprehensive feature vector comprising 400 values 
        for each audio sample. Each value corresponds to a specific MFCC coefficient.

        2.2. Pitch Extraction:

        We employ the probabilistic YIN (pYIN) algorithm from the librosa library to extract pitch,
        specifically targeting the typical frequency range of human speech. 

  3. Structuring and Saving Data in CSV file________________________________________________________

After feature extraction, the data was meticulously organized into a structured format. Each
sample’s feature set, consisting of one pitch and 400 MFCCs, was combined with its corresponding
gender label into a pandas DataFrame.

The data organization and consolidation process was optimized through parallel processing,
using a ProcessPoolExecutor to handle multiple files simultaneously. This improved the efficiency
of the process and scaled effectively with the size of the dataset.

Finally, the consolidated DataFrame was saved in a CSV file, providing a well-organized and
accessible format for further analysis and model training.



