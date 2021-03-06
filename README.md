# DeepMIMO: A Generic Deep Learning Dataset for Millimeter Wave and Massive MIMO Applications
This is a MATLAB code package of the DeepMIMO dataset generated using [Remcom Wireless InSite](http://www.remcom.com/wireless-insite) software. The [DeepMIMO dataset](http://deepmimo.net/) is a publicly available parameterized dataset published for deep learning applications in mmWave and massive MIMO systems.

This MATLAB code package is related to the following article: 
>Ahmed Alkhateeb, “[DeepMIMO: A Generic Deep Learning Dataset for Millimeter Wave and Massive MIMO Applications](https://arxiv.org/pdf/1902.06435.pdf),” in Proc. of Information Theory and Applications Workshop (ITA), San Diego, CA, Feb. 2019.
# Abstract of the Article
Machine learning tools are finding interesting applications in millimeter wave (mmWave) and massive MIMO systems. This is mainly thanks to their powerful capabilities in learning unknown models and tackling hard optimization problems. To advance the machine learning research in mmWave/massive MIMO, however, there is a need for a common dataset. This dataset can be used to evaluate the developed algorithms, reproduce the results, set *benchmarks*, and compare the different solutions. In this work, we introduce the DeepMIMO dataset, which is a generic dataset for mmWave/massive MIMO channels. The DeepMIMO dataset generation framework has two important features. First, the DeepMIMO channels are constructed based on accurate ray-tracing data obtained from Remcom Wireless InSite. The DeepMIMO channels, therefore, capture the dependence on the environment geometry/materials and transmitter/receiver locations, which is essential for several machine learning applications. Second, the DeepMIMO dataset is generic/parameterized as the researcher can adjust a set of system and channel parameters to tailor the generated DeepMIMO dataset for the target machine learning application. The DeepMIMO dataset can then be completely defined by the (i) the adopted ray-tracing scenario and (ii) the set of parameters, which enables the accurate definition and reproduction of the dataset. In this paper, an example DeepMIMO dataset is described based on an outdoor ray-tracing scenario of 18 base stations and more than one million users. The paper also shows how this dataset can be used in an example deep learning application of mmWave beam prediction.
# Dataset Generation
**To generate the dataset, please follow these steps:** 
1. Download the 'DeepMIMO_Dataset_Generation_v1.1.zip' file and expand/uncompress it.
2. Download the ray-tracing output file for the adopted scenario and expand/uncompress it.
(Note that these ray-tracing scenarios are described in detail on [this website](http://deepmimo.net/ray_tracing.html))
   - For the 'O1_60' scenario, download the file named 'O1_60.zip' using [this link](https://drive.google.com/drive/folders/1enHxTkokm60z2kvo91_MmZ26KNB_7ZIR?usp=sharing).
   - For the 'O1_28' scenario, download the file named 'O1_28.zip' using [this link](https://drive.google.com/drive/folders/1quUFyRN_kkgc7dQG3xwhKZlNcu8aefbe?usp=sharing).
   - For the 'O1_3p5' scenario, download the file named 'O1_3p5.zip' using [this link](https://drive.google.com/drive/folders/1UjBMKTIDXWv1cU8pZXxiMbxp0kqxj_Dl?usp=sharing).
   - For the 'I1_2p5' scenario, download the file named 'I1_2p5.zip' using [this link](https://drive.google.com/drive/folders/11L8-MDipu7AbA0mKAGzOyShn_tdaHLjZ?usp=sharing).
   - For the 'I1_2p4' scenario, download the file named 'I1_2p4.zip' using [this link](https://drive.google.com/drive/folders/1rbIHfK__JUn5e52y5GWI7p-0cL5OSZUO?usp=sharing).
3. Add the expanded folder of the ray-tracing scenario, for example the 'O1' folder, to the path 'DeepMIMO_Dataset_Generation/RayTracing Scenarios/'.
4. Open the file 'DeepMIMO_Dataset_Generation.m' and adjust the DeepMIMO dataset parameters. (Note that these parameters are described in detail in Section III-B of the paper).
5. From the MATLAB command window, call the function `DeepMIMO_dataset=DeepMIMO_Dataset_Generator()`. This function will generate the DeepMIMO dataset given the defined ray-tracing scenario and adopted parameters set.
6. Given the generated DeepMIMO dataset, the channels and users' locations can be accessed as described in Section III-D of the paper.
# License and Referencing
This code package is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/). If you in any way use this code for research that results in publications, please cite both the original article and the Remcom Wireless InSite website:
> - A. Alkhateeb, “[DeepMIMO: A Generic Deep Learning Dataset for Millimeter Wave and Massive MIMO Applications](https://arxiv.org/pdf/1902.06435.pdf),” in Proc. of Information Theory and Applications Workshop (ITA), San Diego, CA, Feb. 2019.
> - Remcom, Wireless insite, “http://www.remcom.com/wireless-insite”
