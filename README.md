# Deepfake Soft-Voting Ensemble

FreqNet × GenConViT × CaFft ( + optional legacy detectors)

간단한 소프트 보팅(가중 평균) 만으로도 대회 Final Test에서 AUC 1.0000 / Acc 0.9667 / F1 0.9789 / FP=0 를 달성한 실험 레포입니다.
핵심 아이디어는 서로 다른 관점(주파수·공간·스펙트럼)을 갖는 모델을 확률 가중 평균으로 섞는 것입니다.

✨ Highlights

아이디어: FreqNet(주파수) · GenConViT(전역 문맥/공간 패턴) · CaFft(FFT 기반 스펙트럼) 소프트 보팅

최종 성능 (Final Test Set)

AUC: 1.0000

Accuracy: 0.9667

F1: 0.9789

Confusion (th=0.5): TP=93, TN=23, FP=0, FN=4

Fake acc=0.9588 / Real acc=1.0000

가중치 학습 결과(예시): GenConViT에 ~0.96이 몰리고, 나머지는 미세 보정 역할로 수렴

운영 친화: 오탐(FP) 0 유지 → 사람 리뷰/정책 비용 절감

참고: 내부 검증(399 샘플)에서도 Precision=1.0000 / FP=0로 일관된 패턴을 보였습니다(Recall=0.9286).

### Reference
https://github.com/chuangchuangtan/FreqNet-DeepfakeDetection
https://github.com/erprogs/GenConViT
