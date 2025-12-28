# Mathematical Model of Vibration Isolation for Thresher-Class Rafting System

## Introduction

The primary noise-reduction technology employed in the Thresher-class submarines is the machinery rafting system, which decouples major vibration sources (pumps, turbines, reduction gears) from the pressure hull. This document presents the fundamental mathematical model used to quantify the vibration isolation performance of the raft.

## Lumped-Parameter Model

The rafting system is modeled as a **single-degree-of-freedom (SDOF) mass-spring-damper system** in the vertical direction, with the following elements:

- **Mass (m):** The total effective mass of the machinery assembly mounted on the raft, including the raft structure itself. For the Thresher class, this mass is on the order of 40–60 metric tons.
- **Spring (k):** The effective stiffness of the elastomeric mounts that support the raft. These mounts are designed to have a low stiffness to achieve a low natural frequency, typically below 10 Hz.
- **Damper (c):** The viscous damping coefficient representing energy dissipation in the mounts and any supplemental dampers.

The equation of motion for the raft displacement \( x(t) \) relative to the hull under a harmonic force excitation \( F(t) = F_0 \cos(\omega t) \) is:

\[
m \ddot{x} + c \dot{x} + k x = F_0 \cos(\omega t)
\]

## Transfer Function and Isolation Performance

The steady‑state response amplitude \( X \) is obtained from the complex transfer function:

\[
H(\omega) = \frac{X}{F_0} = \frac{1}{k - m\omega^2 + i c \omega}
\]

The magnitude of the transfer function (compliance) is:

\[
|H(\omega)| = \frac{1}{\sqrt{(k - m\omega^2)^2 + (c\omega)^2}}
\]

The **isolation effectiveness** is conventionally expressed as the *transmissibility* \( T \), defined as the ratio of the force transmitted to the hull to the exciting force:

\[
T(\omega) = \frac{F_{\text{transmitted}}}{F_0} = \sqrt{\frac{1 + (2\zeta r)^2}{(1 - r^2)^2 + (2\zeta r)^2}}
\]

where:
- \( r = \omega / \omega_n \) is the frequency ratio,
- \( \omega_n = \sqrt{k/m} \) is the undamped natural frequency,
- \( \zeta = c / (2\sqrt{mk}) \) is the damping ratio.

## Design Criteria and Parameter Selection

For effective isolation, the system must operate in the **isolation region** where \( r > \sqrt{2} \). In this region, \( T < 1 \) and the force transmitted to the hull is attenuated. The Thresher‑class design targets:

- Natural frequency \( f_n = \omega_n / 2\pi \approx 6–8\ \text{Hz} \).
- Damping ratio \( \zeta \approx 0.1–0.15 \) (lightly damped to avoid excessive response at resonance while maintaining good high‑frequency isolation).
- Isolation starting frequency ≈ 10–12 Hz, providing > 20 dB attenuation above 20 Hz.

## Physical Significance of Model Parameters

1. **Mass (m):** A larger raft mass lowers the natural frequency for a given spring stiffness, shifting the isolation region to lower frequencies. It also reduces the static deflection under weight.

2. **Spring (k):** The mount stiffness directly sets the natural frequency. Soft mounts (low k) are essential for low‑frequency isolation but must be compatible with static load capacity and stability requirements.

3. **Damper (c):** Damping controls the amplification at resonance. Excessive damping degrades isolation at higher frequencies, while insufficient damping leads to large resonant peaks that could damage equipment during start‑up or transient events.

## Multi‑Axis Considerations

Although the above model is one‑dimensional, the actual raft is a three‑dimensional system with coupled pitch, roll, and heave modes. The full 6‑DOF model uses a mass matrix \( \mathbf{M} \), a stiffness matrix \( \mathbf{K} \), and a damping matrix \( \mathbf{C} \). The equations of motion become:

\[
\mathbf{M} \ddot{\mathbf{x}} + \mathbf{C} \dot{\mathbf{x}} + \mathbf{K} \mathbf{x} = \mathbf{F}(t)
\]

The eigenvalues of \( \mathbf{M}^{-1}\mathbf{K} \) give the six natural frequencies, and the corresponding eigenvectors describe the mode shapes. The Thresher raft was tuned to avoid coincidence with the dominant forcing frequencies of the main machinery (typically 30–100 Hz for turbines and reduction gears).

## Conclusion

This lumped‑parameter model, extended to multi‑axis dynamics, formed the analytical foundation for the Thresher‑class rafting system. By carefully selecting mass, stiffness, and damping parameters, the design achieved a dramatic reduction in structure‑borne noise, making the Thresher one of the quietest submarines of its era. The same principles continue to inform modern submarine quieting technologies.

---

*Document prepared by the original design team as part of the Thresher‑class technical archive.*