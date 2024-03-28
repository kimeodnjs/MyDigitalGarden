---
title: Chapter 1. Fundamentals of Radiative Transfer
tags: [astronomy]
date:
---
## 하위 레벨
[[1. The Electromagnetic Spectrum; Elementary Properties of Radiation]]

[[2. Radiative Flux]]

## 3. The Specific Intensity and Its Moments
<hr>

### 3. 1 Definition of Specific Intensity or Brightness
<hr>

&ensp;The flux is a measure of the energy carried by *all rays* passing through a given area. A more detailed description of radiation is to give the energy carried along by *individual rays*(or sets of rays). The appropriate definition is the following: Construct an area $\mathrm{d}A$ normal to the direction of the given ray and consider all rays passing through $\mathrm{d}A$ whose direction is within a solid angle $\mathrm{d}\Omega$ of the given ray. 

<br>

![figure2](https://velog.velcdn.com/images/dae_111/post/27d64777-5435-432a-8e22-dcdbafc8d656/image.png)

<br>

&ensp;The energy crossing $\mathrm{d}A$ in time $\mathrm{d}t$ and in frequency range $\mathrm{d}\nu$ is then defined by the relation
$$\mathrm{d}E = I_{\nu}\mathrm{d}A\mathrm{d}t\mathrm{d}\Omega\mathrm{d}\nu$$
where $I_{\nu}$ is the *specific intensity* or *brightness*.
$${\therefore}{\,}I_{\nu} = erg{\,}s^{-1}{\,}cm^{-2}{\,}ster^{-1}{\,}Hz^{-1}$$.

<br>

> [!note]
> $I_{\nu}$ depends on location in space, on direction, and on frequency.

<br>
<br>
<br>

### 3. 2 Net Flux and Momentum Flux
<hr>

&ensp;Suppose that we have a radiation field(rays in all directions) and construct a small element of area $\mathrm{d}A$ at some arbitrary orientation $\mathbf{n}$.

<br>

![figure3](https://velog.velcdn.com/images/dae_111/post/1b8ef11a-ce5f-4986-ac77-39891d07609c/image.png)

<br>

&ensp;Then the differential amount of flux from the solid angle $\mathrm{d}\Omega$ is
$$\mathrm{d}F_{\nu}(erg{\,}s^{-1}{\,}cm^{-2}{\,}Hz^{-1}) = I_{\nu}\cos\theta{\,}\mathrm{d}\Omega$$
The *net flux* in the direction $\mathbf{n}$, $F_{\nu}(\mathbf{n})$ is obtained by integrating $\mathrm{d}F$ over all solid angles:
$$F_{\nu} = {\intop}I_{\nu}\cos\theta{\,}\mathrm{d}\Omega$$

<br>

> [!note]
> If $I_{\nu}$ is an isotropic radiation field(not a function of angle), then net flux is *zero*, since ${\intop}\cos\theta{\,}\mathrm{d}\Omega = 0$. There is just as much energy crossing $\mathrm{d}A$ in the $\mathbf{n}$ direction as the $-\mathbf{n}$ direction.

<br>

&ensp;To get the flux of momentum normal to $\mathrm{d}A$(momentum per unit time per unit area = pressure), remember that the momentum of a photon is $E/c$. Then the momentum flux along the ray at angle $\theta$ is $\mathrm{d}F_{\nu}/c$. To get the component of momentum flux normal to $\mathrm{d}A$, we multiply by another factor of $\cos\theta$. Integrating, we obtain
$$p_{\nu}(dynes{\,}cm^{-2}{\,}Hz^{-1}) = \frac{1}{c}{\intop}I_{\nu}\cos^2\theta{\,}\mathrm{d}\Omega$$.

<br>

> [!note]
> $F_{\nu}$ and $p_{\nu}$ are *moments*(multiplications by powers of $\cos\theta$ and integration over $\mathrm{d}\Omega$) of the intensity $I{\nu}$. 

<br>

&ensp;Similarly, we get the total
$$F(erg{\,}s^{-1}{\,}cm^{-2}) = {\intop}F_{\nu}\mathrm{d}{\nu}$$
$$p(dynes{\,}cm^{-2}) = {\intop}p_{\nu}\mathrm{d}{\nu}$$
$$I(erg{\,}s^{-1}{\,}cm^{-2}{\,}ster^{-1}) = {\intop}I_{\nu}\mathrm{d}{\nu}$$

<br>
<br>
<br>

### 3. 3 Radiative Energy Density
<hr>

&ensp;The specific energy density $u_{\nu}$ is defined as the energy per unit volume per unit frequency range. To determine this, it is convenient to consider first the energy density per unit solid angle $u_{\nu}(\Omega)$ by $\mathrm{d}E = u_{\nu}(\Omega)\mathrm{d}V\mathrm{d}\Omega\mathrm{d}\nu$ where $\mathrm{d}V$ is a volume elemt. Consider a cylinder about a ray of length $ct$.

<br>

![figure4](https://velog.velcdn.com/images/dae_111/post/a1c280bc-34ff-47ed-b116-0872d68d58d2/image.png)

<br>

&ensp;Since the volume of the cylinder is $\mathrm{d}A{\,}c\mathrm{d}t$,
$$\mathrm{d}E = u_{\nu}(\Omega)\mathrm{d}Ac{\,}\mathrm{d}t\mathrm{d}\Omega\mathrm{d}\nu$$

<br>

&ensp;Radiation travels at velocity $c$, so that in time $\mathrm{d}t$ all the radiation in the cylinder will pass out of it:
$$\mathrm{d}E = I_{\nu}\mathrm{d}A\mathrm{d}\Omega\mathrm{d}t\mathrm{d}\nu$$
$${\therefore}{\,}u_{\nu}(\Omega) = \frac{I_{\nu}}{c}$$

<br>

&ensp;Integrating over all solid angles we have
$$u_{\nu} = {\intop}u_{\nu}(\Omega)\mathrm{d}\Omega = \frac{1}{c}{\intop}I_{\nu}\mathrm{d}\Omega$$
or
$$u_{\nu} = \frac{4\pi}{c}J_{\nu}$$
where we have defined the *mean intensity* $J_{\nu}$:
$$J_{\nu} = \frac{1}{4\pi}{\intop}I_{\nu}\mathrm{d}\Omega$$

<br>

&ensp;The total radiation density($erg{\,}cm^{-3}$) is obtained by integrating $u_{\nu}$ over all frequencies
$$u = {\intop}u_{\nu}\mathrm{d}\nu = \frac{4\pi}{c}{\intop}J_{\nu}\mathrm{d}\nu$$

<br>
<br>
<br>

### 3. 4 Radiation Pressure in an Enclosure Containing an Isotropic Radiation Field
<hr>

&ensp;Consider a reflecting enclousre containing an isotropic radiation field. Each photon transfer *twice* its normal component of momentum on reflection. Thus we have the relation
$$p_{\nu} = \frac{2}{c}{\intop}I_{\nu}\cos^{2}\theta\,\mathrm{d}\Omega$$

<br>

Now by isotropy, $I_{\nu} = J_{\nu}$. So
$$P = \frac{2}{c}{\intop}J_{\nu}\mathrm{d}\nu{\intop}\cos^{2}\theta\,\mathrm{d}\Omega$$
The angular integration yields
$$P = \frac{1}{3}u$$

<br>

&ensp;Therefore, the radiation pressure of an isotropic radiation field is $\frac{1}{3}$ times density.

<br>
<br>
<br>

### 3. 5 Constancy of Specific Intensity Along Rays in 'Free Space'
<hr>

&ensp;Consider any ray $L$ and any two points along the ray. Construct areas $\mathrm{d}A_1$ and $\mathrm{d}A_2$ normal to the ray at these points. We now make use of the fact that energy is conserved. Consider the energy carried by that set of rays passing through both $\mathrm{d}A_1$ and $\mathrm{d}A_2$.

<br>

![](https://velog.velcdn.com/images/dae_111/post/ef767b5a-7b99-4354-856a-78680b380b66/image.png)

<br>

This can be expressed in two ways:
$$\mathrm{d}E_1 = I_{{\nu}_1}\,\mathrm{d}A_1\,\mathrm{d}t\,\mathrm{d}{\Omega}_1\,\mathrm{d}{\nu}_1 = \mathrm{d}E_2 = I_{{\nu}_2}\,\mathrm{d}A_2\,\mathrm{d}t\,\mathrm{d}{\Omega}_2\,\mathrm{d}{\nu}_2$$
Here $\mathrm{d}{\Omega}_1$ is the solid angle subtended by $\mathrm{d}A_2$ at $\mathrm{d}A_1$ and so forth. Since $\mathrm{d}{\Omega}_1 = \mathrm{d}A_2/R^2$, $\mathrm{d}{\Omega}_2 = \mathrm{d}A_1/R^2$ and $\mathrm{d}{\nu}_1 = \mathrm{d}{\nu}_2$, we have 
$$I_{{\nu}_1} = I_{{\nu}_2}$$

<br>

&ensp;Thus the intensity is constant along a ray:
$$I_{\nu} = constant.$$
or
$$\frac{\mathrm{d}I_{\nu}}{\mathrm{d}s} = 0,$$
where $\mathrm{d}s$ is a differnetial element of length along the ray.

<br>
<br>
<br>

### 3. 6 Proof of the Inverse Law for a Uniformly Bright Sphere
<hr>

&ensp;To show that there is no conflict between the constancy of specific intensity and the inverse square law, let us calculate the flux at an arbitrary distance from a sphere of uniform brightness B(that is, all rays leaving the sphere have the same brightness). Such a sphere is clearly an isotropic source. At P, the specific intensity is B if the ray intersects the sphere and zero otherwise.

<br>

![](https://velog.velcdn.com/images/dae_111/post/a3e4a460-c3fc-4fb4-8691-45c33cb4eb81/image.png)

<br>

Then,
$$F = {\intop}I\,\cos\theta\,\mathrm{d}\Omega = B{\intop}^{2\pi}_0\mathrm{d}\Phi\,{\intop}^{\theta_c}_0\sin\theta\cos\theta\,\mathrm{d}\theta,$$
where $\theta_c = \sin^{-1}R/r$ is the angle at which a ray from P is tangent to the sphere. It follows that,
$$F = {\pi}B(\frac{R}{r})^2$$
or
$$F = {\pi}B(1-{\cos}^2\theta_c) = {\pi}B\sin^2\theta_c.$$
Thus the specific intensity is constant, but the solid angle subtended by the given object decreases in such a way that the inverse square law is recovered. A useful result is obtained by setting $r = R$:
$$F = {\pi}B$$
That is, the flux at a surface of uniform brightness $B$ is simply ${\pi}B$.

<br>
<br>
<br>

## 4. Radiative Transfer
<hr>

&ensp;If a ray passes through matter, energy may be added or subtracted from it by emission or absorption, and the specific intensity will not in general remain constant.

<br>
<br>
<br>

### 4. 1 Emission
<hr>

The spontaneous emission coefficient $j$ is defined as the energy emitted per unit time per unit solid angle and per unit volume.
$$\mathrm{d}E = {\intop}j\,\mathrm{d}V\,\mathrm{d}\Omega\,\mathrm{d}t$$
A monochromatic emission coefficien can be similarly defined so that
$$\mathrm{d}E = j_{\nu}\,\mathrm{d}V\,\mathrm{d}\Omega\,\mathrm{d}t\,\mathrm{d}\nu,$$
where $j_{\nu}$ has units of $erg{\,}cm^{-3}{\,}s^{-1}{\,}ster^{-1}{\,}Hz^{-1}$.

<br>

For an *isotropic* emitter, or for a distribution of randomly oriented emitters, we can write
$$j_{\nu} = \frac{1}{4\pi}P_{\nu},$$
where $P_{\nu}$ is the radiated power per unit volume per unit frequency. Sometimes the spontaneous emission is defined by the emissivity $\epsilon_{\nu}$, defined as the energy emitted spontaneously per unit frequency per unit time per unit mass with units of $erg{\,}gm^{-1}{\,}s^{-1}{\,}Hz^{-1}$. If the emission is isotropic, then
$$\mathrm{d}E = \epsilon_{\nu}\rho\mathrm{d}V{\,}\mathrm{d}t{\,}\mathrm{d}\nu{\,}\frac{\mathrm{d}\Omega}{4\pi}.$$
where $\rho$ is the mass density of the emitting medium. Comparing the above two expressions for $\mathrm{d}E$, we have the relation between $\epsilon_{\nu}$ and $j_{\nu}$:
$$j_{\nu} = \frac{\epsilon_{\nu}\rho}{4\pi},$$
holding for isotropic emission. In going a distance $\mathrm{d}s$, a beam of cross section $\mathrm{d}A$ travels through avolume $\mathrm{d}V = \mathrm{d}A{\,}\mathrm{d}s$. Thus the intensity added to the beam by spontaneous emission is:
$$\mathrm{d}I_{\nu} = j_{\nu}\mathrm{d}s.$$

<br>
<br>
<br>

### 4. 2 Absorption
<hr>

&ensp;We define the *absorption coefficient*, $\alpha_{\nu}(cm^{-1})$ by the following equation, representing the loss of intensity in a beam as it travels a distance $\mathrm{d}s$:
$$\mathrm{d}I_{\nu} = -{\alpha}I_{\nu}\mathrm{d}s$$
Consider absorbers, whose effective absorbing area, or *cross section* $\sigma_{\nu}(cm^2)$ and density $n$. The total absorbing area presented by absorbers equals $n\sigma_{\nu}\mathrm{d}A{\,}\mathrm{d}s$. The *energy* absorbed out of the beam is
$$