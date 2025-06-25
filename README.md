# TeleProNet-Imaginary-Speech-Decoding-via-Prototypical-Network-with-Delta-Band-Modulation
Imagined Speech Decoding Based on Prototype Networks, Multiband Fusion and Delta Band Complementation
Acknowledgments: The data acquisition and data preprocessing at the beginning of this code came from MDS_Kara_One, by Matt-Golightly, thank you very much! It was his code that helped me with this whole project, love you! Thank you!

First: run first step: get the data and labels.py, this step will get the Kara One dataset, and do some primer processing

Second: run Kara One data Processing and epoching.py, this is the most important step for processing the data and get the labels ,
also,this will filtering and do ica for data,and save the processed data as .pkl file,this is the best format to save,(some kind of reservation methods will cause fault)

Third，run network training and test.py， this is the all work I did in this Project,most of the code is written by GPT(hahahaha),
this file contains the labels encoding for model input,hibert transform and FIR filtering, and channel selection ,and network structure, 
and Prototype network construction and training


finally, if you have any question,please concat me  Wechat：CMU_ann (15291835753), email:xduann@163.com 
and my telephone number:+86 15291835753
