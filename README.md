# Data-Availability
# Real-Vehicle Experimental Data for Steer-by-Wire Path Tracking

This repository provides the real-vehicle experimental data used in the manuscript:

**Robust Guaranteed-Cost Path Tracking Control for Steer-by-Wire Vehicles Considering Communication Delay and Actuator Dynamics**

## Data Description

The dataset contains real-vehicle path-tracking experimental data collected from a steer-by-wire pickup vehicle using a dSPACE real-time control and data-acquisition platform. The experiments include single-lane-change (SLC) and double-lane-change (DLC) maneuvers under different nominal vehicle speeds and controller configurations.

The data were recorded during real-vehicle tests and exported as MATLAB `.mat` files from the dSPACE/ControlDesk environment.

## Data Format

All data files are provided in MATLAB `.mat` format and can be loaded using:
data = load('filename.mat');
