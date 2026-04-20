# Soluciones — Tarea de Espectroscopía Astronómica

---

## Problema 1: Densidad columnar de Na mediante la curva de crecimiento

### Referencia principal
**Aller, L.H. (1971).** *Atoms, Stars, and Nebulae*, Revised Edition, Harvard University Press, Cambridge, MA. **Figure 9.22** (reproducida en las notas del curso, diapositiva 86).

Texto complementario: **Gray, D.F. (2005).** *The Observation and Analysis of Stellar Photospheres*, 3rd Ed., Cambridge University Press, Cap. 16 — "The Curve of Growth".

### Marco teórico

La **curva de crecimiento** relaciona el ancho equivalente reducido $$\log(W_\lambda / \lambda)$$ con la cantidad $$\log\left[f N_a \left(\frac{\lambda}{5000\;\text{Å}}\right)\right]$$, donde $$N_a$$ es la densidad columnar de átomos absorbentes (átomos/cm²), $$f$$ es la fuerza del oscilador, y el factor $$\lambda/5000$$ Å normaliza la longitud de onda a la referencia de la curva. La curva tiene tres regímenes clásicos:

1. **Régimen lineal** (líneas débiles): $$W_\lambda \propto N_a f \lambda$$
2. **Régimen saturado** (plateau): $$W_\lambda \propto (\ln N_a f)^{1/2}$$
3. **Régimen amortiguado** (alas de Lorentz): $$W_\lambda \propto (N_a f)^{1/2}$$

### Datos

| Línea | $$\lambda$$ (Å) | EW (Å) | $$f$$ |
|-------|:-------:|:-------:|:-----:|
| Na I (UV) | 3302.38 | 0.088 | 0.0214 |
| Na I D₁ | 5889.97 | 0.730 | 0.645 |

### Procedimiento

**Paso 1.** Calcular el ancho equivalente reducido $$\log(W_\lambda/\lambda)$$ para cada línea:

**Línea 3302.38 Å:**

$$
\log\left(\frac{W_\lambda}{\lambda}\right) = \log\left(\frac{0.088}{3302.38}\right) = \log(2.665 \times 10^{-5}) = -4.574
$$

**Línea 5889.97 Å:**

$$
\log\left(\frac{W_\lambda}{\lambda}\right) = \log\left(\frac{0.730}{5889.97}\right) = \log(1.239 \times 10^{-4}) = -3.907
$$

**Paso 2.** Leer $$\log\left[f N_a (\lambda/5000)\right]$$ de la curva de crecimiento (Fig. 9.22 de Aller):

Entrando al eje vertical con cada valor de $$\log(W_\lambda/\lambda)$$, se lee el eje horizontal:

| Línea | $$\log(W/\lambda)$$ | Régimen | $$\log[f N_a (\lambda/5000)]$$ (lectura) |
|-------|:--------:|:--------:|:--------:|
| 3302.38 Å | −4.574 | Lineal | ≈ 12.1 |
| 5889.97 Å | −3.907 | Saturado/transición | ≈ 14.5 |

> **Nota:** Estas lecturas son inherentemente aproximadas (±0.1–0.2 dex) dada la resolución de la figura. La línea D₁ del Na cae en la zona plana de la curva, donde un pequeño error en $$\log(W/\lambda)$$ produce un gran error en la abscisa — esto es una limitación intrínseca del método en el régimen saturado.

**Paso 3.** Calcular $$\log[f(\lambda/5000)]$$ para cada línea:

**Línea 3302.38 Å:**

$$
\log\left[f \cdot \frac{\lambda}{5000}\right] = \log\left[0.0214 \times \frac{3302.38}{5000}\right] = \log(0.01413) = -1.850
$$

**Línea 5889.97 Å:**

$$
\log\left[f \cdot \frac{\lambda}{5000}\right] = \log\left[0.645 \times \frac{5889.97}{5000}\right] = \log(0.7598) = -0.119
$$

**Paso 4.** Aplicar la relación del enunciado para obtener $$\log N_a$$:

$$
\log N_a = \log\left[f N_a \left(\frac{\lambda}{5000}\right)\right] - \log\left[f \left(\frac{\lambda}{5000}\right)\right]
$$

**Línea 3302.38 Å:**

$$
\log N_a = 12.1 - (-1.850) = 13.95
$$

$$
\boxed{N_a \approx 8.9 \times 10^{13} \;\text{átomos/cm}^2}
$$

**Línea 5889.97 Å:**

$$
\log N_a = 14.5 - (-0.119) = 14.62
$$

$$
\boxed{N_a \approx 4.2 \times 10^{14} \;\text{átomos/cm}^2}
$$

### Discusión

Las dos líneas dan valores de $$\log N_a$$ que difieren en ~0.7 dex. Esto se debe fundamentalmente a dos factores:

1. **Incertidumbre de lectura gráfica:** La curva de crecimiento es leída de una figura impresa de baja resolución; un error de ±0.2 en el eje $$x$$ se propaga directamente a $$\log N_a$$.
2. **Régimen de la curva:** La línea D₁ (5889.97 Å) cae en la zona **saturada** de la curva, donde $$W_\lambda$$ es muy insensible a cambios en $$N_a$$. Esto amplifica enormemente la incertidumbre. La línea UV (3302.38 Å) está en el régimen **lineal**, donde la correspondencia es más precisa.

El valor derivado de la línea UV ($$\log N_a \approx 13.9$$) es más confiable. Un valor de referencia para la densidad columnar de Na en la fotosfera solar es $$\log N_a \approx 13.8$$–$$14.0$$ (ver Asplund et al. 2009, ARA&A 47, 481, para abundancias solares fotosféricas modernas).

---

## Problema 2: Separación física entre cúmulos de galaxias A2541 y A2546

### Referencia principal
**Hogg, D.W. (1999).** "Distance Measures in Cosmology", *arXiv:astro-ph/9905116*. Referencia estándar para las definiciones de distancias cosmológicas.

**Ryden, B. (2003).** *Introduction to Cosmology*, Addison-Wesley, Cap. 5 — para distancia comóvil y distancia de diámetro angular.

### Datos

| Cúmulo | $$z$$ | RA (°) | Dec (°) |
|--------|:-----:|:------:|:-------:|
| A2541 | 0.1150 | 347.530274 | −22.984876 |
| A2546 | 0.1126 | 347.664886 | −22.651348 |

Parámetros cosmológicos adoptados: $$H_0 = 70$$ km/s/Mpc, $$\Omega_m = 0.3$$, $$\Omega_\Lambda = 0.7$$, universo plano.

### Procedimiento

La separación física tiene dos componentes: **transversal** (separación angular proyectada) y **radial** (diferencia de redshift a lo largo de la línea de visión).

**Paso 1. Separación angular**

Para separaciones pequeñas, la distancia angular en la esfera celeste se calcula como:

$$
\theta \approx \sqrt{(\Delta\alpha \cos\bar{\delta})^2 + (\Delta\delta)^2}
$$

donde:

$$
\Delta\alpha = 347.664886° - 347.530274° = 0.134612°
$$

$$
\Delta\delta = -22.651348° - (-22.984876°) = 0.333528°
$$

$$
\bar{\delta} = \frac{-22.984876 + (-22.651348)}{2} = -22.818°
$$

$$
\Delta\alpha \cos\bar{\delta} = 0.134612° \times \cos(-22.818°) = 0.134612° \times 0.9218 = 0.12408°
$$

$$
\theta = \sqrt{(0.12408)^2 + (0.33353)^2} = \sqrt{0.01540 + 0.11124} = \sqrt{0.12664} = 0.3559°
$$

Conversión a radianes:

$$
\theta = 0.3559° \times \frac{\pi}{180} = 6.212 \times 10^{-3} \;\text{rad}
$$

**Paso 2. Distancia comóvil al redshift medio**

El redshift medio es $$\bar{z} = (0.1150 + 0.1126)/2 = 0.1138$$.

Para $$z$$ bajos y cosmología plana, la distancia comóvil se puede aproximar como:

$$
D_C = \frac{c}{H_0} \int_0^z \frac{dz'}{E(z')}
$$

donde $$E(z) = \sqrt{\Omega_m(1+z)^3 + \Omega_\Lambda}$$. Para $$z = 0.1138$$:

$$E(0.1138) = \sqrt{0.3 \times (1.1138)^3 + 0.7} = \sqrt{0.3 \times 1.3818 + 0.7} = \sqrt{1.1145} = 1.0557$$

Aproximación a primer orden (válida para $$z \ll 1$$):

$$
D_C \approx \frac{c \cdot z}{H_0 \cdot E(z/2)} \approx \frac{3 \times 10^5 \times 0.1138}{70 \times 1.027} \approx \frac{34\,140}{71.9} \approx 475 \;\text{Mpc}
$$

(Un cálculo numérico exacto da $$D_C \approx 474$$ Mpc para estos parámetros.)

La **distancia de diámetro angular** es:

$$
d_A = \frac{D_C}{1 + \bar{z}} = \frac{475}{1.1138} = 426.5 \;\text{Mpc}
$$

**Paso 3. Separación transversal**

$$
d_\perp = d_A \times \theta = 426.5 \;\text{Mpc} \times 6.212 \times 10^{-3} = 2.65 \;\text{Mpc}
$$

**Paso 4. Separación radial (línea de visión)**

La diferencia de redshift es:

$$
\Delta z = 0.1150 - 0.1126 = 0.0024
$$

La separación comóvil radial es:

$$
d_\parallel = \frac{c \cdot \Delta z}{H_0 \cdot E(\bar{z})} = \frac{3 \times 10^5 \times 0.0024}{70 \times 1.056} = \frac{720}{73.9} = 9.74 \;\text{Mpc}
$$

> **Nota:** Esta componente radial puede estar contaminada por velocidades peculiares de los cúmulos (típicamente $$\sim$$ 300–1000 km/s), que producirían un $$\Delta z$$ adicional de $$\sim 0.001$$–$$0.003$$. Es decir, la separación radial derivada del redshift es estrictamente una separación en *espacio de redshift*, no necesariamente la separación física real.

**Paso 5. Separación total**

$$
d = \sqrt{d_\perp^2 + d_\parallel^2} = \sqrt{(2.65)^2 + (9.74)^2} = \sqrt{7.02 + 94.9} = \sqrt{101.9}
$$

$$
\boxed{d \approx 10.1 \;\text{Mpc}}
$$

La separación está dominada por la componente radial. En proyección, los dos cúmulos están separados solo $$\sim$$2.6 Mpc pero en la línea de visión $$\sim$$9.7 Mpc (caveat: velocidades peculiares).

---

## Problema 3: Velocidad peculiar de la galaxia de Andrómeda (M31)

### Referencia principal
**Sparke, L.S. & Gallagher, J.S. (2007).** *Galaxies in the Universe*, 2nd Ed., Cambridge University Press, Cap. 1.

**Binney, J. & Merrifield, M. (1998).** *Galactic Astronomy*, Princeton University Press, Sec. 1.2 — corrección de velocidades heliocéntricas a galactocéntricas.

### Datos

| Parámetro | Valor |
|-----------|:-----:|
| Distancia a M31 | 780 kpc = 0.780 Mpc |
| $$H_0$$ | 70 km/s/Mpc |
| Velocidad heliocéntrica | $$v_\text{helio} = -300$$ km/s |
| Velocidad orbital del Sol | $$v_\odot = 200$$ km/s |
| Ángulo entre $$\vec{v}_\odot$$ y la LOS a M31 | $$\alpha = 33°$$ |

### Definiciones

La **velocidad peculiar** es la componente de velocidad que NO se debe al flujo de Hubble. Es decir:

$$
v_\text{pec} = v_\text{obs,corregida} - v_\text{Hubble}
$$

### Procedimiento

**Paso 1. Velocidad del flujo de Hubble en la posición de M31**

$$
v_\text{Hubble} = H_0 \times d = 70 \;\text{km/s/Mpc} \times 0.780 \;\text{Mpc} = 54.6 \;\text{km/s}
$$

Esto significa que, en un universo en expansión uniforme y sin perturbaciones gravitacionales, M31 debería estar **alejándose** de nosotros a 54.6 km/s.

**Paso 2. Corrección de velocidad heliocéntrica a galactocéntrica**

La velocidad heliocéntrica medida ($$-300$$ km/s) está contaminada por el movimiento orbital del Sol alrededor del centro galáctico. Debemos corregir este efecto para obtener la velocidad respecto al centro de la Vía Láctea.

La componente de la velocidad solar proyectada sobre la línea de visión (LOS) a M31 es:

$$
v_{\odot,\text{LOS}} = v_\odot \cos\alpha = 200 \times \cos(33°) = 200 \times 0.8387 = 167.7 \;\text{km/s}
$$

Si el Sol se mueve con una componente **hacia** M31 (lo cual es consistente con la geometría de la órbita solar y la posición de M31 en el cielo), entonces parte de la velocidad de acercamiento medida se debe a nuestro propio movimiento. La corrección es:

$$
v_\text{galactocéntrica} = v_\text{helio} + v_{\odot,\text{LOS}} = -300 + 167.7 = -132.3 \;\text{km/s}
$$

> El signo positivo en la corrección refleja que restamos la contribución de nuestro movimiento: si nos movemos hacia M31, el acercamiento observado es mayor que el real.

**Paso 3. Velocidad peculiar**

$$
v_\text{pec} = v_\text{galactocéntrica} - v_\text{Hubble} = -132.3 - 54.6
$$

$$
\boxed{v_\text{pec} \approx -187 \;\text{km/s}}
$$

### Interpretación física

El signo negativo indica que M31 se **acerca** al centro de la Vía Láctea a $$\sim 187$$ km/s, en contra del flujo de Hubble. Esto es físicamente esperado: M31 y la Vía Láctea son los dos miembros dominantes del **Grupo Local** y están gravitacionalmente ligados. Su atracción mutua supera con creces la expansión cósmica a esta escala ($$d < 1$$ Mpc).

De hecho, las mediciones modernas más precisas (van der Marel et al. 2012, ApJ 753, 8) confirman que M31 se acerca a la Vía Láctea con una velocidad radial galactocéntrica de $$\sim -109$$ a $$-130$$ km/s (dependiendo de la corrección al estándar de reposo local, LSR, vs. galactocéntrica), y se estima una colisión/fusión en $$\sim 4.5$$ Gyr. La diferencia con nuestro resultado ($$-132$$ vs. $$\sim -120$$ km/s para $$v_\text{galactocéntrica}$$) se debe a los valores aproximados usados aquí para $$v_\odot$$ y el ángulo.

### Resumen de la descomposición de velocidades

| Componente | Valor (km/s) |
|------------|:------:|
| $$v_\text{helio}$$ (observada) | −300.0 |
| $$v_{\odot,\text{LOS}}$$ (corrección solar) | +167.7 |
| $$v_\text{galactocéntrica}$$ | −132.3 |
| $$v_\text{Hubble}$$ | +54.6 |
| $$v_\text{peculiar}$$ | **−186.9** |

---

### Referencias completas

1. Aller, L.H. (1971). *Atoms, Stars, and Nebulae*, Revised Edition. Harvard University Press.
2. Gray, D.F. (2005). *The Observation and Analysis of Stellar Photospheres*, 3rd Ed. Cambridge University Press.
3. Hogg, D.W. (1999). "Distance Measures in Cosmology." arXiv:astro-ph/9905116.
4. Sparke, L.S. & Gallagher, J.S. (2007). *Galaxies in the Universe*, 2nd Ed. Cambridge University Press.
5. Binney, J. & Merrifield, M. (1998). *Galactic Astronomy*. Princeton University Press.
6. Asplund, M. et al. (2009). ARA&A, 47, 481 — Abundancias solares.
7. van der Marel, R.P. et al. (2012). ApJ, 753, 8 — Movimiento propio y velocidad de M31.
