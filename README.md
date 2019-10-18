# IB-cGAN

Code for paper:

A modality conversion approach to MV-DRs and KV-DRRs registration using information bottlenecked conditional generative adversarial network.

Liu C1, Lu Z2, Ma L1, Wang L1, Jin X3, Si W4,5.
Author information
1
Ningbo Institute of Technology, Zhejiang University, Ningbo, 315100, China.
2
School of Aeronautics and Astronautics, Zhejiang University, Hangzhou, 310058, China.
3
Radiation and Medical Oncology Department, 1st Affiliated Hospital of Wenzhou Medical University, Wenzhou, 325003, China.
4
Internet of Things College, Shanghai Business School, Shanghai, 201400, China.
5
Huashan Hospital, Fudan University, Shanghai, 200031, China.

Abstract

PURPOSE:
As affordable equipment, electronic portal imaging devices (EPIDs) are wildly used in radiation therapy departments to verify patients' positions for accurate radiotherapy. However, these devices tend to produce visually ambiguous and low-contrast planar digital radiographs under megavoltage x ray (MV-DRs), which poses a tremendous challenge for clinicians to perform multimodal registration between the MV-DRs and the kilovoltage digital reconstructed radiographs (KV-DRRs) developed from the planning computed tomography. Furthermore, the existent of strong appearance variations also makes accurate registration beyond the reach of current automatic algorithms.

METHODS:
We propose a novel modality conversion approach to this task that first synthesizes KV images from MV-DRs, and then registers the synthesized and real KV-DRRs. We focus on the synthesis technique and develop a conditional generative adversarial network with information bottleneck extension (IB-cGAN) that takes MV-DRs and nonaligned KV-DRRs as inputs and outputs synthesized KV images. IB-cGAN is designed to address two main challenges in deep-learning-based synthesis: (a) training with a roughly aligned dataset suffering from noisy correspondences; (b) making synthesized images have real clinical meanings that faithfully reflects MV-DRs rather than nonaligned KV-DRRs. Accordingly, IB-cGAN employs (a) an adversarial loss to provide training supervision at semantic level rather than the imprecise pixel level; (b) an IB to constrain the information from the nonaligned KV-DRRs.

RESULTS:
We collected 2698 patient scans to train the model and 208 scans to test its performance. The qualitative results demonstrate realistic KV images can be synthesized allowing clinicians to perform the visual registration. The quantitative results show it significantly outperforms current nonmodality conversion methods by 22.37% (P = 0.0401) in terms of registration accuracy.

CONCLUSIONS:
The modality conversion approach facilitates the downstream MV-KV registration for both clinicians and off-the-shelf registration algorithms. With this approach, it is possible to benefit the developing countries where inexpensive EPIDs are widely used for the image-guided radiation therapy.


The code and model trained by pytorch will be released after acceptance.

We show some interesting videos below. The z is a latent representation vector with 8 elements.

1. We manipulate all the elements of z from -1 to 1 simultaneously. 

![](WGAN_SN_encodedZ.gif)
![](WGAN_SN_1.gif)

2. We manipulate z for a specific patient.

![](LR.png)

a) Varying all the elements of z from -1 to 1 simultaneously for a specific patient.

![](all_z.gif)

b) Varying the 3rd element of z from -1 to 1, and set all other elements to 0.

![](z3.gif)

c) Varying the 4-th element of z from -1 to 1, and set all other elements to 0.

![](z4.gif)

d) Varying the 5-th element of z from -1 to 1, and set all other elements to 0.

![](z5.gif)

e) Varying the 7-th element of z from -1 to 1, and set all other elements to 0.

![](z7.gif)

f) Varying the 8-th element of z from -1 to 1, and set all other elements to 0.

![](z8.gif)
