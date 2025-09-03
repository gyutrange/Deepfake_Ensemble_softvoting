# Deepfake Soft-Voting Ensemble

This repository presents a simple yet effective experiment: by applying soft voting (weighted averaging) across models that capture different perspectives — frequency, spatial context, and spectral features — we achieved AUC 1.0000 / Accuracy 0.9667 / F1 0.9789 / FP=0 on the competition’s Final Test Set.

https://gyutrange.github.io/Deepfake-Ensemble/

✨ Highlights

Idea: Soft voting with

FreqNet (frequency-domain artifacts)

GenConViT (global/spatial context via vision transformer)

CaFft (FFT-based spectral cues)

Final Test Results:

AUC: 1.0000

Accuracy: 0.9667

F1: 0.9789

Confusion (threshold=0.5): TP=93, TN=23, FP=0, FN=4

Fake detection accuracy = 0.9588 / Real detection accuracy = 1.0000

Learned Weights: ~0.96 allocated to GenConViT, with the rest acting as minor correction factors.

Operational benefit: FP=0 ensures no real videos are mistakenly flagged, reducing manual review and policy costs.

Validation Consistency: On an internal set of 399 samples, we observed Precision=1.0000, FP=0, with Recall at 0.9286.

### Reference
https://github.com/chuangchuangtan/FreqNet-DeepfakeDetection
https://github.com/erprogs/GenConViT
