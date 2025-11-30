# VueNir: Emotion & Crisis Detection System

## Project Overview
Developed an advanced mental health monitoring system that simultaneously detects 28 distinct emotions and identifies critical suicide-risk indicators using fine-tuned BERT architecture. The system provides real-time emotional analysis with prioritized crisis detection for mental health applications.

## Technical Implementation

### Model Architecture
- **Base Model**: BERT-base fine-tuned for emotional analysis
- **Dual-Head Design**: 
  - 28-class emotion classification head
  - Binary crisis detection head
- **Multi-Task Learning**: Simultaneous emotion and risk prediction

### Data Pipeline & Preprocessing
- **Multi-Source Integration**: Combined GoEmotions dataset with specialized mental health data
- **Class Balancing**: Addressed severe data imbalance in crisis labels
- **Data Augmentation**: Enhanced training diversity while maintaining label integrity

## Performance Optimization

### Technical Improvements
- **Custom Weighted Loss Function**: Prioritized crisis detection accuracy
- **Precision-Recall Optimization**: Balanced detection sensitivity and specificity
- **Performance Gain**: Achieved 10% overall improvement in model performance

### Key Metrics
- **Emotion Classification**: 28-category granular emotional analysis
- **Crisis Detection**: High-precision risk flagging system
- **Real-time Processing**: Optimized for deployment in mental health platforms

## Technical Challenges & Solutions

### Data Imbalance
- **Challenge**: Severe class imbalance in crisis indicators
- **Solution**: Custom sampling strategies and weighted loss functions
- **Result**: Maintained high recall for rare but critical crisis cases

### Multi-Objective Optimization
- **Challenge**: Balancing emotion classification with crisis detection priorities
- **Solution**: Dual-head architecture with task-specific optimization
- **Result**: Simultaneous high performance on both tasks

## Impact & Applications

### Mental Health Monitoring
- **Early Intervention**: Proactive crisis detection capabilities
- **Comprehensive Analysis**: Detailed emotional state assessment
- **Clinical Support**: Decision support tool for mental health professionals

### Technical Innovation
- **Novel Architecture**: dual-head BERT implementation for combined emotion/crisis detection
- **Performance Benchmark**: State-of-the-art results on mental health text classification
- **Deployment Ready**: Optimized for real-world mental health applications

## Technologies Used
- **ML Framework**: PyTorch, Transformers
- **Model Architecture**: BERT, Custom Classification Heads
- **Data Processing**: Pandas, NumPy, Scikit-learn
- **Optimization**: Custom loss functions, class weighting strategies

---

**Project Type**: Internship Project
