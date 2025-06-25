# TeleProNet-Imaginary-Speech-Decoding-via-Prototypical-Network-with-Delta-Band-Modulation
Imagined Speech Decoding Based on Prototype Networks, Multiband Fusion and Delta Band Complementation
Acknowledgments: The data acquisition and data preprocessing at the beginning of this code came from MDS_Kara_One, by Matt-Golightly, thank you very much! It was his code that helped me with this whole project, love you! Thank you!

First: download the Kara One dataset in: https://www.cs.toronto.edu/~complingweb/data/karaOne/karaOne.html

get the data and labels.py, this step will get the Kara One dataset, and do some primer processing

Second: run Kara One data Processing and epoching.py, this is the most important step for processing the data and get the labels ,
also,this will filtering and do ica for data,and save the processed data as .pkl file,this is the best format to save,(some kind of reservation methods will cause fault)
by the way, before run this file,you must change the path to your dataset in "PATH_TO_DATA = "D:/Downloads/KARA_ONE_Data/"  ,

Third： run network training and test.py， this is the all work I did in this Project,most of the code is written by GPT(hahahaha),
this file contains the labels encoding for model input,hibert transform and FIR filtering, and channel selection ,and network structure, 
and Prototype network construction and training
and the same, before run this file,you must change the path to your dataset in "PATH_TO_DATA = "D:/Downloads/KARA_ONE_Data/" ,
and change your save path in here: "save_path_to_data = "E:/迅雷下载/xduer-SI-15600-5/",which is in line 1350

Kara One dataset,you can download in here:https://www.cs.toronto.edu/~complingweb/data/karaOne/karaOne.html

Evaluation Protocol: Leave-One-Subject-Out (LOSO)

(This project strictly follows a Leave-One-Subject-Out (LOSO) cross-validation protocol to ensure subject-independent evaluation and eliminate any risk of data leakage. For each evaluation fold:

    One subject is held out as the test set.

    The remaining subjects are used exclusively as the training set.

    No overlap exists between training and testing data in any fold.

    The model is retrained from scratch for each fold to avoid subject-specific bias.

✅ No Data Leakage Guarantee

To prevent any potential data leakage, the data loading and processing pipeline is carefully designed:

    Subject-level Separation:
    In each LOSO fold, the EEG recordings of the test subject are completely excluded from training. They are only used during evaluation.

    Independent Preprocessing:
    EEG filtering (bandpass), envelope extraction, downsampling, and segmentation are performed after the LOSO split. This guarantees that no statistical information from the test subject contaminates the training pipeline.

    Subject Labels for Episode Sampling:
    The episode construction function create_episode_diverse_support_balanced_query() ensures that the support and query samples come from different subjects, further reinforcing subject-level independence during few-shot training.

    Reproducible Protocol:
    All data processing is done dynamically within each training fold. No precomputed shared artifacts (e.g., global PCA, scaling) are reused across folds.)
    
finally, if you have any question,please concat me  Wechat：CMU_ann (15291835753), email:xduann@163.com 

and my telephone number:+86 15291835753，You're more than welcome to come see me and discuss your problems！
