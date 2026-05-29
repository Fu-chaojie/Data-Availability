# Real-Vehicle Experimental Data

This repository provides real-vehicle experimental data on robust guaranteed-cost path tracking control for Steer-by-Wire Vehicles, Chapter 5 of the manuscript titled "Robust Guaranteed-Cost Path Tracking Control for Steer-by-Wire Vehicles Considering Communication Delay and Actuator Dynamics". The data was collected from the dSPACE real-time control and data acquisition platform during single-lane change (SLC) and two-lane change (DLC) experiments. The original experimental records are provided as MATLAB `.mat` files.
## Data Format

Each `.mat` file contains dSPACE-exported time-series data. In the original data structure, the key signals are stored in `filename.Y(i).Data` and `filename.X.Data`.
## MATLAB Loading Example

```matlab
data = load('rec1_017.mat');

% Replace "filename" with the actual variable name stored in the MAT file
t       = rec1_017.X.Data;
ephi    = rec1_017.Y(2).Data;
ey      = rec1_017.Y(3).Data;
delta_f = rec1_017.Y(7).Data;
vx      = rec1_017.Y(8).Data;
vy      = rec1_017.Y(9).Data;
x       = rec1_017.Y(10).Data;
y       = rec1_017.Y(11).Data;
```

## Experimental Data Index

The following `.mat` file IDs correspond to the real-vehicle experimental datasets reported in Chapter 5 of the manuscript.

| Manuscript case | MAT file IDs | Description |
|---|---:|---|
| DLC, 40 km/h | 17, 25, 33 | DADGC, LQR and Baseline experimental data |
| DLC, 25 km/h | 15, 24, 31 | DADGC, LQR and Baseline experimental data |
| SLC, 25 km/h | 8, 21, 27 | DADGC, LQR and Baseline experimental data |
| SLC, 40 km/h | 19, 22, 28 | DADGC, LQR and Baseline experimental data |
| SLC, 40 km/h | 13, 23 | DADGC and LQR controller experimental data |

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
