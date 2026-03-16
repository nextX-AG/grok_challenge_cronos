# AQEA Zero-Shot Anomaly Detection Benchmark

> **AQEA CRONOS Analytics** is built on pure mathematics - no neural networks, no machine learning.
>
> Part of the **AQEA Engine**, a unified mathematical physics framework where signal processing, anomaly detection, and pattern recognition emerge from the same underlying physical principles.

Benchmark results across three diverse domains - **without any domain-specific training**.

## Results Summary

| Dataset | Domain | Metric | Result |
|---------|--------|--------|--------|
| **CWRU Bearing** | Industrial | Accuracy | **92.2%** |
| **CWRU Bearing** | Industrial | F1 Score | **95.9%** |
| **CWRU Bearing** | Industrial | Recall | **98.3%** |
| **UCI HAR** | Human Activity | Accuracy | **95.4%** |
| **UCI HAR** | Human Activity | LAYING Detection | **99.8%** |
| **ALFA UAV** | Robotics | Sensitivity | **100%** |
| **ALFA UAV** | Robotics | Fault Detection | **14/14** |

## Performance

| Dataset | Samples | Processing Time | Throughput |
|---------|---------|-----------------|------------|
| **CWRU Bearing** | 2,028 windows | **89 ms** | 22,787 windows/sec |
| **UCI HAR** | 7,352 samples | **12 ms** | 612,667 samples/sec |
| **ALFA UAV** | 27 flights (22k vectors) | **675 ms** | 40 flights/sec |

### Hardware Requirements

| Resource | Used | Notes |
|----------|------|-------|
| **RAM** | **< 100 MB** | Peak memory ~97 MB |
| **GPU** | **None** | Pure CPU computation |
| **Cores** | **1** | Single-threaded execution |
| **Architecture** | Any | Runs on x86, ARM, embedded |

No GPU acceleration. No CUDA. No TensorFlow. No PyTorch.

Pure mathematical operations that run on any CPU - from Raspberry Pi to data center.

## Datasets

### CWRU Bearing Fault Dataset
- **Source**: Case Western Reserve University Bearing Data Center
- **URL**: https://engineering.case.edu/bearingdatacenter
- **Description**: Vibration signals from bearings with seeded faults (inner race, outer race, ball)
- **Sensors**: Accelerometer at 12kHz/48kHz
- **Classes**: Normal, Inner Race Fault, Outer Race Fault, Ball Fault

### UCI Human Activity Recognition
- **Source**: UCI Machine Learning Repository
- **URL**: https://archive.ics.uci.edu/dataset/240/human+activity+recognition+using+smartphones
- **Description**: Smartphone IMU data from 30 subjects performing daily activities
- **Sensors**: Accelerometer + Gyroscope at 50Hz
- **Classes**: WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING

### ALFA UAV Fault Detection
- **Source**: CMU AirLab
- **URL**: https://theairlab.org/alfa-dataset/
- **Paper**: "ALFA: A Dataset for UAV Fault and Anomaly Detection"
- **Description**: Real drone flight recordings with injected motor faults
- **Sensors**: IMU (accelerometer + gyroscope) at 10Hz
- **Classes**: Normal Flight, Motor Fault

## Method

Pure mathematics. No machine learning.

**Key properties:**
- **Zero-shot**: No training on target domain
- **Universal**: Same algorithm for brain, motors, and robots
- **Real-time**: Sub-second inference, embedded-ready
- **Deterministic**: No randomness, fully reproducible

## Files

- `cwru_cronos_results.json` - CWRU bearing fault detection results
- `uci_har_cronos_results.json` - UCI human activity recognition results
- `alfa_cronos_results.json` - ALFA UAV fault detection results

## Citation

If you use these results, please cite the original datasets:

```
@misc{cwru_bearing,
  title={Case Western Reserve University Bearing Data Center},
  url={https://engineering.case.edu/bearingdatacenter}
}

@misc{uci_har,
  title={Human Activity Recognition Using Smartphones},
  author={Anguita, D. and Ghio, A. and Oneto, L. and Parra, X. and Reyes-Ortiz, J.L.},
  year={2013},
  publisher={UCI Machine Learning Repository}
}

@inproceedings{alfa_dataset,
  title={ALFA: A Dataset for UAV Fault and Anomaly Detection},
  author={Keipour, Azarakhsh and Mousaei, Mohammadreza and Scherer, Sebastian},
  booktitle={IEEE International Conference on Robotics and Automation (ICRA)},
  year={2020}
}
```

## License

Benchmark results: MIT License
Original datasets: See respective sources for licensing
