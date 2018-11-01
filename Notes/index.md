
## Electromagnetics
Quantities/Names | Formulas
---- | ----
E-field boundary condition | $(\vec{E_2}-\vec{E_1}) \times \hat{n}= \vec{M_s}$
H-field boundary condition | $\hat{n} \times (\vec{H_2}-\vec{H_1})  = \vec{J_s}$
D-field boundary condition | $(\vec{D_2}-\vec{D_1}) \cdot \hat{n}= \rho_s$
B-field boundary condition | $(\vec{B_2}-\vec{B_1}) \cdot \hat{n}= 0$
$\hat{n}$ from medium 1 to 2
Quantities/Names | Formulas
---- | ----
Poynting Vector | $\vec{S} = \frac{1}{2}\vec{E} \times \vec{H}^*$
power dissipated | $P_{diss} = \iiint_V \frac{1}{2}\sigma\lvert\vec{E}\rvert dV$
electric energy stored | $W_e = \frac{1}{2}\iiint_V \frac{1}{2}\epsilon\lvert\vec{E}\rvert dV$
magnetic energy stored | $W_e = \frac{1}{2}\iiint_V \frac{1}{2}\mu\lvert\vec{H}\rvert dV$
source power | $P_s = -\iiint_V \frac{1}{2}(\vec{E}\cdot\vec{J}^*+\vec{H}^*\cdot\vec{M})dV$

Quantities/Names | Formulas
---- | ----
wave equation for $\vec{A}$ | $\nabla^2\vec{A}+k ^2\vec{A} = -\mu\vec{J}$
solution to <br/> wave equation for $\vec{A}$ | $\vec{A} = \iiint_{V'}\mu\vec{J}\frac{e^{-jk  R}}{4\pi R}dV$
solving $\vec{H}$ from $\vec{A}$ | $\vec{H} = \frac{1}{\mu}\nabla\times\vec{A}$
solving $\vec{E}$ from $\vec{A}$ | $\vec{E} = -j\omega\vec{A}-j\frac{1}{\omega\mu\epsilon}\nabla(\nabla\cdot\vec{A})$

## Some Maths
Quantities/Names | Formulas
---- | ----
integral in radiated power of ideal dipole|$\int_0^\pi (\sin\theta)^3 d\theta = \frac{4}{3}$
integral in fields of finite length dipole <br/> (refer to lecture 2 p.15)| $\int_{-\frac{L}{2}}^\frac{L}{2} \sin k(\frac{L}{2}-\lvert z'\rvert)e^{jkz'\cos\theta} dz'$ <br/> $= \frac{2}{k\sin\theta} \frac{\cos\left(\frac{kL}{2}\cos\theta\right)-\cos\frac{kL}{2}}{\sin\theta}$ <br/> $= \frac{2}{k\sin\theta}P(\theta)$

## Definitions
Quantities/Names | Definitions
---- | ----
radiation pattern | variation of the radiated electric field over a spherical surface
## General Relations
Quantities/Names | Formulas
---- | ----
complex power density <br/> (Poynting vector) | $\vec{S} = \frac{1}{2}\vec{E} \times \vec{H}^*$
radiation intensity | $U = \operatorname{Re}\{\vec{S}\} \cdot \hat{r} r^2$
complex power flowing out <br/> through S| $P_{rad} = \iint_S \vec{S} \cdot d\vec{S}$
differential area | $d\vec{S}  = \hat{r} r^2\sin\theta d\theta d\phi = \hat{r} r^2d\Omega$
differential solid angle | $d\Omega = \sin\theta d\theta d\phi$
radiated power | $P_{rad} = \int_0^{2\pi}\int_0^\pi \operatorname{Re}\{\vec{S}\}\hat\cdot{r}r^2\sin\theta d\theta d\phi = \iint U d\Omega$
integral of differential solid angle | $\iint d\Omega = 4\pi$
integral of directivity | $\iint D d\Omega = 4\pi$

## Radiation Characteristics
Quantities/Names | Formulas
---- | ----
normalized field patter <br/> (field pattern function)| $F = \frac{\lvert\vec{E}\rvert}{\operatorname{max}\{\lvert\vec{E}\rvert\}}$
average radiation intensity | $U_{av} = \frac{P_{rad}}{4\pi}$
directivity | $D = \frac{U}{U_{av}}=\frac{4\pi U}{P_{rad}}$
normalized radiation intensity pattern <br/> (power pattern function)| $$
beam solid angle | $\Omega_A = \iint \lvert F\rvert^2 d\Omega$
another formula for radiated power | $P_{rad} = U_m \Omega_A$
gain | $G(\theta, \phi) = \frac{U(\theta, \phi)}{\frac{P_{in}}{4\pi}}$

## Ideal Dipole
Quantities/Names | Formulas
---- | ----
magnetic vector potential $\vec{A}$ | $\vec{A} = \hat{z}\mu I\Delta z\frac{e^{-jk  r}}{4\pi r}$
magnetic field $\vec{H}$ <br/> (full expression)| $\vec{H} = \hat{\phi} jk  I \Delta z\sin{\theta}\left(1+\frac{1}{jk  r}\right)\frac{e^{-jk  r}}{4\pi r}$
electric field $\vec{E}$ <br/> (full expression)| $\vec{E} = \hat{\theta} j\omega\mu I \Delta z\sin{\theta} \left(1+\frac{1}{jk  r}+\frac{1}{(jk  r)^2}\right)\frac{e^{-jk  r}}{4\pi r}+$<br/>$\hat{r}j\omega\mu I \Delta z\cos{\theta\left(\frac{1}{jk  r}+\frac{1}{(jk  r)^2}\right)}\frac{e^{-jk  r}}{2\pi r}$
magnetic field $\vec{H}$ <br/> (far field)| $\vec{H} = \hat{\phi} jk  I \Delta z\sin{\theta}\frac{e^{-jk  r}}{4\pi r}$<br/>$=\hat{\phi}\frac{1}{\eta}j\omega A_z\sin{\theta}$
electric field $\vec{E}$ <br/> (far field)| $\vec{E} = \hat{\theta} j\omega \mu  I \Delta z\sin{\theta}\frac{e^{-jk  r}}{4\pi r}$<br/>$=\hat{\theta}j\omega A_z\sin{\theta}$
radiated power density | $\vec{S} = \hat{r}\frac{1}{2}\omega\mu k I^2(\Delta z \sin\theta)^2\frac{1}{(4\pi r)^2}$
radiated power | $P_{rad} = \frac{\omega\mu k}{12\pi}(I\Delta z)^2$
radiation resistance | $R_{rad} = 80\pi^2\left(\frac{\Delta z}{\lambda}\right)^2$
reactive power density <br/> (near field) | $\vec{S}^{nf} = $

## Finite Length Dipole
Quantities/Names | Formulas
---- | ----
current distribution | $I(z') = I_m\sin k(\frac{L}{2}-\lvert z'\rvert)$
pattern factor | $P(\theta) = \frac{\cos\left(\frac{kL}{2}\cos\theta\right)-\cos\frac{kL}{2}}{\sin\theta}$
magnetic vector potential $\vec{A}$ | $\vec{A} = $
magnetic field $\vec{H}$ <br/> (far field)| $\vec{H} = \hat{\phi} j I_m\frac{e^{-jkr}}{2\pi r}P(\theta)$
electric field $\vec{E}$ <br/> (far field)| $\vec{E} = \hat{\theta} j\eta I_m\frac{e^{-jkr}}{2\pi r}P(\theta)$
effective length (height) | $\frac{2I_m}{kI(0)}P(\theta)$

## Ideal Loop
Quantities/Names | Formulas
---- | ----
magnetic vector potential $\vec{A}$ | $\vec{A} = \hat{\phi}j\mu I(kS\sin\theta)\frac{e^{-jk  r}}{4\pi r}$
magnetic field $\vec{H}$ <br/> (far field)| $\vec{H} = \hat{\theta} jk  I \Delta z\sin{\theta}\frac{e^{-jk  r}}{4\pi r}$<br/>$=\hat{\theta}\frac{1}{\eta}j\omega A_\phi$
electric field $\vec{E}$ <br/> (far field)| $\vec{E} = \hat{\phi} j\omega \mu  I \Delta z\sin{\theta}\frac{e^{-jk  r}}{4\pi r}$<br/>$=-\hat{\phi}j\omega A_\phi$

## Long-Wire Antennas
Quantities/Names | Formulas
---- | ----

## Antenna Reception
Quantities/Names | Definitions
---- | ----
maximum available received power ($P_{rm}$) | 
maximum effective aperture ($A_{em}$) | 

Quantities/Names | Formulas
---- | ----
received power | $P_{r} = \frac{1}{2}{\lvert\frac{V_A}{Z_A+Z_L}\rvert}^2R_L$
maximum available received power ($P_{rm}$) | $P_{rm} = SA_{em}$
maximum effective aperture ($A_{em}$) | $A_{em} = \frac{P_{rm}}{S}$
effective aperture ($A_e$) | $A_e = e_r A_{em}$
available power ($P_A$) | $P_A = SA_e$
relation between gain and effective aperture | $G = \frac{4\pi}{\lambda^2}A_e$
