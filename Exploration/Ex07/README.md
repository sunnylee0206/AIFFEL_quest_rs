# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 이희선
- 리뷰어 : 황성연


# PRT(Peer Review Template)
- [x]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 문제에서 요구하는 최종 결과물이 첨부되었는지 확인
        - 중요! 해당 조건을 만족하는 부분을 캡쳐해 근거로 첨부
        - <img width="598" height="824" alt="image" src="https://github.com/user-attachments/assets/d661773d-6f13-4855-9242-86b24b862b45" />
        - <img width="1412" height="504" alt="image" src="https://github.com/user-attachments/assets/c347a684-b899-40f9-8573-f0f0bf9a8dd8" />
        - <img width="1854" height="550" alt="image" src="https://github.com/user-attachments/assets/ea50bc2f-1e13-41d4-9130-b0f0aab13437" />
        - 평가 루브릭에 있는 데이터 전처리, 모델학습, 추상vs추출 비교를 모두 수행하였습니다.



    
- [x]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 해당 코드 블럭을 왜 핵심적이라고 생각하는지 확인
    - 해당 코드 블럭에 doc string/annotation이 달려 있는지 확인
    - 해당 코드의 기능, 존재 이유, 작동 원리 등을 기술했는지 확인
    - 주석을 보고 코드 이해가 잘 되었는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
        - <img width="756" height="774" alt="image" src="https://github.com/user-attachments/assets/3c4817d1-13cb-493b-a425-ca91493d37cf" />
        - 인코더, 어텐션, 디코더 구조를 잘 설계했고, 실습때와 다르게 거대해진 데이터셋 규모에 맞춰 양방향 LSTM과 additive어텐션을 사용했습니다.

        
- [ ]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**
    - 문제 원인 및 해결 과정을 잘 기록하였는지 확인
    - 프로젝트 평가 기준에 더해 추가적으로 수행한 나만의 시도, 
    실험이 기록되어 있는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
        
- [x]  **4. 회고를 잘 작성했나요?**
    - 주어진 문제를 해결하는 완성된 코드 내지 프로젝트 결과물에 대해
    배운점과 아쉬운점, 느낀점 등이 기록되어 있는지 확인
    - 전체 코드 실행 플로우를 그래프로 그려서 이해를 돕고 있는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
        - <img width="1876" height="568" alt="image" src="https://github.com/user-attachments/assets/f4cf29ee-b379-45fd-ace5-288ea4b255eb" />
           결론에 대한 분석과 회고가 잘 작성 되어있스니다.

        
- [x]  **5. 코드가 간결하고 효율적인가요?**
    - 파이썬 스타일 가이드 (PEP8) 를 준수하였는지 확인
    - 코드 중복을 최소화하고 범용적으로 사용할 수 있도록 함수화/모듈화했는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
        - <img width="746" height="776" alt="image" src="https://github.com/user-attachments/assets/16b2e901-2783-45f9-868c-ab8340eb61d3" />
        - 사진 외에도 여러가지 함수나 모델을 정의하여 범용적으로 사용가능하게 하였습니다.



# 회고(참고 링크 및 코드 개선)
```
평가 루브릭을 모두 만족했고, 데이터 셋(뉴스기사 요약)에 맞는 인코더와 어텐션 설계가 좋았습니다.
```
