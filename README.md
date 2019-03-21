# mirage in temporal correlation

This is the repository of the published paper
 "Mirage in Temporal Correlation functions for Baryon-Baryon
Interaction in Lattice QCD", JHEP1610(2016)101,
DOI:10.1007/JHEP10(2016)101 [arXiv:1607.06371[hep-lat]](https://arxiv.org/abs/1607.06371).

The two-baryon systems ($\Xi\Xi$ and $NN$), triton and helium from 2+1 flavor lattice QCD
at pion mass 510 MeV on four lattice volumes from two quark sources are studied.

* data : Directory of data
  + Eeffs.pickle : effective energy shifts of two-baryon, triton, helium

    $E_\mathrm{eff}(t) = \log \frac{C_\mathrm{BB}(t)}{C_\mathrm{BB}(t+1)}$

    with the two-baryon propagator
    $C_\mathrm{BB}(t) = \langle B(t)^2 \bar{B}(0)^2 \rangle$.

  + Meffs.pickle : effective masses of nucleon and $\Xi$

    $M_\mathrm{eff}(t) = \log \frac{C_\mathrm{B}(t)}{C_\mathrm{B}(t+1)}$

    with the single baryon propagator
    $C_\mathrm{B}(t) = \langle B(t) \bar{B}(0) \rangle$.

  + dEeffs.pickle : the effective energy shifts

    $\Delta E_\mathrm{eff}(t) \equiv \frac{R(t)}{R(t+1)}$
    with $R(t) = C_\mathrm{BB}(t)/\{C_\mathrm{B}(t)\}^2$.

  + dE_fits.pickle : the plateau values of the effective energy shift

    $\Delta E_\mathrm{eff}(t) \rightarrow \Delta E_L$ (reliable?)

  + dEeffs_proj.pickle : sink operator projected effective energy shift

    $C_\mathrm{BB}^g(t) = \sum_r g(r) \sum_x \langle B(x + r,t) B(x, t) \overline{\mathcal{J}}(t=0)\rangle$

By using python3, these data are available as follows.
```
import pickle

with open('Eeffs.pickles', 'rb') as f:
  Eeffs = pickle.load(f)
```

* notes : Jupyternotebook to plot figures
    (style of thees pictures differ from the original published ones)

  + effective energy shifts.ipynb

    plot effective energy shifts in Appendix B

  + mock-up effective energies.ipynb

    generate the mock-up effective energy shift in Sec. 2

    one can plot the mock-up plateaux with arbitrary parameters

  + sink operator dependence.ipynb

    plot effective energy shifts with sink operator projected correlator
    for $\Xi\Xi$(1S0) at L = 48 in Appendix A

  + triton and helium.ipynb

    plot effective energy, energy shifts, and infinite volume limit

  + two-baryon systems.ipynb

    plot effective mass, energy, energy shifts, and infinite volume limit


* figs : figures
