# Open-Source-Event-Driven-ECG-Dataset

This dataset contains 7-bit Event-Driven ECG data simulated from the Physionet MIT-BIH Arrhythmia Database [1], as described in 
**M. Saeed et al., "Evaluation of Level-Crossing ADCs for Event-Driven ECG Classification," in IEEE Transactions on Biomedical Circuits and Systems, vol. 15, no. 6, pp. 1129-1139, Dec. 2021, doi: 10.1109/TBCAS.2021.3136206.**

Level-Crossing ADC Parameters:

ADC Resolution (M) = 7 bits <br />
Clock Frequency (Fc) = 2385Hz <br />
Counter Clock Resolution (N) = 6 bits <br />

For each of the 48 records in the original MIT-BIH dataset (sampled at 360Hz), there are two event-driven files here, one for each channel in the dataset. Furthermore, each dataset file is a .mat and contains a MATLAB structure called 'edECG' described as follows:

    edECG.signal            is the event-driven ECG signal
    edECG.time              is the time in secs for each sample of the event-driven ECG signal
    edECG.counter           is the counter value at each sample of the event-driven ECG signal
    edECG.lcrate            is the average level-crossing rate in the event-driven ECG signal
    edECG.rec               is the record number
    edECG.Fc                is the clock frequency of the LC-ADC
    edECG.N                 is the counter clock resolution of the LC-ADC
    edECG.M                 is the resolution of the of the LC-ADC
    edECG.q                 is the LSB size
    edECG.polarity          is the polarity signal, see [2].
    edECG.ann, edECG.anntype, edECG.subtype, edECG.channel, edECG.num and edECG.comments contain the annotation data, see [3].
    edECG.RR and edECG.tms  contain the RR interval data, see [4].
    edECG.cr                contains the compression ratio of ED ECG signal
    edECG.prd               contains the Percentage Root-Mean Squared Difference of the ED ECG signal
    edECG.sdr               contains the Signal-to-Distortion Ratio of the ED ECG Signal
    edECG.channel           is the channel number of the original dataset


If you use this dataset, kindly cite the following research article:
"M. Saeed et al., "Evaluation of Level-Crossing ADCs for Event-Driven ECG Classification," in IEEE Transactions on Biomedical Circuits and Systems, vol. 15, no. 6, pp. 1129-1139, Dec. 2021, doi: 10.1109/TBCAS.2021.3136206."


References: 
[1] https://physionet.org/content/mitdb/1.0.0/ <br />
[2] Y. Zhao, Z. Shang and Y. Lian, "A 13.34 μW Event-Driven Patient-Specific ANN Cardiac Arrhythmia Classifier for Wearable ECG Sensors," in IEEE Transactions on Biomedical Circuits and Systems, vol. 14, no. 2, pp. 186-197, April 2020, doi: 10.1109/TBCAS.2019.2954479. <br />
[3] https://archive.physionet.org/physiotools/matlab/wfdb-app-matlab/html/rdann.html <br />
[4] https://archive.physionet.org/physiotools/matlab/wfdb-app-matlab/html/ann2rr.html <br />
