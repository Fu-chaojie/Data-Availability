# Real-Vehicle Experimental Data

This repository provides the real-vehicle experimental data used in Chapter 5 of the associated manuscript on robust guaranteed-cost path tracking control for steer-by-wire vehicles.

The data were collected from a dSPACE real-time control and data-acquisition platform during single-lane-change (SLC) and double-lane-change (DLC) experiments. The original experimental records are provided as MATLAB `.mat` files.

## Data Format

Each `.mat` file contains dSPACE-exported time-series data. In the original data structure, the key signals are stored in `filename.Y(i).Data`, where `filename` denotes the loaded data object.

The key signal correspondence is:

```matlab
ephi    = filename.Y(2).Data;   % heading error, rad
ey      = filename.Y(3).Data;   % lateral error, m
delta_f = filename.Y(7).Data;   % steering angle, raw unit from recorder
vx      = filename.Y(8).Data;   % longitudinal velocity, m/s
vy      = filename.Y(9).Data;   % lateral velocity, m/s
x       = filename.Y(10).Data;  % longitudinal/global x-position, m
y       = filename.Y(11).Data;  % lateral/global y-position, m
```

## MATLAB Loading Example

```matlab
data = load('example.mat');

% Replace "filename" with the actual variable name stored in the MAT file
ephi    = filename.Y(2).Data;
ey      = filename.Y(3).Data;
delta_f = filename.Y(7).Data;
vx      = filename.Y(8).Data;
vy      = filename.Y(9).Data;
x       = filename.Y(10).Data;
y       = filename.Y(11).Data;
```

## Experimental Data Index

The following `.mat` file IDs correspond to the real-vehicle experimental datasets reported in Chapter 5 of the manuscript.

| Manuscript case | MAT file IDs | Description |
|---|---:|---|
| DLC, 40 km/h | 17, 25, 33 | Three-controller experimental data |
| DLC, 25 km/h | 15, 24, 31 | Three-controller experimental data |
| SLC, 25 km/h | 8, 21, 27 | Three-controller experimental data |
| SLC, 40 km/h | 19, 22, 28 | Three-controller experimental data |
| SLC, 40 km/h | 13, 23 | Two-controller experimental data |

## Notes

- `ephi` is the heading error and is stored in radians.
- `ey` is the lateral tracking error and is stored in meters.
- `delta_f` is the front steering angle signal recorded by the dSPACE system. Its unit follows the raw recorder configuration and should be interpreted according to the original calibration setting.
- `vx` and `vy` are the longitudinal and lateral vehicle velocities, respectively.
- `x` and `y` are the recorded vehicle position signals used for trajectory analysis.

## Data Availability

The real-vehicle experimental data supporting the findings of the associated study are provided in MATLAB `.mat` format in this repository. Additional information about the experimental setup, signal definitions, or data processing can be requested from the corresponding author.

## Citation

If you use these data, please cite the associated manuscript.
