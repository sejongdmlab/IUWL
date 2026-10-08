# IUWL

This article provides executables of all frameworks and all datasets used in our research of Incremental Uncertain Weighted Pattern Mining.

The executables include all the frameworks, such as IUWL, LIU, ILUNA, L-UWFP+, and U-WFI+ and all the datasets which are used in our experiment: Accidents, Pumsb, Bms-pos, Webview, OnlineRetail, E-Shop, and T10I4DxK.

All executables were compiled to run on 64-bit architectures.

Please refer to the following guide:

1. Note that the name of the executable for each algorithm is as follows:

| Original Name   | IUWL | LIU | ILUNA | L-UWFP+ | U-WFI+ | 
| --------------- | ---- | --- | ----- | ------- | ------ | 
| Executable Name | IUWL | LIU | ILUNA | L-UWFP  | U-WFI  |

2. The parameters of the executables are as follows:

 for IUWL, L-UWFP+, and U-WFI+
```bash
[0]          [1]            [2]                           [3]                         [4]                      [5]              [6]              [7]               [8]
[Executable] [Threshold(%)] [Transaction Data Path(.dat)] [Uncertain Data Path(.txt)] [Weight Data Path(.txt)] [Minimum Weight] [Maximum Weight] [Division Number] [Output File(.txt)]
```

for LIU and ILUNA
```bash
[0]          [1]            [2]                           [3]                         [4]               [5]              
[Executable] [Threshold(%)] [Transaction Data Path(.dat)] [Uncertain Data Path(.txt)] [Division Number] [Output File(.txt)]
```

3. Next, the file name and the parameters of each dataset are as follows:

|  Dataset     | Database Size       | Number of Items | Average Transaction Length |
| ------------ | ------------------- | --------------- | -------------------------- |
| Accidents    | 340,183             | 468             | 33.8                       |
| Pumsb        | 49,046              | 7,116           | 73.6                       |
| Bms-pos      | 515,597             | 1,656           | 6.5                        |
| Webview      | 59,602              | 497             | 2.5                        |
| OnlineRetail | 530,104             | 7,918           | 6.8                        |
| E-Shop       | 165,474             | 24,564          | 13.0                       |
| T10I4DxK     | 200,000 - 1,000,000 | 1,000           | 10                         |

The datasets can be found at https://drive.google.com/file/d/1usDrRhxFZw7aOEkYBzoeTq1nbtgTDTWl/view?usp=sharing.

In the (uncNum-experiment) dataset names, Num represents the mean value of the Gaussian distribution.

The experiment abbreviations are defined as follows:
abl : Ablation study
sen : Sensitivity evaluation
mul : Multivariable evaluation

4. For example
```bash
IUWL.exe 0.009  ..\Data\webview.dat ..\Data\webview(unc).txt ..\Data\webview(wei).txt 0.3 0.6 10 IUWL.txt 
```
will run IUWL on Webview, with the minimum support threshold set to 0.009%, the minimum and maximum weights set to 0.3 and 0.6, respectively, the division number set to 10, and the output file specified as IUWL.txt.
```bash
LIU.exe 14 ..\Data\accidents.dat ..\Data\accidents(unc).txt 10 LIU.txt
```
will run LIU on Accidents, with the minimum support threshold set to 14%, the division number set to 10, and the output file specified as LIU.txt.

5. The output directory "/out" is required for writing result patterns for all algorithms.