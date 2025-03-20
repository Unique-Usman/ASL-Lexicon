---
layout: page
title: Advanced ASL techniques and parameters
permalink: /advanced_asl_techniques/
---


![OSIPI logo](https://osipi.github.io/assets/img/logo.png)

&nbsp;&nbsp;

OSIPI Task force 4.1: ASL lexicon  
Milestone \#2:   
Advanced ASL techniques and parameters     

**Organization of this document**  
This document aims to organize comprehensive lists of consensus terminology for advanced ASL techniques and parameters, including acquisition protocol and output parameter maps. Source code for the LaTex equations is provided in a supplementary [document](https://docs.google.com/document/d/e/2PACX-1vQmi8TZWi8bqromDVylCEef0PnExt0b_EIBwgCKfVkBLGKqB_RgqBoc7uuiQrzpsQ/pub). Throughout the document, the following nomenclature is used:

* **Parameters:** Parameters are the quantities of interest of the ASL perfusion imaging and analysis. Output parameter maps are derived from the input dataset.  
* **Attributes:** Attributes are technical quantities or descriptions related to the imaging, analysis or pre-processing procedures. They define the performed steps of extracting parameters maps from the input dataset.

Within each individual section, parameters/concepts are organized into tables, where each parameter/concept should correspond to a single row in a table, with following items to be listed if applicable:

* **Name:** A unique name for the parameter or attribute.   
* **Notation:** If applicable, a commonly used abbreviation or acronym  
* **Description:** A short definition or specification; if available, a mathematical formula will be utilized as it provides a unique description of the quantity, regardless of varying nomenclature and interpretation.  
* **Dimension:** If applicable, the general physical units.  
* **Reference:** To the literature establishing the concept or corresponding analysis method and providing relevant details. If applicable the publication first introducing the respective technique is cited. For general concepts and quantities, review papers will be cited which give an overview of the general concept.

&nbsp;&nbsp;

**General classification**  
This document for “advanced ASL techniques and parameters” goes beyond the consensus paper for brain ASL perfusion imaging by the Perfusion Study Group of the International Society for Magnetic Resonance in Medicine (ISMRM) and the EU-COST action ‘ASL in dementia’ (Alsop et al., 2015). The standard techniques and parameters are found elsewhere. In this document, the term “labeling” is used throughout all techniques, which is however interchangeable to “tagging”.

**Advanced ASL Labeling Strategies**

| *Name* | *Notation* | *Description* | *References* |
| :---- | :---- | :---- | :---- |
| Transfer insensitive labeling technique | **TILT** | Version of PASL, in which labeling is achieved by two successive 90° radiofrequency (RF) pulses. For the control, the phase of the second pulse is shifted by 180°, thereby yielding no net effect on blood water magnetization | (Golay et al., 1999\)  |
| Flow encoding arterial spin tagging | **FEAST** | A technique based on (p)CASL that acquires a pair of ASL subtraction images with and without additional bipolar gradients for vascular crushing. The ATT is calculated using the ratio between (p)CASL images with and without vascular crushing | (Wang et al., 2003\)  |
| QUIPSS II with window-sliding saturation sequence | **Q2WISE** | A hybrid technique between Q2TIPS and QUIPSS II. In Q2WISE, the series of RF pulses (20-30 in Q2TIPS) is replaced by 2 thin saturation pulses and 1 thick slab saturation pulse to reduce the RF energy | (Song et al., 2012\)  |
| Velocity-selective ASL | **vs-ASL** | A spatially non-selective method in which blood spins flowing above a certain threshold velocity are saturated. Generally, the saturation (labeling) is achieved by a pulse train consisting of 90°, two adiabatic 180° (or BIR-8) and \-90° pulses in combination with velocity encoding gradients. Control images are acquired without velocity encoding gradients.       | (Wong et al., 2006\)  |
| Fourier-transform based Velocity-selective inversion ASL | **FT-VSI ASL** | A variation of vs-ASL, in which the magnetization within a certain velocity band is inverted by a train of composite pulses incorporating velocity-sensitive bipolar gradients and refocusing 180° pulses based on Fourier-transform of the B1 field. By achieving inversion of the magnetization, SNR can be improved as compared to the conventional vs-ASL. | (Qin and van Zijl, 2016\)  |
| Acceleration-selective ASL | **AccASL** | A spatially non-selective method similar to vs-ASL, but that labels (saturates) based upon the accelerating/decelerating blood spins instead of velocity. Since arterial blood exhibits stronger acceleration/deceleration, it labels predominantly arterial (as opposed to venous) blood. AccASL includes both CBF and CBV weighting.  | (Schmid et al., 2014\)  |
| External RF labelling coils |  | Placing external RF transmission coils over the artery/arteries of interest (on the neck), to reduce power deposition and avoid MT effects in the perfused organ | (Zhang et al., 1995\) |
| MR fingerprinting ASL | **MRF-ASL** | An ASL method which uses pseudo-random variation of the acquisition parameters, based on the principle of MR fingerprinting (MRF). By taking advantage of the rich information contained in the MRF sequence, multiple hemodynamic parameters such as B1+, T1, ATT and CBF can be estimated concomitantly. | (Su et al., 2017\)  (Zhang et al., 2020\)  |

**Multi-PLD and time-encoding approaches**

| Look-Locker | LL-ASL | Pulsed ASL technique in which images are acquired at multiple TI points after a single labeling pulse. Low flip angle readouts are used to avoid complete nulling of the label in the tissue by the first readouts. | (Gunther et al., 2001\)  |
| :---- | :---- | :---- | :---- |
| Quantitative STAR labeling of arterial regions | **QUASAR** | A model-free approach to obtain quantitative ASL data, based on convolution. The sequence has multiple Look-Locker readouts with two different flip angles after labeling while using a bolus saturation, and additional Look-Locker readouts with vascular crushing. | (Petersen et al., 2006\)  |
| Low-resolution ATT mapping |  | A fast multi PLD ASL implementation that is specifically used to acquire low spatial resolution arterial transit time maps. Typically used as ancillary scan to enhance the quantification accuracy of a single PLD ASL acquisition | (Dai et al., 2012\)  |
| time-encoded ASL (commonly referred to as Hadamard-encoded) | **te-ASL** | Segmenting the pCASL module into alternating control and label modules for each readout according to a matrix. This improves the temporal efficiency of ASL \- i.e. reduces the number of acquisitions required for a multi-PLD data set. The most typical implementation is Hadamard encoding. Modifications include for example Walsh-ordering.  | (Günther, 2007\) (Wells et al., 2010\) (Dai et al., 2013\) (Teeuwisse et al., 2014\) (von Samson-Himmelstjerna et al., 2016\) |

**Vessel-selective and territorial ASL approaches**

| Pencil beam | SASL | Selective labeling of an individual artery using 2D pencil beam RF pulses | (Davies and Jezzard, 2003\) |
| :---- | :---- | :---- | :---- |
| Anatomically tilted / slab-selective |  | Tilting the labeling plane that only blood flowing inside the artery of interest is being inverted or use a strict sagittal approach with suppression pulses | (Detre et al., 1994\) (Eastwood et al., 2002\) |
| Rotating oblique plane | **CASSL** | The CASL labeling plane is both tilted and rotating to label only one single artery | (Werner et al., 2005\) |
| Pulsed Star Labeling of Arterial Regions | **PULSAR** | STAR labeling in anatomically selective regions, combined with presaturation (rather than postsaturation) | (Golay et al., 2005\)  |
| Cycled ASL |  | A PASL technique that combines both anatomically tilted tagging volumes and label/control acquisition according to a Hadamard matrix | (Günther, 2006\)  |
| Vessel-encoded ASL | **VE-ASL** | modified pCASL labeling using additional transverse gradients and phase cycling to selectively tag particular arteries. Can use Hadamard vessel encoding or other schemes to generate vascular territory maps. | (Wong, 2007\)  |
| Super-selective/rotating encoded ASL | **ss-ASL** | Creating a labeling disc by incorporating additional gradients in x and y direction during pCASL labeling to choose a single artery | (Helle et al., 2010\) (Dai et al., 2010\) |
| Ternary encoded ASL |  | Encoding super-selective pCASL with a ternary matrix – i.e. a three-fold matrix \- without control condition | (Lindner et al., 2020\) |

**ASL Angiography**

| ASL-based MR Angiography | ASL-MRA | MR Angiography obtained by employing an ASL scheme combined with a high spatial resolution 3D (or 2D) readout module. Typically, the readout is performed immediately after the labeling while the labeled blood flows within the macro-vasculature. Not only a static 3D MRA, but also a dynamic MRA is obtainable by using Look-Locker readout or time-encoded ASL scheme. Both PASL and pCASL are applicable. | (Yan et al., 2010\) (Bi et al., 2010\) (Suzuki et al., 2019\) review  |
| :---- | :---- | :---- | :---- |
| Acquisition of ConTRol and labEled imaging in the Same Shot | **ACTRESS** | Look-locker sampling after ASL labeling. The first phase, in which labelled blood has not yet arrived in the imaging volume, serves as control condition, making the acquisition more efficient | (Y. Suzuki et al., 2018\)  |
| Vessel-selective ASL Angiography |  | Vessel-selective labeling combined with either static or dynamic readout | (Okell et al., 2010\) (Nakamura et al., 2013\) (Jensen-Kondering et al., 2015\) |
| Combined ASL and Phase Contrast Angiography |  | (super-selective) pseudo-continuous  labeling with phase-contrast readout | (Lindner et al., 2017\) |
| combined ASL angiography and perfusion |  | A simultaneous acquisition concept in which both angiographic (macro-vasculature) and subsequent perfusion (micro-vasculature) images are obtained by sharing the labeling module within a single ASL sequence.  | (Y. Suzuki et al., 2018\) (Okell, 2019\) |

**Modified ASL methods and methods for special derivatives**

| Attenuating the static signal in arterial spin tagging | ASSIST | FAIR ASL approach with multiple inversion pulses during the blood transit time (first implementation of background suppression) | (Ye et al., 2000\)  |
| :---- | :---- | :---- | :---- |
| T2-Relaxation-Under-Spin-Tagging | **TRUST** | A method to measure the cerebral metabolic rate of oxygen (CMRO2). TRUST MRI utilizes the spin tagging principle to label venous blood and uses T2-preparation pulses to modulate the signal with different T2-weightings and thereby measure venous oxygenation | (Lu and Ge, 2008\)  |
| Dual echo ASL BOLD |  | Acquiring ASL with two echoes, thus being able to extract both ASL signal and BOLD activation. Recently being used to also evaluate CMRO2 changes. | (Glover et al., 1996\) (Silva et al., 1999\) (Fernández-Seara et al., 2016\) (Englund et al., 2020\) |
| QUantitative Imaging of eXtraction of Oxygen and TIssue Consumption | **QUIXOTIC** | Method to measure OEF and CMRO2 which uses velocity-selective spin labeling to isolate MR signal exclusively from postcapillary venular blood on a voxel-by-voxel basis. Venous oxygenation is estimated via a T2 measurement of the isolated venular blood signal, and OEF and CMRO2 are calculated based on this. | (Bolar et al., 2011\)  |
| water-extraction-with-phase-contrast-arterial-spin-tagging | **WEP-CAST** | A method to study water extraction fraction map. Variant of the pCASL method that incorporates a phase-contrast velocity-encoding gradient and measures the amount of ASL signal that passes through into the venous outflow | (Lin et al., 2018\)  |
| Diffusion-weighted ASL | **DW-ASL** | A method which uses vascular crusher gradients to enable acquisition of ASL data with and without the intravascular contribution, and thereby allow estimation of IV-EV water exchange rate. | (Wang et al., 2007\) (Shao et al., 2019a)  |
| Magnetisation transfer weighted ASL | **MT-ASL** | A method to separate two compartments (capillary and brain tissue) of ASL signal based on the magnetisation transfer effects of tissue spins which are combined to large molecules. Water exchange rate across the blood-brain barrier can then be quantified | (Silva et al., 1997\) (Kim and Kim, 2005\)  |
| Multi-TE ASL |  | A method to measure apparent T2 of the perfusion signal with multiple echo times, and separate two compartments (capillary and brain tissue) of ASL signal based on their T2 differences. Water exchange rate across the blood-brain barrier can then be quantified. | (Wells et al., 2013\) (Gregori et al., 2013\) (Ohene et al., 2019\) (Schidlowski et al., 2020).  |
| Intrinsic Diffusivity Encoding of Arterial Labeled Spin | **IDEALS** | A method for whole-brain mapping of water permeability using separation of the intravascular and extravascular signal with segmented 3D-GRASE by modulating the relative sensitivity between relaxation, true diffusion, and pseudo diffusion. | (Wengler et al., 2019\)  |
| vascular space occupancy (VASO)-dependent functional MRI (fMRI)  | **VASO** | A method predominantly used for fMRI that detects changes in CBV by using a flow-independent inversion pulse. Readout is performed when blood signal is zero while tissue signal is positive. | (Lu et al., 2003\)  |
| inflow vascular-space-occupancy | **iVASO** | iVASO technique uses spatially selective inversion to suppress the signal from blood flowing into a slice, with a control scan to measure absolute arterial cerebral blood volume aCBV using cerebrospinal fluid (CSF) for signal normalization. | (Hua et al., 2011\)  |
| Arterial cerebral blood volume-weighted functional MRI using pseudocontinuous arterial spin tagging  | **AVAST**  | AVAST is a technique for fast imaging of aCBV signals suitable for functional imaging studies. AVAST was developed in order to achieve a contrast that depends on aCBV with little contamination from perfusion signals by taking advantage of the kinetics of the tag through the vasculature.  | (Jahanian et al., 2015\)  |

**Non-standard ASL derivative parameters**

| *Name* | *Notation* | *Unit* | *Description* | *References* |
| :---- | :---- | :---- | :---- | :---- |
| Tissue transit time | **TTT** or **𝜹** | ms | TTT is the time between the spins being labeled and arriving in the tissue compartment (after being transported from capillary to tissue). TTT can be quantified from the one compartment Kety model with a vascular compartment. | (Alsop and Detre, 1996\) (Wang et al., 2002\) |
| Pre-exchange lifetime, or mean blood water residence time, or  mean exchange time | **Tex or** e | ms | The difference between TTT and ATT (see standard techniques) | (Wells et al., 2013\) (Dickie et al., 2020\) |
| Arterial input function | **AIF**  | a.u. | Describes inflowing magnetization and is obtained by multiplication of the delivery function by 2M0b | (Knutsson, et al. 2008\) |
| Fractional arterial input function Delivery function | **c(t)** | fraction (0 to 1\) | Fractional signal in larger arteries. Corresponds to the normalized arterial concentration of magnetization and is subject to T1 decay. Its shape depends on the labeling type | (Knutsson, et al. 2008\) (Buxton, et al. 1998\) |
| Equilibrium water exchange rate from capillary to tissue | **kin or kw** | min-1 | Water exchange rate across the blood-brain barrier, which is mediated by multiple pathways including passive diffusion through endothelium, active cotransport (i.e. with ion channel), and diffusion through water channel proteins (aquaporin-4) at the end feet of astrocytes. This exchange rate can be quantified with the knowledge about the signal contributions in two compartments (capillary and tissue). | (Parkes and Tofts, 2002\) (Wang et al., 2007\) (St. Lawrence et al., 2012\) (Gregori et al., 2013\) (Dickie et al., 2020\) |
| Arterial blood flow | **aBF** | mL/mL/min | Arterial blood flow in large arteries can be quantified using model-free methods under the assumption of indicator-dilution theory from dynamic MR angiography with sufficient spatial and temporal resolution | (Shao et al., 2019b)  |
| Arterial cerebral blood volume | **aCBV** | % | aCBV is a vital indicator of tissue perfusion and vascular reactivity. aCBV can be measured by different approaches (iVASO, AVAST, dMRA, QUASAR, etc). | (Hua et al., 2011\) (Jahanian et al., 2015\) |
| Vascular compliance | **VC** |  | VC is defined as the ratio of change in arterial cerebral blood volume (ΔCBV) and change in arterial pressure (ΔBP) between the systolic and diastolic phases of the cardiac cycle. ΔCBV can be measured by synchronized dynamic ASL.  | (Yan et al., 2016\)  |
| Cerebrovascular reactivity  | **CVR** | Δ%CBF/mmHg | CVR is a measure of the change in cerebral blood flow for a given vasodilatory stimulus (i.e CO2, acetazolamide).  | (Tancredi et al., 2012\) |


&nbsp;&nbsp;

### **Partial volume effects**

![][image1]

(Asllani, et al. 2008\)

| *Name* | *Notation* | *Unit* | *Description* | *References* |
| :---- | :---- | :---- | :---- | :---- |
| Tissue partial volume | **pGM, pWM** | fraction (0 to 1\) | Partial volume of different tissue types (gray matter, white matter, cerebro-spinal fluid) as a fraction of the total voxel volume | (Asllani, et al. 2008\) |
| Tissue specific perfusion | **CBFGM CBFWM** |  | Tissue specific perfusion, corrected for the partial volume effects | (Asllani, et al. 2008\) |

### 

**ASL in body**

| Organ | *Name* | *Notation* | *Unit* | *Description* | *References* |
| :---- | :---- | :---- | :---- | :---- | :---- |
| Placenta | Placental Blood Flow / Placental perfusion | PBF | mL/100g/min | Perfusion value in placenta | (Shao et al., 2018\) (Zun and Limperopoulos, 2018\) |
| Kidney | Renal Blood Flow / Renal perfusion | RBF | mL/100g/min | Tissue perfusion value in kidney | (Nery et al., 2018\) (Odudu et al., 2018\) |
| Liver | Hepatic arterial perfusion |  | mL/100g/min | Perfusion arising from the hepatic arteries in liver | (Schalkx et al., 2015\) (Pan et al., 2016\) (Martirosian et al., 2019\) |
|  | Portal-venous perfusion |  | mL/100g/min | Perfusion arising from the portal veins in liver |  |
|  | Hepatic perfusion index | HPI | % | Percentage ratio of the hepatic arterial perfusion to the global liver perfusion |  |
| Heart | Myocardial blood flow | MBF | mL/100g/min | Perfusion value in myocardium | (Kober et al., 2016\) |
|  | Myocardial perfusion reserve | MPR |  | MPR was defined as the ratio of MBF at stress (i.e. using adenosine vasodilation) and at rest.  | (Yoon et al., 2017\) (Aramendía-Vidaurreta et al., 2020\) |

&nbsp;&nbsp;

**References:**  
Alsop, D.C., Detre, J.A., 1996\. Reduced transit-time sensitivity in noninvasive magnetic resonance imaging of human cerebral blood flow. J. Cereb. Blood Flow Metab. https://doi.org/10.1097/00004647-199611000-00019  
Aramendía-Vidaurreta, V., Echeverría-Chasco, R., Vidorreta, M., Bastarrika, G., Fernández-Seara, M.A., 2020\. Quantification of Myocardial Perfusion With Vasodilation Using Arterial Spin Labeling at 1.5T. J. Magn. Reson. Imaging 1–12. https://doi.org/10.1002/jmri.27396  
Asllani, I., Borogovac, A., Brown, T. R. (2008). Regression algorithm correcting for partial volume effects in arterial spin labeling MRI. Magn Reson Med. https://doi.org/10.1002/mrm.21670  
Bi, X., Weale, P., Schmitt, P., Zuehlsdorff, S., Jerecic, R., 2010\. Non-contrast-enhanced four-dimensional (4D) intracranial MR angiography: A feasibility study. Magn. Reson. Med. 63, 835–841. https://doi.org/10.1002/mrm.22220  
Bolar, D.S., Rosen, B.R., Sorensen, A.G., Adalsteinsson, E., 2011\. QUantitative Imaging of eXtraction of oxygen and TIssue consumption (QUIXOTIC) using venular-targeted velocity-selective spin labeling. Magn. Reson. Med. 66, 1550–1562. https://doi.org/10.1002/mrm.22946  
Buxton, R. B., Frank, L. R., Wong, E. C., Siewert, B., Warach, S., Edelman, R. R. (1998) A general kinetic model for quantitative perfusion imaging with arte- rial spin labeling. Magn. Reson. Med*.* https://doi.org/10.1002/mrm.1910400308  
Dai, W., Robson, P.M., Shankaranarayanan, A., Alsop, D.C., 2012\. Reduced resolution transit delay prescan for quantitative continuous arterial spin labeling perfusion imaging. Magn. Reson. Med. 67, 1252–1265. https://doi.org/10.1002/mrm.23103  
Dai, W., Robson, P.M., Shankaranarayanan, A., Alsop, D.C., 2010\. Modified pulsed continuous arterial spin labeling for labeling of a single artery. Magn. Reson. Med. 64, 975–982. https://doi.org/10.1002/mrm.22363  
Dai, W., Shankaranarayanan, A., Alsop, D.C., 2013\. Volumetric measurement of perfusion and arterial transit delay using hadamard encoded continuous arterial spin labeling. Magn. Reson. Med. https://doi.org/10.1002/mrm.24335  
Davies, N.P., Jezzard, P., 2003\. Selective arterial spin labeling (SASL): Perfusion territory mapping of selected feeding arteries tagged using two-dimensional radiofrequency pulses. Magn. Reson. Med. 49, 1133–1142. https://doi.org/10.1002/mrm.10475  
Detre, J.A., Zhang, W., Roberts, D.A., Silva, A.C., Williams, D.S., Grandis, D.J., Koretsky, A.P., Leigh, J.S., 1994\. Tissue specific perfusion imaging using arterial spin labeling. NMR Biomed. 7, 75–82. https://doi.org/10.1002/nbm.1940070112  
Dickie, B.R., Parker, G.J.M., Parkes, L.M., 2020\. Measuring water exchange across the blood-brain barrier using MRI. Prog. Nucl. Magn. Reson. Spectrosc. 116, 19–39. https://doi.org/10.1016/j.pnmrs.2019.09.002  
Eastwood, J.D., Holder, C.A., Hudgins, P.A., Song, A.W., 2002\. Magnetic resonance imaging with lateralized arterial spin labeling. Magn. Reson. Imaging 20, 583–586. https://doi.org/10.1016/S0730-725X(02)00536-2  
Englund, E.K., Fernández-Seara, M.A., Rodríguez-Soto, A.E., Lee, H., Rodgers, Z.B., Vidorreta, M., Detre, J.A., Wehrli, F.W., 2020\. Calibrated fMRI for dynamic mapping of CMRO2 responses using MR-based measurements of whole-brain venous oxygen saturation. J. Cereb. Blood Flow Metab. 40, 1501–1516. https://doi.org/10.1177/0271678X19867276  
Fernández-Seara, M.A., Rodgers, Z.B., Englund, E.K., Wehrli, F.W., 2016\. Calibrated bold fMRI with an optimized ASL-BOLD dual-acquisition sequence. Neuroimage 142, 474–482. https://doi.org/10.1016/j.neuroimage.2016.08.007  
Glover, G.H., Lemieux, S.K., Drangova, M., Pauly, J.M., 1996\. Decomposition of inflow and blood oxygen level-dependent (BOLD) effects with dual-echo spiral gradient-recalled echo (GRE) fMRI. Magn. Reson. Med. 35, 299–308. https://doi.org/10.1002/mrm.1910350306  
Golay, X., Petersen, E.T., Hui, F., 2005\. Pulsed Star Labeling of Arterial Regions (PULSAR): A robust regional perfusion technique for high field imaging. Magn. Reson. Med. https://doi.org/10.1002/mrm.20338  
Golay, X., Stuber, M., Pruessmann, K.P., Meier, D., Boesiger, P., 1999\. Transfer insensitive labeling technique (TILT): Application to multislice functional perfusion imaging. J. Magn. Reson. Imaging 9, 454–461. https://doi.org/10.1002/(SICI)1522-2586(199903)9:3\<454::AID-JMRI14\>3.0.CO;2-B  
Gregori, J., Schuff, N., Kern, R., Günther, M., 2013\. T2-based arterial spin labeling measurements of blood to tissue water transfer in human brain. J. Magn. Reson. Imaging 37, 332–342. https://doi.org/10.1002/jmri.23822  
Günther, M., 2007\. Highly efficient accelerated acquisition of perfusion inflow series by Cycled Arterial Spin Labeling. Proc. Intl. Soc. Mag. Reson. Med. 15, 380\.  
Günther, M., 2006\. Efficient visualization of vascular territories in the human brain by cycled arterial spin labeling MRI. Magn. Reson. Med. 56, 671–675. https://doi.org/10.1002/mrm.20998  
Gunther, M., Bock, M., Schad, L.R., 2001\. Arterial spin labeling in combination with a look-locker sampling strategy: Inflow turbo-sampling EPI-FAIR (ITS-FAIR). Magn. Reson. Med. 46, 974–984. https://doi.org/10.1002/mrm.1284  
Helle, M., Norris, D.G., Rüfer, S., Alfke, K., Jansen, O., Van Osch, M.J.P., 2010\. Superselective pseudocontinuous arterial spin labeling. Magn. Reson. Med. 64, 777–786. https://doi.org/10.1002/mrm.22451  
Hua, J., Qin, Q., Donahue, M.J., Zhou, J., Pekar, J.J., Van Zijl, P.C.M., 2011\. Inflow-based vascular-space-occupancy (iVASO) MRI. Magn. Reson. Med. 66, 40–56. https://doi.org/10.1002/mrm.22775  
Jahanian, H., Peltier, S., Noll, D.C., Garcia, L.H., 2015\. Arterial cerebral blood volume-weighted functional MRI using pseudocontinuous arterial spin tagging (AVAST). Magn. Reson. Med. 73, 1053–1064. https://doi.org/10.1002/mrm.25220  
Jensen-Kondering, U., Lindner, T., Van Osch, M.J.P., Rohr, A., Jansen, O., Helle, M., 2015\. Superselective pseudo-continuous arterial spin labeling angiography. Eur. J. Radiol. 84, 1758–1767. https://doi.org/10.1016/j.ejrad.2015.05.034  
Kim, T., Kim, S.G., 2005\. Quantification of cerebral arterial blood volume and cerebral blood flow using MRI with modulation of tissue and vessel (MOTIVE) signals. Magn. Reson. Med. 54, 333–342. https://doi.org/10.1002/mrm.20550  
Knutsson, L., Bloch, K. M., Holtås, S., Wirestam, R., Ståhlberg, F. (2008) Model-free arterial spin labelling for cerebral blood flow quantification: introduction of regional arterial input functions identified by factor analysis. Magn. Reson. Med. https://doi.org/10.1016/j.mri.2007.10.006  
Kober, F., Jao, T., Troalen, T., Nayak, K.S., 2016\. Myocardial arterial spin labeling. J. Cardiovasc. Magn. Reson. 18, 1–16. https://doi.org/10.1186/s12968-016-0235-4  
Lin, Z., Li, Y., Su, P., Mao, D., Wei, Z., Pillai, J.J., Moghekar, A., van Osch, M., Ge, Y., Lu, H., 2018\. Non-contrast MR imaging of blood-brain barrier permeability to water. Magn. Reson. Med. 80, 1507–1520. https://doi.org/10.1002/mrm.27141  
Lindner, T., Jansen, O., Helle, M., 2020\. Ternary encoded super-selective arterial spin labeling for time-resolved flow territory mapping. Phys. Med. Biol. 65\. https://doi.org/10.1088/1361-6560/ab7ef0  
Lindner, T., Larsen, N., Jansen, O., Helle, M., 2017\. Selective arterial spin labeling in conjunction with phase-contrast acquisition for the simultaneous visualization of morphology, flow direction, and velocity of individual arteries in the cerebrovascular system. Magn. Reson. Med. 78, 1469–1475. https://doi.org/10.1002/mrm.26542  
Lu, H., Ge, Y., 2008\. Quantitative evaluation of oxygenation in venous vessels using T2-relaxation-under-spin-tagging MRI. Magn. Reson. Med. 60, 357–363. https://doi.org/10.1002/mrm.21627  
Lu, H., Golay, X., Pekar, J.J., Van Zijl, P.C.M., 2003\. Functional magnetic resonance imaging based on changes in vascular space occupancy. Magn. Reson. Med. 50, 263–274. https://doi.org/10.1002/mrm.10519  
Martirosian, P., Pohmann, R., Schraml, C., Schwartz, M., Kuestner, T., Schwenzer, N.F., Scheffler, K., Nikolaou, K., Schick, F., 2019\. Spatial-temporal perfusion patterns of the human liver assessed by pseudo-continuous arterial spin labeling MRI. Z. Med. Phys. 29, 173–183. https://doi.org/10.1016/j.zemedi.2018.08.004  
Nakamura, M., Yoneyama, M., Tabuchi, T., Takemura, A., Obara, M., Tatsuno, S., Sawano, S., 2013\. Vessel-selective, non-contrast enhanced, time-resolved MR angiography with vessel-selective arterial spin labeling technique (CINEMA-SELECT) in intracranial arteries. Radiol. Phys. Technol. 6, 327–334. https://doi.org/10.1007/s12194-013-0204-7  
Nery, F., Gordon, I., Thomas, D., 2018\. Non-Invasive Renal Perfusion Imaging Using Arterial Spin Labeling MRI: Challenges and Opportunities. Diagnostics 8, 2\. https://doi.org/10.3390/diagnostics8010002  
Odudu, A., Nery, F., Harteveld, A.A., Evans, R.G., Pendse, D., Buchanan, C.E., Francis, S.T., Fernández-Seara, M.A., 2018\. Arterial spin labelling MRI to measure renal perfusion: a systematic review and statement paper. Nephrol. Dial. Transplant 33, ii15–ii21. https://doi.org/10.1093/ndt/gfy180  
Ohene, Y., Harrison, I.F., Nahavandi, P., Ismail, O., Bird, E. V., Ottersen, O.P., Nagelhus, E.A., Thomas, D.L., Lythgoe, M.F., Wells, J.A., 2019\. Non-invasive MRI of brain clearance pathways using multiple echo time arterial spin labelling: an aquaporin-4 study. Neuroimage 188, 515–523. https://doi.org/10.1016/j.neuroimage.2018.12.026  
Okell, T.W., 2019\. Combined angiography and perfusion using radial imaging and arterial spin labeling. Magn. Reson. Med. 81, 182–194. https://doi.org/10.1002/mrm.27366  
Okell, T.W., Chappell, M.A., Woolrich, M.W., Günther, M., Feinberg, D.A., Jezzard, P., 2010\. Vessel-encoded dynamic magnetic resonance angiography using arterial spin labeling. Magn. Reson. Med. 64, 430–438. https://doi.org/10.1002/mrm.22412  
Pan, X., Qian, T., Fernandez-Seara, M.A., Smith, R.X., Li, K., Ying, K., Sung, K., Wang, D.J.J., 2016\. Quantification of liver perfusion using multidelay pseudocontinuous arterial spin labeling. J. Magn. Reson. Imaging 43, 1046–1054. https://doi.org/10.1002/jmri.25070  
Parkes, L.M., Tofts, P.S., 2002\. Improved accuracy of human cerebral blood perfusion measurements using arterial spin labeling: Accounting for capillary water permeability. Magn. Reson. Med. 48, 27–41. https://doi.org/10.1002/mrm.10180  
Petersen, E.T., Lim, T., Golay, X., 2006\. Model-free arterial spin labeling quantification approach for perfusion MRI. Magn. Reson. Med. 55, 219–232. https://doi.org/10.1002/mrm.20784  
Qin, Q., van Zijl, P.C.M., 2016\. Velocity-selective-inversion prepared arterial spin labeling. Magn. Reson. Med. 76, 1136–1148. https://doi.org/10.1002/mrm.26010  
Schalkx, H.J., Petersen, E.T., Peters, N.H.G.M., Veldhuis, W.B., van Leeuwen, M.S., Pluim, J.P.W., van den Bosch, M.A.A.J., van Stralen, M., 2015\. Arterial and portal venous liver perfusion using selective spin labelling MRI. Eur. Radiol. 25, 1529–1540. https://doi.org/10.1007/s00330-014-3524-z  
Schidlowski, M., Boland, M., Rüber, T., Stöcker, T., 2020\. Blood–brain barrier permeability measurement by biexponentially modeling whole-brain arterial spin labeling data with multiple T2-weightings. NMR Biomed. 33, 1–12. https://doi.org/10.1002/nbm.4374  
Schmid, S., Ghariq, E., Teeuwisse, W.M., Webb, A., Van Osch, M.J.P., 2014\. Acceleration-selective arterial spin labeling. Magn. Reson. Med. https://doi.org/10.1002/mrm.24650  
Shao, X., Liu, D., Martin, T., Chanlaw, T., Devaskar, S.U., Janzen, C., Murphy, A.M., Margolis, D., Sung, K., Wang, D.J.J., 2018\. Measuring human placental blood flow with multidelay 3D GRASE pseudocontinuous arterial spin labeling at 3T. J. Magn. Reson. Imaging 47, 1667–1676. https://doi.org/10.1002/jmri.25893  
Shao, X., Ma, S.J., Casey, M., D’Orazio, L., Ringman, J.M., Wang, D.J.J., 2019a. Mapping water exchange across the blood–brain barrier using 3D diffusion-prepared arterial spin labeled perfusion MRI. Magn. Reson. Med. 81, 3065–3079. https://doi.org/10.1002/mrm.27632  
Shao, X., Zhao, Z., Russin, J., Amar, A., Sanossian, N., Wang, D.J.J., Yan, L., 2019b. Quantification of intracranial arterial blood flow using noncontrast enhanced 4D dynamic MR angiography. Magn. Reson. Med. 82, 449–459. https://doi.org/10.1002/mrm.27712  
Silva, A.C., Lee, S.P., Yang, G., Ladecola, C., Kim, S.G., 1999\. Simultaneous blood oxygenation level-dependent and cerebral blood flow functional magnetic resonance imaging during forepaw stimulation in the rat. J. Cereb. Blood Flow Metab. 19, 871–879. https://doi.org/10.1097/00004647-199908000-00006  
Silva, A.C., Zhang, W., Williams, D.S., Koretsky, A.P., 1997\. Estimation of water extraction fractions in rat brain using magnetic resonance measurement of perfusion with arterial spin labeling. Magn. Reson. Med. 37, 58–68. https://doi.org/10.1002/mrm.1910370110  
Song, R., Loeffler, R.B., Hillenbrand, C.M., 2012\. QUIPSS II with window-sliding saturation sequence (Q2WISE). Magn. Reson. Med. 67, 1127–1132. https://doi.org/10.1002/mrm.23093  
St. Lawrence, K.S., Owen, D., Wang, D.J.J., 2012\. A two-stage approach for measuring vascular water exchange and arterial transit time by diffusion-weighted perfusion MRI. Magn. Reson. Med. 67, 1275–1284. https://doi.org/10.1002/mrm.23104  
Su, P., Mao, D., Liu, P., Li, Y., Pinho, M.C., Welch, B.G., Lu, H., 2017\. Multiparametric estimation of brain hemodynamics with MR fingerprinting ASL. Magn. Reson. Med. 78, 1812–1823. https://doi.org/10.1002/mrm.26587  
Suzuki, Y., Fujima, N., Ogino, T., Meakin, J.A., Suwa, A., Sugimori, H., Van Cauteren, M., van Osch, M.J.P., 2018\. Acceleration of ASL-based time-resolved MR angiography by acquisition of control and labeled images in the same shot (ACTRESS). Magn. Reson. Med. 79\. https://doi.org/10.1002/mrm.26667  
Suzuki, Y., Fujima, N., van Osch, M.J.P., 2019\. Intracranial 3D and 4D MR Angiography Using Arterial Spin Labeling: Technical Considerations. Magn. Reson. Med. Sci. https://doi.org/10.2463/mrms.rev.2019-0096  
Suzuki, Yuriko, Helle, M., Koken, P., Van Cauteren, M., van Osch, M.J.P., 2018\. Simultaneous acquisition of perfusion image and dynamic MR angiography using time-encoded pseudo-continuous ASL. Magn. Reson. Med. 79, 2676–2684. https://doi.org/10.1002/mrm.26926  
Tancredi, F.B., Gauthier, C.J., Madjar, C., Bolar, D.S., Fisher, J.A., Wang, D.J.J., Hoge, R.D., 2012\. Comparison of pulsed and pseudocontinuous arterial spin-labeling for measuring CO2-induced cerebrovascular reactivity. J. Magn. Reson. Imaging 36, 312–321. https://doi.org/10.1002/jmri.23658  
Teeuwisse, W.M., Schmid, S., Ghariq, E., Veer, I.M., Van Osch, M.J.P., 2014\. Time-encoded pseudocontinuous arterial spin labeling: Basic properties and timing strategies for human applications. Magn. Reson. Med. 72, 1712–1722. https://doi.org/10.1002/mrm.25083  
von Samson-Himmelstjerna, F., Madai, V.I., Sobesky, J., Guenther, M., 2016\. Walsh-ordered hadamard time-encoded pseudocontinuous ASL (WH pCASL). Magn. Reson. Med. 76, 1814–1824. https://doi.org/10.1002/mrm.26078  
Wang, J., Alsop, D.C., Li, L., Listerud, J., Gonzalez-At, J.B., Schnall, M.D., Detre, J.A., 2002\. Comparison of quantitative perfusion imaging using arterial spin labeling at 1.5 and 4.0 Tesla. Magn. Reson. Med. 48, 242–254. https://doi.org/10.1002/mrm.10211  
Wang, J., Alsop, D.C., Song, H.K., Maldjian, J.A., Tang, K., Salvucci, A.E., Detre, J.A., 2003\. Arterial transit time imaging with flow encoding arterial spin tagging (FEAST). Magn. Reson. Med. 50, 599–607. https://doi.org/10.1002/mrm.10559  
Wang, J., Fernández-Seara, M.A., Wang, S., St Lawrence, K.S., 2007\. When perfusion meets diffusion: In vivo measurement of water permeability in human brain. J. Cereb. Blood Flow Metab. 27, 839–849. https://doi.org/10.1038/sj.jcbfm.9600398  
Wells, J.A., Lythgoe, M.F., Gadian, D.G., Ordidge, R.J., Thomas, D.L., 2010\. In vivo Hadamard encoded Continuous arterial spin labeling (H-CASL). Magn. Reson. Med. 63, 1111–1118. https://doi.org/10.1002/mrm.22266  
Wells, J.A., Siow, B., Lythgoe, M.F., Thomas, D.L., 2013\. Measuring biexponential transverse relaxation of the ASL signal at 9.4 T to estimate arterial oxygen saturation and the time of exchange of labeled blood water into cortical brain tissue. J. Cereb. Blood Flow Metab. 33, 215–224. https://doi.org/10.1038/jcbfm.2012.156  
Wengler, K., Bangiyev, L., Canli, T., Duong, T.Q., Schweitzer, M.E., He, X., 2019\. 3D MRI of whole-brain water permeability with intrinsic diffusivity encoding of arterial labeled spin (IDEALS). Neuroimage 189, 401–414. https://doi.org/10.1016/j.neuroimage.2019.01.035  
Werner, R., Norris, D.G., Alfke, K., Mehdorn, H.M., Jansen, O., 2005\. Continuous artery-selective spin labeling (CASSL). Magn. Reson. Med. https://doi.org/10.1002/mrm.20475  
Wong, E.C., 2007\. Vessel-encoded arterial spin-labeling using pseudocontinuous tagging. Magn. Reson. Med. 58, 1086–1091. https://doi.org/10.1002/mrm.21293  
Wong, E.C., Cronin, M., Wu, W.C., Inglis, B., Frank, L.R., Liu, T.T., 2006\. Velocity-selective arterial spin labeling. Magn. Reson. Med. https://doi.org/10.1002/mrm.20906  
Yan, L., Liu, C.Y., Smith, R.X., Jog, M., Langham, M., Krasileva, K., Chen, Y., Ringman, J.M., Wang, D.J.J., 2016\. Assessing intracranial vascular compliance using dynamic arterial spin labeling. Neuroimage 124, 433–441. https://doi.org/10.1016/j.neuroimage.2015.09.008  
Yan, L., Wang, S., Zhuo, Y., Wolf, R.L., Stiefel, M.F., An, J., Ye, Y., Zhang, Q., Melhem, E.R., Wang, D.J.J., 2010\. Unenhanced dynamic MR angiography: High spatial and temporal resolution by using true FISP-based spin tagging with alternating radiofrequency. Radiology 256, 270–279. https://doi.org/10.1148/radiol.10091543  
Ye, F.Q., Frank, J.A., Weinberger, D.R., McLaughlin, A.C., 2000\. Noise reduction in 3D perfusion imaging by attenuating the static signal in arterial spin tagging (ASSIST). Magn. Reson. Med. 44, 92–100. https://doi.org/10.1002/1522-2594(200007)44:1\<92::AID-MRM14\>3.0.CO;2-M  
Yoon, A.J., Do, H.P., Cen, S., Fong, M.W., Saremi, F., Barr, M.L., Nayak, K.S., 2017\. Assessment of segmental myocardial blood flow and myocardial perfusion reserve by adenosine-stress myocardial arterial spin labeling perfusion imaging. J. Magn. Reson. Imaging 46, 413–420. https://doi.org/10.1002/jmri.25604  
Zhang, Q., Su, P., Chen, Z., Liao, Y., Chen, S., Guo, R., Qi, H., Li, X., Zhang, X., Hu, Z., Lu, H., Chen, H., 2020\. Deep learning–based MR fingerprinting ASL ReconStruction (DeepMARS). Magn. Reson. Med. 84, 1024–1034. https://doi.org/10.1002/mrm.28166  
Zhang, W., Silva, A.C., Williams, D.S., Koretsky, A.P., 1995\. NMR Measurement of Perfusion Using Arterial Spin Labeling Without Saturation of Macromolecular Spins. Magn. Reson. Med. 33, 370–376. https://doi.org/10.1002/mrm.1910330310  
Zun, Z., Limperopoulos, C., 2018\. Placental perfusion imaging using velocity-selective arterial spin labeling. Magn. Reson. Med. 80, 1036–1047. https://doi.org/10.1002/mrm.27100  


[image1]: <data:image/png;base64,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>

&nbsp;&nbsp;
