# Experiment 6 — RNN LSTM GRU and Video Understanding

## CS3807 — Deep Learning Laboratory

### Objective
Study Vanilla RNN LSTM and GRU for sequence learning and compare their performance on temporal data. The experiment also covers BPTT video understanding using CNN with recurrent models and sequence to sequence learning.

### Datasets
UCI Human Activity Recognition Using Smartphones Dataset  
Input shape: `128 × 9`  
Training: `7352` sequences  
Testing: `2947` sequences  
Classes: `6`

UCF101 Video Dataset  
Selected classes: `Basketball` `Biking` `CricketBowling` `TennisSwing` `WalkingWithDog`  
Videos: `25` per class  
Total videos: `125`  
Frames per video: `10`  
Frame size: `224 × 224 × 3`

### Models
- Vanilla RNN
- LSTM
- GRU
- CNN LSTM for video understanding
- CNN GRU for video understanding
- Encoder Decoder LSTM for sequence to sequence learning

### Main Results

| Model | Accuracy | Macro Precision | Macro Recall | Macro F1 | Parameters | Training Time |
|---|---:|---:|---:|---:|---:|---:|
| Simple RNN | 82.08% | 82.52% | 82.17% | 82.10% | 1,974 | 73.65 s |
| LSTM | 90.19% | 90.28% | 90.44% | 90.30% | 6,006 | 42.83 s |
| GRU | 89.79% | 89.71% | 89.95% | 89.81% | 4,758 | 31.44 s |

### Sequence Length Results

| Sequence Length | RNN F1 | LSTM F1 | GRU F1 |
|---:|---:|---:|---:|
| 32 | 84.21% | 88.43% | 89.20% |
| 64 | 78.48% | 88.72% | 90.44% |
| 128 | 74.86% | 89.07% | 90.68% |

### Video Results

MobileNetV2 feature dimension: `1280`  
Recurrent input shape: `125 × 10 × 1280`  
Train / Validation / Test: `87 / 19 / 19`

| Model | Accuracy | Macro F1 | Parameters | Training Time |
|---|---:|---:|---:|---:|
| CNN LSTM | 94.74% | 94.29% | 168,229 | 4.76 s |
| CNN GRU | 100.00% | 100.00% | 126,309 | 6.23 s |

### Sequence to Sequence Results

Input sequence length: `4`  
Output sequence length: `3`  
Training sequences: `4800`

```text
Token Accuracy = 100.00%
Sequence Accuracy = 100.00%
Training Loss = 0.0005
Validation Loss = 0.0006
