# IB-cGAN
Code for paper IB-cGAN

The code and model trained by pytorch will be released after acceptance.


We show some interesting videos below. The z is a latent representation vector with 8 elements.

1. We manupulate all the elements of z from -1 to 1 simultaneously. 

![](WGAN_SN_encodedZ.gif)
![](WGAN_SN_1.gif)

2. We manupulate z for for a specific patient.

![](LR.png)

a) Varing all the elements of z from -1 to 1 simultaneously for a specific patient.

![](all_z.gif)

b) Varing the 3-th element of z from -1 to 1, and set all other elements to 0.

![](z3.gif)

c) Varing the 4-th element of z from -1 to 1, and set all other elements to 0.

![](z4.gif)

d) Varing the 5-th elements of z from -1 to 1, , and set all other elements to 0.

![](z5.gif)

e) Varing the 7-th elements of z from -1 to 1, , and set all other elements to 0.

![](z7.gif)

f) Varing the 8-th elements of z from -1 to 1, , and set all other elements to 0.

![](z8.gif)
