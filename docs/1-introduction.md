---
layout: page
title: 1. Introduction
permalink: /1-introduction/
---


![OSIPI logo](https://osipi.github.io/assets/img/logo.png)

&nbsp;&nbsp;

Following the consensus statement for the recommended implementation of arterial spin labeling (ASL) perfusion MRI for clinical application in the brain <sup>1</sup> by the Perfusion Study Group (SG) of the International Society for Magnetic Resonance in Medicine (ISMRM) and the European Consortium for ASL in Dementia (COST Action BM1103) in 2014 (referred to hereafter as the ‘ASL White Paper’), standardized ASL perfusion imaging sequences have now been implemented by the majority of MRI manufacturers. Recommended acquisition protocols and the increased availability of ASL imaging sequences have encouraged the use of ASL in clinical applications <sup>2</sup>. However, ASL remains a rapidly and widely developing field, both in terms of improving the accuracy and precision of cerebral blood flow (CBF) quantification via advances in pulse sequence and post-processing methods, and providing other output derivatives in addition to CBF (e.g., arterial transit times). These advances have greatly expanded the scope of ASL, but also bring further divergence of the technique, particularly in the terminology used, which can lead to confusion and hamper interoperability. In addition, motivated by the non-invasive nature of ASL, there is an increased number of large cohort studies that adopt ASL perfusion imaging, such as the Alzheimer’s Disease Neuroimaging Initiative (ADNI3; [http://adni.loni.usc.edu/adni-3/](http://adni.loni.usc.edu/adni-3/)) and some branches of the Human Connectome Project <sup>3</sup>, in which data are acquired from multiple sites using different MRI scanners. To maximize the usefulness of these data, guidelines for consistent reporting of image acquisition parameters are essential.

As part of the ISMRM Open Science Initiative for Perfusion Imaging (ISMRM OSIPI, referred to hereafter as “OSIPI”), an initiative and activity of the ISMRM Perfusion SG, the ASL Lexicon Task Force has been working on the development of an ASL Lexicon and Reporting Recommendation for Perfusion Imaging and Analysis. The purpose of the ASL lexicon is to develop standardized nomenclature and terminology for the broad range of ASL imaging techniques and parameters, as well as for the physiological constants required for quantitative analysis. However, this ASL lexicon does not provide recommended standard ASL implementations and optimal parameter values, which is the remit of the other parallel recommendations/guidelines, and the readers are directed to those, such as the ‘ASL White Paper’ for a standard ASL implementation and processing approach, and its recent extensions for up-to-date summaries of more specific ASL techniques and developments (see the following subsection “1.1 Previous efforts on ASL standardization relevant to the development of ASL Lexicon and Reporting Recommendation”). Instead, ASL lexicon aims to provide harmonization across documentation, reports and publications, by standardizing the terminology and parameter definitions, which is beyond the scope of the ‘ASL White Paper’ and the others. In addition, the developed ASL lexicon is intended to form a common, community-endorsed recommendation for reporting of ASL perfusion imaging, providing a list describing which parameters in acquisition protocols should be reported by investigators and how, aiming to improve the interoperability and comparability of reported studies. 

In summary, this article is primarily intended to provide:



* A lexicon for researchers/developers of ASL sequences and analysis tools to conform to the community-based consensus recommendation, to avoid misunderstandings caused by diverse terminologies and inconsistent definitions.
* A reporting guideline for researchers using ASL sequences and analysis tools to find how their ASL studies and results should be documented and reported, which should make their studies more widely understandable and reproducible. 

Within the OSIPI framework, an overarching aim of this article is to enable researchers and developers to use openly available datasets (e.g., data repositories) without ambiguity relating to the acquisition parameters used.


&nbsp;&nbsp; 
## **1.1. Previous efforts on ASL standardization relevant to the development of ASL Lexicon and Reporting Recommendation**

* A consensus statement of recommended implementations of ASL perfusion imaging for clinical applications (‘ASL White Paper <sup>1</sup>’), published by an expert group of members of the ISMRM Perfusion SG and the European Consortium for ASL in Dementia (European Cooperation in Science and Technology (EU-COST) Action BM1103). 
* Brain Image Data Structure (BIDS) extension for ASL <sup>4</sup> (which is referred to as ‘ASL-BIDS’ in this article): A community effort to standardize how to organize and share neuroimaging datasets, which was extended to include ASL in 2021 ([https://bids-specification.readthedocs.io/en/stable/04-modality-specific-files/01-magnetic-resonance-imaging-data.html#arterial-spin-labeling-perfusion-data](https://bids-specification.readthedocs.io/en/stable/04-modality-specific-files/01-magnetic-resonance-imaging-data.html#arterial-spin-labeling-perfusion-data)).
* Technical recommendations for renal ASL <sup>5</sup> from an international group of experts working under the framework of the PARENCHIMA project, funded by the EU COST Action CA16103 (referred to here as ‘PARENCHIMA renal ASL’).
* A series of extensions to the 2015 ASL White Paper (referred to as the ‘ASL Grey Papers’ in this article) on the following topics:
    * Velocity-selective arterial spin labeling perfusion MRI: A review of the state of the art and recommendations for clinical implementation <sup>6</sup>
    * Recent Technical Developments in ASL: A Review of the State of the Art <sup>7</sup>
    * Current state and guidance on arterial spin labeling perfusion MRI in clinical neuroimaging <sup>2</sup>
    * Update on state-of-the-art for arterial spin labeling (ASL) human perfusion imaging outside of the brain <sup>8</sup>
    * Quantitative Cerebral Perfusion MRI using Multi-timepoint Arterial Spin Labeling: Recommendations and Clinical Applications (in preparation)

&nbsp;&nbsp; 
## **1.2. Development process of ASL Lexicon and Reporting Recommendation**

The ASL Lexicon task force consists of eleven Perfusion SG members with diverse expertise in ASL imaging, who attended the launch events of OSIPI during and after the annual ISMRM meeting in 2019 and expressed their interest to contribute. The developmental process of the ASL Lexicon and Reporting Recommendation was as follows

**Stage 1 (June 2020 - April 2021):** Previously published ASL papers were reviewed by the task force members and comprehensive lists of ASL techniques, acquisition parameters, output derivatives, and physiological parameters required for quantification were compiled. Terminology was harmonized with other community efforts, as mentioned above. The Reporting Recommendation was also drafted based on the BIDS extension for ASL <sup>4</sup>, consisting of two recommendation levels:


* **Required: essential for meaningful interpretation of the ASL data and for quantitative analysis.** These must be included in an ASL publication in order for its data set to be ‘_OSIPI compliant_’.
* **Recommended: parameters that are useful for interpretation of the ASL data and could explain specific characteristics or systematic differences between data sets.** Authors are encouraged to include as many of these as possible in ASL publications.

**Stage 2 (June — July 2021):** a separate and independent expert panel provided feedback and comments on the Stage 1 draft. These experts are all currently involved with the development of a new set of ASL consensus review articles (the ‘ASL Grey Papers’; please see the previous subsection “1.2 Previous efforts on ASL standardization relevant to the development of ASL Lexicon and Reporting Recommendation”). Based on their feedback, an updated Stage 2 draft was generated.

**Stage 3 (June — October 2021):** A manufacturer survey was carried out with the major MRI scanner manufacturers (in alphabetical order: Canon, Fujifilm, GE, Philips, and Siemens) to identify any potential conflicts or incompatible terminologies and definitions with their current ASL product implementation. In addition, information was requested relating to if/how the acquisition parameters listed in the reporting recommendation can be obtained via the graphical user interface (GUI) of the commercial MRI scanners.

**Stage 4 (November 2021 - January 2022):** The draft document was shared with all members of the ISMRM Perfusion SG for general feedback and comments. Also, a survey was enclosed so that they could indicate if they agreed with the drafted Reporting Recommendation categories with regard to the ASL acquisition parameters. In the survey, the responders were provided with four options for each ASL acquisition parameter listed in the recommendation:

* Yes, I think “_Required/Recommended_” is the appropriate category for parameter “xxx”
* No, the parameter “xxx” should be in another category (i.e. _Recommended_ for _Required _/ _Required_ for _Recommended_)
* No, we should remove the parameter “xxx” from the recommendation
* I am not familiar with this parameter

On 19th November 2021, a virtual Q&A session was held with ISMRM Perfusion SG members, in which the concept of this initiative was explained and any queries were addressed. 

**Stage 5 (February 2022 - April 2022):** A total of 38 responses to the survey were collected and are summarized in Supporting Information Figure S1, S2 and S3, which are available online. Based on those responses, the reporting recommendation was finalized and is provided in ‘Section 3. Reporting Recommendation’. United Imaging also joined the manufacturer survey, and the summary of the survey responses from all six MRI manufacturers is provided in Supporting Information Figure S4 and S5, showing how the acquisition parameters listed in the Reporting Recommendation can be obtained via the commercial MRI scanner GUIs. It was found that, when the specific sequence/technique is implemented as a product, all corresponding parameters in the “Required” category were either displayed in the GUI or available on request from the manufacturers. In the “Recommended” category, however, several parameters are not available for some manufacturers. Therefore, the recommendation level remains that we only “encourage” authors to include as many of the recommended parameters as possible in ASL publications. After all feedback/comments were addressed, the ASL Lexicon was divided into two groups: (a) techniques and their parameters that are widely used and mature enough to be standardized, which are mostly covered by the ‘ASL White Paper’ and some (but not all) of the ‘ASL Grey Papers’, and (b) advanced and emerging techniques and their parameters. Only the former (i.e. (a)) is included in this manuscript, to avoid premature standardization of emerging techniques in a published article. The final draft of the manuscript was shared with the ISMRM Perfusion SG members for endorsement. 

**May 2022 - future:** the online version of the ASL Lexicon and Reporting Recommendation will be managed and updated by the community as further methods and improvements are developed. 

&nbsp;&nbsp; 
## **References**

1. 	Alsop DC, Detre JA, Golay X, et al. Recommended implementation of arterial spin-labeled perfusion MRI for clinical applications: A consensus of the ISMRM perfusion study group and the European consortium for ASL in dementia. _Magn Reson Med_. 2015;73(1):102-116. 

2. 	Lindner T, Bolar DS, Achten E, et al. Current state and guidance on arterial spin labeling perfusion MRI in clinical neuroimaging. _Magn Reson Med_. 2023;89(5):2024-2047. 

3. 	Harms MP, Somerville LH, Ances BM, et al. Extending the Human Connectome Project across ages: Imaging protocols for the Lifespan Development and Aging projects. _Neuroimage_. 2018;183:972-984. 

4. 	Clement P, Castellaro M, Okell TW, et al. ASL-BIDS, the brain imaging data structure extension for arterial spin labeling. _Scientific Data 2022 9:1_. 2022;9(1):1-8. 

5. 	Nery F, Buchanan CE, Harteveld AA, et al. Consensus-based technical recommendations for clinical translation of renal ASL MRI. _Magnetic Resonance Materials in Physics, Biology and Medicine_. 2020;33(1):141-161. 

6. 	Qin Q, Alsop DC, Bolar DS, et al. Velocity-selective arterial spin labeling perfusion MRI: A review of the state of the art and recommendations for clinical implementation. _Magn Reson Med_. 2022;88(4):1528-1547. 

7. 	Hernandez-Garcia L, Aramendía-Vidaurreta V, Bolar DS, et al. Recent Technical Developments in ASL: A Review of the State of the Art. _Magn Reson Med_. 2022;88(5):2021-2042. 

8. 	Taso M, Aramendía-Vidaurreta V, Englund EK, et al. Update on state-of-the-art for arterial spin labeling (ASL) human perfusion imaging outside of the brain. _Magn Reson Med_. 2023;89(5):1754-1776. 
