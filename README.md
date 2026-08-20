# Real-Vehicle Experimental Data

This repository provides real-vehicle experimental data on guaranteed-cost path tracking control for Steer-by-Wire Vehicles, Chapter 5 of the manuscript titled "Guaranteed-Cost Path Tracking Control for Steer-by-Wire Vehicles Considering Communication Delay and Actuator Dynamics". The data was collected from the dSPACE real-time control and data acquisition platform during single-lane change (SLC) and two-lane change (DLC) experiments. The original experimental records are provided as MATLAB `.mat` files.
## Data Format

Each `.mat` file contains dSPACE-exported time-series data. In the original data structure, the key signals are stored in `filename.Y(i).Data` and `filename.X.Data`.
## MATLAB Loading Example

```matlab
% Replace "filename" with the actual variable name stored in the MAT file

% For DADGC, LQR and DF Controller 
t       = filename.X.Data;
ephi    = filename.Y(2).Data;
ey      = filename.Y(3).Data;
delta_f = filename.Y(7).Data;
vx      = filename.Y(8).Data;
vy      = filename.Y(9).Data;
x       = filename.Y(10).Data;
y       = filename.Y(11).Data;
% For LPV-MPC Controller 
t       = filename.X(2).Data;
ephi    = filename.Y(23).Data;
ey      = filename.Y(25).Data;
delta_f = filename.Y(11).Data;
vx      = filename.Y(12).Data;
vy      = filename.Y(13).Data;
x       = filename.Y(14).Data;
y       = filename.Y(15).Data;
```
## Experimental Data Index
| Manoeuvre | Speed (km/h) | Controller | filename ID |
| --------- | --------: | ---------- | -----: |
| SLC       |           25 | DF         |     27 |
| SLC       |           40 | DF         |     28 |
| DLC       |           25 | DF         |     31 |
| DLC       |           40 | DF         |     33 |
| SLC       |           30 | DADGC      |    128 |
| SLC       |           30 | DADGC      |    129 |
| SLC       |           30 | DADGC      |    130 |
| SLC       |           30 | LQR        |    146 |
| SLC       |           30 | LQR        |    148 |
| SLC       |           30 | LQR        |    149 |
| SLC       |           30 | LPV-MPC    |    563 |
| SLC       |           30 | LPV-MPC    |    564 |
| SLC       |           40 | DADGC      |    140 |
| SLC       |           40 | DADGC      |    141 |
| SLC       |           40 | DADGC      |    142 |
| SLC       |           40 | LQR        |    150 |
| SLC       |           40 | LQR        |    151 |
| SLC       |           40 | LQR        |    152 |
| SLC       |           40 | LPV-MPC    |    567 |
| SLC       |           40 | LPV-MPC    |    580 |
| SLC       |           50 | DADGC      |    143 |
| SLC       |           50 | DADGC      |    144 |
| SLC       |           50 | DADGC      |    145 |
| SLC       |           50 | LQR        |    153 |
| SLC       |           50 | LQR        |    154 |
| SLC       |           50 | LQR        |    155 |
| SLC       |           50 | LPV-MPC    |    581 |
| SLC       |           50 | LPV-MPC    |    582 |
| DLC       |           30 | DADGC      |    131 |
| DLC       |           30 | DADGC      |    132 |
| DLC       |           30 | DADGC      |    133 |
| DLC       |           30 | LQR        |    158 |
| DLC       |           30 | LQR        |    159 |
| DLC       |           30 | LQR        |    160 |
| DLC       |           40 | DADGC      |    135 |
| DLC       |           40 | DADGC      |    136 |
| DLC       |           40 | DADGC      |    137 |
| DLC       |           40 | LQR        |    161 |
| DLC       |           40 | LQR        |    162 |
| DLC       |           40 | LQR        |    163 |
| DLC       |           40 | LPV-MPC    |    577 |
| DLC       |           40 | LPV-MPC    |    578 |
| DLC       |           50 | DADGC      |    079 |
| DLC       |           50 | DADGC      |    080 |
| DLC       |           50 | DADGC      |    082 |
| DLC       |           50 | LQR        |    062 |
| DLC       |           50 | LQR        |    064 |
| DLC       |           50 | LQR        |    076 |
| DLC       |           50 | LPV-MPC    |    334 |
| DLC       |           50 | LPV-MPC    |    335 |



## Notes

- `ephi` is the heading error and is stored in radians.
- `ey` is the lateral tracking error and is stored in meters.
- `delta_f` is the actual front wheel steering angle signal recorded by the dSPACE system.
- `vx` and `vy` are the longitudinal and lateral vehicle velocities, respectively.
- `x` and `y` are the recorded vehicle position signals used for trajectory analysis.

## Data Availability

The real-vehicle experimental data supporting the findings of the associated study are provided in MATLAB `.mat` format in this repository. Additional information about the experimental setup, signal definitions, or data processing can be requested from the corresponding author.

## Citation

If you use these data, please cite the associated manuscript.
