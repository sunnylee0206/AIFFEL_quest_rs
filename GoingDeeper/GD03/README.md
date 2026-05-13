# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 이희선
- 리뷰어 : 송세미


# PRT(Peer Review Template)
- [X]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - KITTI 데이터셋 로드부터 U-Net 및 U-Net++ 모델 구현, 그리고 두 모델의 성능 비교(mIoU)까지 프로젝트에서 요구하는 전 과정이 포함되어 있습니다. base_channels 8, 16, 32 세 가지 설정에 대한 학습 결과(Loss/IoU 그래프)가 명확히 시각화되어 있어 최종 결과물을 한눈에 확인할 수 있었습니다.
    
- [X]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 네 잘 이해되었습니다. UNetPlusPlus 클래스 내부에서 Nested Skip Connection 구조를 구현할 때, j=1부터 j=4까지 각 Dense Node가 어떻게 연결되는지 수식(x^{i,j})과 함께 주석을 달아주셔서 복잡한 아키텍처임에도 흐름을 쉽게 파악할 수 있었습니다.
        <img width="495" height="784" alt="image" src="https://github.com/user-attachments/assets/cecb8141-635c-4b6e-91ad-24857468f58e" />

- [X]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**
    - 단순히 모델 구조만 비교한 것이 아니라, Base Channels를 변수로 설정한 Ablation Study를 수행했습니다. 모델의 capacity가 성능(IoU)에 미치는 영향을 확인하기 위해 파라미터 수를 69만 개(ch=8)부터 1,100만 개(ch=32)까지 가변적으로 설정하며 실험한 점이 논리적인 접근이었다고 생각합니다. 
        
- [X]  **4. 회고를 잘 작성했나요?**
    - 실험 결과 분석 부분에서 정량적 분석(IoU Bar Chart)과 정성적 분석(Overlay 비교)을 병행하여 작성되었습니다. 채널 수가 너무 적으면 표현력이 부족하여 IoU가 낮아진다는 가설을 실험 결과로 입증하고, 파라미터 수 대비 효율성을 분석한 회고 내용이 잘 작성되었습니다. 데이터가 충분히 많은 환경이었더라면 또는 epoch을 더 늘려 실험했더라면 ch=32와 U-Net 사이의 차이가 더 벌어졌을 수도 있을것 같다라는 회고와 함께 나아가서 추가 실험 아이디어까지 잘 작성되었습니다.
      <img width="1341" height="478" alt="image" src="https://github.com/user-attachments/assets/9d34b285-dc13-469e-b277-b2ba4abae94d" />

        
- [X]  **5. 코드가 간결하고 효율적인가요?**
    - DoubleConv, KittiDataset 등 반복되는 로직을 모듈화하여 코드의 가독성을 높였습니다. 세 가지 채널 설정에 대해 실험을 진행할 때 run_experiment 함수를 만들어 자동화한 부분이 매우 효율적이며 PEP8 스타일 가이드를 잘 준수하고 있습니다.
<img width="820" height="354" alt="image" src="https://github.com/user-attachments/assets/8776e804-58ce-4b4b-8a7d-99a4d9a1765d" />


# 회고(참고 링크 및 코드 개선)
```
# 희선님의 프로젝트는 설계의 정석을 보여준 사례라고 생각합니다. 저는 단순히 구조적 차이(U-Net vs U-Net++)에만 집중했으나, 희선님은 한 단계 더 나아가 채널 차원수라는 핵심 하이퍼파라미터를 변수로 두어 모델의 체급별 성능 변화를 추적하여 실험했습니다. UNetPP_ch32 모델이 UNet_base64 모델에 비해 파라미터 수는 훨씬 적음에도 불구하고 상당히 근접한 IoU를 기록했다는 분석은, U-Net++의 구조적 우월성을 증명하는 아주 좋은 근거였습니다. 실험 조건을 완벽히 통제(Seed 고정, 동일 Augmentation)한 상태에서 진행된 Ablation Study라 결과의 신뢰도가 매우 높게 느껴졌습니다.

[U-Net++: A Nested U-Net Architecture](https://arxiv.org/abs/1807.10165): 구현된 Dense Skip Path의 논리적 근거를 확인하기 위해 원문 논문을 참고했습니다.
```
