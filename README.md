# AI Security Project: Privacy-Preserving Machine Learning with Differential Privacy

## Overview

This project demonstrates the implementation and comparative analysis of differential privacy techniques in machine learning using TensorFlow Privacy. The notebook provides a hands-on exploration of the privacy-utility tradeoff in AI systems, comparing standard machine learning models against differentially private implementations.

## Project Objectives

- **Demonstrate Differential Privacy**: Implement mathematically rigorous privacy protections in machine learning
- **Quantify Privacy Costs**: Measure the performance impact of privacy-preserving techniques
- **Visualise Trade-offs**: Create comprehensive visualisations showing privacy vs. utility relationships
- **Educational Purpose**: Provide clear examples of privacy-preserving AI for educational and research use

## What's in the Notebook

### 🔧 Technical Implementation
- **Dataset**: MNIST handwritten digit classification (28x28 greyscale images)
- **Models**: Convolutional Neural Network architecture
- **Privacy Framework**: TensorFlow Privacy library with DP-SGD optimiser
- **Comparison**: Side-by-side training of standard vs. differentially private models

### 📊 Comprehensive Analysis
The notebook includes detailed analysis across multiple dimensions:

1. **Training Dynamics**
   - Learning curves comparison
   - Loss function behaviour
   - Convergence patterns under privacy constraints

2. **Performance Metrics**
   - Overall accuracy comparison
   - Per-class accuracy breakdown
   - Confusion matrix analysis

3. **Privacy Quantification**
   - Epsilon (ε) budget calculations
   - Privacy-utility trade-off curves
   - Impact of different noise multipliers

### 📈 Visualisations Generated

The notebook produces several key visualisations:
- **Training Metrics Comparison**: Side-by-side learning curves
- **Test Accuracy Bar Charts**: Direct performance comparison
- **Confusion Matrices**: Classification pattern analysis
- **Per-Class Accuracy**: Impact across different digit classes
- **Privacy-Utility Trade-off**: Curves showing accuracy vs. privacy budget
- **Prediction Confidence**: Uncertainty analysis between models

## Key Findings

From the implementation, you'll observe:

- **Standard Model**: ~98% accuracy (no privacy protection)
- **DP Model**: ~70% accuracy (with privacy guarantees)
- **Privacy Cost**: ~28% accuracy reduction for strong privacy protection
- **Heterogeneous Impact**: Some digits (like '1') less affected than complex digits (like '8')
- **Confidence Reduction**: DP models show appropriate uncertainty, preventing memorisation

## Technical Requirements

```python
# Required packages (automatically installed in notebook)
tensorflow==2.14.0
tensorflow-privacy==0.9.0
numpy
matplotlib
seaborn
scikit-learn
```

## How to Use

1. **Open in Google Colab**: Click the "Open in Colab" badge or copy the notebook URL
2. **Runtime Setup**: Use GPU runtime for faster training (Runtime → Change runtime type → GPU)
3. **Run All Cells**: Execute cells sequentially (Runtime → Run all)
4. **View Results**: Scroll through generated visualisations and analysis

## Code Structure

The notebook is organised into logical sections:

```
1. Environment Setup & Installation
2. Data Loading & Preprocessing
3. Model Architecture Definition
4. Standard Model Training
5. Differential Privacy Model Training
6. Performance Evaluation
7. Privacy Budget Calculation
8. Visualisation Generation
9. Comparative Analysis
```

## Understanding the Results

### Privacy-Utility Trade-off
The core insight from this project is the quantification of privacy costs:
- **Higher Privacy** (lower ε) → **Lower Accuracy**
- **Lower Privacy** (higher ε) → **Higher Accuracy**

### Practical Implications
- **Healthcare**: Patient data protection with slight diagnostic accuracy reduction
- **Finance**: Transaction privacy with moderate fraud detection impact
- **Mobile**: Keyboard prediction privacy without losing functionality

## Privacy Parameters Explained

- **Noise Multiplier**: Controls the amount of noise added (higher = more privacy)
- **L2 Norm Clip**: Gradient clipping threshold (prevents gradient explosion)
- **Epsilon (ε)**: Privacy budget (lower = stronger privacy guarantees)
- **Delta (δ)**: Probability of privacy breach (typically set to 1e-5)

## Educational Value

This notebook serves as:
- **Introduction to Differential Privacy**: Practical implementation with real results
- **Visualisation of Abstract Concepts**: Making privacy-utility trade-offs tangible
- **Benchmark Implementation**: Reference for differential privacy in deep learning
- **Research Foundation**: Starting point for advanced privacy-preserving ML research

## Real-World Applications

The techniques demonstrated here are used by:
- **Apple**: iOS keyboard predictions
- **Google**: Location data analysis
- **Microsoft**: Telemetry data collection
- **Healthcare Systems**: Patient data analysis
- **Financial Institutions**: Transaction pattern analysis

## Future Extensions

Potential improvements and extensions:
- Different datasets (CIFAR-10, medical imaging)
- Alternative privacy mechanisms (federated learning, homomorphic encryption)
- Advanced DP optimisers and techniques
- Privacy accounting with different composition methods

## Repository Structure

```
├── AI_Security_Project_Privacy_Preserving_AI_with_Differential_Privacy_with_visualizations.ipynb
├── README.md
└── outputs/
    ├── training_metrics_comparison.png
    ├── test_accuracy_comparison.png
    ├── confusion_matrices.png
    ├── per_class_accuracy.png
    ├── privacy_utility_tradeoff.png
    └── prediction_confidence.png
```

## Citation

If you use this work in research or educational contexts, please reference:

```bibtex
@misc{fatunla2024differential_privacy,
  title={Privacy-Preserving AI with Differential Privacy Visualisation},
  author={Abiola Fatunla},
  year={2025},
  url={https://github.com/AbiolaFatunla/Privacy_Preserving_AI_with_Differential_Privacy_AI_Security_Project},
  note={Implementation of TensorFlow Privacy on MNIST Classification}
}
```

## Licence

This project is available under the MIT Licence for educational and research purposes.

## Contact

For questions or collaboration opportunities:
- GitHub: [@AbiolaFatunla](https://github.com/AbiolaFatunla)
- Repository: [Privacy_Preserving_AI_with_Differential_Privacy_AI_Security_Project](https://github.com/AbiolaFatunla/Privacy_Preserving_AI_with_Differential_Privacy_AI_Security_Project)

---

**Note**: This notebook is designed for educational purposes. For production implementations of differential privacy, consider additional factors such as hyperparameter tuning, more sophisticated privacy accounting, and domain-specific considerations.

**Disclaimer**: The privacy guarantees demonstrated in this project are theoretical. Real-world implementations require careful consideration of additional attack vectors, composition theorems, and regulatory requirements.
