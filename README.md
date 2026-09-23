# PMSM Flux Guides and Rotor Surfacing

Research materials for the study **Codesign of Contour-Conformal Flux Guides and Three-Arc Rotor Surfacing for Permanent Magnet Synchronous Machines**.

The project investigates how rotor air-gap contouring and internal flux guidance interact in an interior permanent-magnet synchronous machine (IPMSM). The work combines electromagnetic finite-element analysis with structural, thermal, prototype, and vibration results.

## Study at a glance

- 30 kW-class traction IPMSM
- 8-pole, 48-slot machine
- Five compared rotor designs, labelled A-E
- Three-arc rotor-surface geometry
- Contour-conformal internal flux guides
- Electromagnetic torque, torque ripple, cogging torque, inductance, and efficiency analysis
- Structural stress and deformation checks up to 12 krpm
- Rotor thermal-boundary estimation and thermal field results
- Prototype laminations, wound stator, and experimental results

The supplementary material reports the structural operating points as 72 N m at 4000 rpm, 39.21 N m at 12000 rpm, 180 N m at 4000 rpm, and 46.21 N m at 12000 rpm. The reported governing structural result is 108.78 MPa maximum stress and 0.0295 mm maximum deformation at 12 krpm.

## Repository contents

| Path | Description |
| --- | --- |
| `TIE_LaTeX_template_v2 - Copy/` | Main manuscript source, IEEE journal classes, bibliography, and manuscript figures |
| `supplymentry/` | Supplementary-material source, compiled PDF, and supporting figures |
| `AUDIT_ACTIONS.md` | Pre-submission audit and list of issues requiring resolution |
| `Claude outputs/` | Referee reports and review artifacts |
| `Sample_papers/` | Reference papers collected during the literature review |

The repository is primarily a document and research-results archive. It does not currently contain the finite-element project files, raw measurement files, simulation scripts, CAD source, or a turnkey numerical reproduction pipeline.

## Building the documents

Install a LaTeX distribution such as TeX Live or MiKTeX, together with `latexmk` and the packages required by IEEEtran and the manuscript sources.

### Supplementary material

From `supplymentry/`, run:

```text
latexmk -pdf Journal.tex
```

The supplementary source expects its figures to be available in the same directory. The compiled document is `supplymentry/Journal.pdf`.

### Main manuscript

From `TIE_LaTeX_template_v2 - Copy/`, run:

```text
latexmk -pdf TEC_main.tex
```

Depending on the local TeX installation, the bibliography may need to be built with BibTeX as part of the `latexmk` run. The bibliography files are in `TIE_LaTeX_template_v2 - Copy/Bibliography/`.

## Interpreting the results

The manuscript uses finite-element results to compare rotor geometries and to assess electromagnetic, mechanical, and thermal behaviour. The supplementary material contains:

- structural stress maps at four torque-speed operating points;
- material properties and the rotor convective film-coefficient derivation;
- prototype lamination and wound-stator photographs;
- flux-guide parameter sweeps;
- inductance and load-angle results; and
- rated-point thermal maps with and without rotor ducts.

These files document the current research and revision state. They should not be treated as a validated software release or as a complete reproduction package.

## Validation status

The current manuscript package is under technical revision. `AUDIT_ACTIONS.md` and `Claude outputs/REFEREE_REPORT.md` identify unresolved issues involving power and frequency consistency, rotor geometry equations, thermal predictions, figure and label references, torque-ripple validation, and demagnetisation limits.

Before using numerical values from the manuscript for design decisions or citing them as final experimental results, consult those audit documents and verify the corrected source data.

## Citation

If you use these materials, cite the associated manuscript when its publication details are available:

> O. J. Singh, B. Sah, and P. Kumar, “Codesign of Contour-Conformal Flux Guides and Three-Arc Rotor Surfacing for Permanent Magnet Synchronous Machines.”

## License

No license has been specified for this repository. Contact the authors before redistributing the manuscript, figures, or supplementary materials.
