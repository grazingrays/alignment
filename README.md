# Alignment

This repository is for discussion and recommendations for sample alignment.

Routines for sample alignment typically use:
- the fraction of transmitted direct beam while scanning different motors,
- the position of the specular reflection, or
- a combination thereof.

## Literature

[literature.md (WIP)](literature.md) contains quotes of publications
discussing GISAS sample alignment.

## Example: Alignment @MOUSE

As a spark for discussion we used the MOUSE alignment routine which,
in its current form, uses the transmission:

![MOUSE alignment routine](https://github.com/grazingrays/alignment/blob/assets/alignment_mouse.png)

![Fitted scans of the incident angle, with illustration of the relative height of the beam w.r.t. the sample surface.](https://github.com/grazingrays/alignment/blob/assets/incident_angle_scan_height.png)

Function to fit the incident angle scan:
$$T(\theta', \theta_0, l_{\mathrm{sample}}, y_{\mathrm{beam}}, \sigma_{\mathrm{beam}}) = 1 - \frac{1}{2}\mathrm{erf}\left[\dfrac{\dfrac{l_\mathrm{sample}}{2}
\cdot |\sin(\theta' - \theta_0)| - {y_{\mathrm{beam}}}}{\sigma_{\mathrm{beam}}}\right]$$
