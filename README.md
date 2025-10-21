Netra-AI: An AI-Powered Screening Tool to Prevent Diabetic Blindness

1. The Problem: A Silent Epidemic in Rural India

Diabetic Retinopathy (DR) is a leading cause of preventable blindness among India's over 100 million diabetics. Early screening is critical, but the necessary equipment is expensive (over ₹12.5 Lakh) and concentrated in urban centers, leaving millions in rural areas unscreened and at risk of irreversible vision loss. Netra-AI aims to bridge this critical gap in public healthcare.

2. Our Solution: Accessible AI for Early Detection

Netra-AI is an ultra-affordable (< ₹42,000 target cost), portable, AI-powered screening tool designed for use in primary health clinics and remote health camps. It empowers community health workers to conduct on-the-spot retinal screenings without needing an internet connection or a specialist's presence.

Key Features

-Instant Analysis: Provides a binary "Disease Present / No Disease" classification in seconds.

-Offline First: All AI processing happens directly on the edge device, ensuring functionality in the most remote areas.

-High Accuracy: The model is highly reliable, ensuring very few sick patients are missed.

-Ultra-Low Cost: Designed with low-cost hardware (Raspberry Pi target) to enable scalable deployment.

-Simple Interface: Can be operated by minimally trained personnel.

3. The AI Model: A Two-Stage Training Strategy

To overcome the challenges of noisy and imbalanced medical data, we developed a robust training strategy.

Step A: Simplification

The initial complex 5-level grading task was simplified into a more stable binary classification problem: detecting the presence of DR versus its absence.

Step B: Two-Stage Transfer Learning


Foundation Training (Generalist Model): A powerful EfficientNetB0 model was first trained on the large, diverse APTOS 2019 dataset (3,600+ images). This built a strong "generalist" model capable of recognizing DR features from a wide variety of sources.

Demographic Specialization (Expert Model): The high-performing generalist model was then fine-tuned on the Indian-specific IDRiD dataset. This crucial step specializes the model's knowledge, enhancing its fairness and accuracy for the target Indian demographic.

4. Final Model Performance

The final specialized model was evaluated on the unseen APTOS validation set, achieving outstanding results for a medical screening tool.

<img width="640" height="194" alt="image" src="https://github.com/user-attachments/assets/c7bcc197-0a22-4741-bd20-ff284380f995" />

These metrics confirm that the model is both highly sensitive (low false negatives) and reliable (low false positives).

