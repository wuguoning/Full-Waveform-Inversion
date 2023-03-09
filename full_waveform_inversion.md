# FULL WAVEFORM INVERSION

##  Full waveform inversion is a high resolution seismic imaging technique 
that is based on using the entire content of seismic traces for extracting
physical parameters of the medium sampled by seismic waves.

## Forward simulation
### Absorbing boundary conditions for the numerical simuation of waves[1]

When calculating solutions to partial differential equations (PDE) it is often
essential to introduce artificial boundaries to limit the area of computation.
We needs boundary conditions at these artificial boundaries in order to guarantee
a unique and well-posed solution to the differential equation.

The wave equation:
$$\frac{\partial^2 w}{\partial t^2} - \frac{\partial^2 w}{\partial x^2} - \frac{\partial^2 w}{\partial y^2} = 0 $$



## Full waveform inversion

Although FWI can achieve high accuracy when the full seismic waveform is matched,
the non-linearity of FWI suffers from local minima due to cycle skipping in the 
wave oscillations used to the form the objective function, i.e. a L_2-norm loss.

1. One solution is to recover or predict the missing low frequency content, such 
as through envelope inversion (Bozdag et al., 2011; Wu et al., 2014).

2. Another solution is to add regularization and preconditioning, such as 
Laplacian smoothing (Burstedde and Ghattas, 2009), L_2 norm penalty (Hu et al., 2009),
L_1-norm penalty (total variation) (Guitton, 2012; Esser et al., 2018), and 
prior information as constraints (Asnaashari et al., 2013).

3. In recent years, the success of deep learning in compter vision, natural language 
processing, and many other fields has drawn attention to its potential application in
FWI (Adler et al., 2021).

  1. One research direction is to build a direct inverse mapping from observations 
  to subserfaces structure by training neural networks on paired data of seismic 
  waveforms and velocity models (Wu et al., 2018; Yang and Ma, 2019; Li et al., 2019
  Kazei et al., 2021). This approach does not rely on solving the wave equation 
  but instead treat FWI as a data-driven machine learning problem similar to that in 
  image recognition. The accuracy and generalization of this approach, however, cannot
  be guaranteed with PDF constraint in FWI.

  2. Another research direction is to apply deep learning as an effective signal 
  processing tool to improve the optimization process of conventional FWI. Fow example 
  several studies applied neural networks to extrapolate the missing low frequencies
  and help mitigate the cycle skipping problem (Ovcharenko et al., 2019; Sun and Demanet, 
  2020; Hu et al., 2021). In addition to these data-driven approaches, another promising 
  direction is to combine neural networks and PDFs to formulate FWI as a physical-
  constrained machine problem (Richardson, 2018a; Mosser et. al., 2020; Wu and McMechan, 2019,
  2020; He and Wang, 2021).

  3. Ulyanov et al. (2018)'s work on deep image prior demonstrated that the CNN 
  architecture without pre-training can be used as a prior with excellent results 
  in inverse problems of computer vision, such as denoising, super-resolution, and 
  impainting.



[1]: (https://authors.library.caltech.edu/34673/) B. Engquist and A. Majda, 
Absorbing boundary conditions for the numerical simulation of waves. 
Mathmatics of Computution, 1977,31(139):629-651


