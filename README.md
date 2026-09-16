# DATASET

Manuscript: Pore-Scale Effect of Dissolution on Residual Oil Saturation in Carbonate Rock under Three Wettability Conditions. Submitted to Applied Sciences (MDPI).

This workbook contains the numerical data underlying every figure and table of the manuscript.

## SHEETS

* **Table1_Core_samples** — Four carbonate cores: injection rate, porosity and permeability before and after treatment, acid pore volumes to breakthrough, dissolution regime.
* **Table2_Pore_networks** — Pore network properties of the eight subvolumes in both states.
* **Table3_Critical_points** — Initial water saturation, residual oil saturation and water relative permeability at residual oil saturation, for three wettability scenarios.
* **Fig2_Pore_radii** — Radius of every pore in every network, 260,040 rows. Source of Figure 2 and of the percentiles in Fig3_Percentiles.
* **Fig3_Percentiles** — 25th, 50th and 75th percentiles of the pore radius distribution.
* **Fig5_Relative_permeability** — Water saturation, capillary pressure and both relative permeabilities along all 48 simulated curves.
* **Fig6_Delta_Sor** — Change in residual oil saturation after dissolution, three scenarios.
* **Statistics** — Means, standard deviations and test results quoted in the text.

Figure 4 of the manuscript is plotted from Table2_Pore_networks. Table 2 and Table 3 of the manuscript correspond to the sheets of the same name.

## SUBVOLUME LABELS

The letter is the core sample, the digit the subvolume within it. Core A was treated at 12 mL/min, B at 16, C at 25 and D at 32. Two subvolumes were extracted from each core at identical coordinates in the scans taken before and after dissolution, which is why a subvolume is its own control.

## UNITS

Pore and throat radii, micrometres. Permeability, millidarcy. Capillary pressure, kilopascal. Porosity, saturation and relative permeability are fractions. Coordination number, tortuosity and formation factor are dimensionless. Contact angles in degrees.

## PERMEABILITY SCALE CORRECTION

The networks were passed to pnflow with lengths in millimetres, which the program read as metres. A factor of 1000 in length gives a factor of 10^6 in permeability, so the value written in the log is divided by 10^6. Both the raw and the corrected value are given in Table2_Pore_networks. The corrected values are the ones quoted in the manuscript.

## FORMATION FACTOR

The formation factor in Table2_Pore_networks was reconstructed from tortuosity and network porosity as FF = tau^2 / phi. Replace it with the Formation factor line of the pnflow .prt output before publication if the logs are available.

## SOFTWARE

Networks extracted with pnextract, two-phase flow simulated with pnflow. Residual oil saturation is taken as 1 minus the water saturation at the last point of each imbibition curve.

Cells containing formulas recalculate from the values above them. Test statistics were computed in Python (scipy.stats) and are entered as numbers; the sheet says which test produced each one.
