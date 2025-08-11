# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 코더의 이름을 작성하세요.
- 리뷰어 : 리뷰어의 이름을 작성하세요.


# PRT(Peer Review Template)
- [ ]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 문제에서 요구하는 최종 결과물이 첨부되었는지 확인
    - 각 모델별로 학습하고 평가하는 부분이 완성되어있다.
    - <img width="400" height="600" alt="image" src="https://github.com/user-attachments/assets/647e12ce-b61f-4492-ba78-96dbb7240b29" />
    
- [ ]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 해당 코드 블럭을 왜 핵심적이라고 생각하는지 확인
    - 해당 코드 블럭에 doc string/annotation이 달려 있는지 확인
    - 해당 코드의 기능, 존재 이유, 작동 원리 등을 기술했는지 확인
    - 주석을 보고 코드 이해가 잘 되었는지 확인
    - pad_sequences_pre 등의 중요 함수에 주석이 잘 달려있다.
    - <img width="400" height="600" alt="image" src="https://github.com/user-attachments/assets/2826fb29-d2f2-4310-a37d-f500a530494e" />

- [ ]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**
    - 문제 원인 및 해결 과정을 잘 기록하였는지 확인
    - 프로젝트 평가 기준에 더해 추가적으로 수행한 나만의 시도, 
    실험이 기록되어 있는지 확인
    - 자체 학습 W2V vs 사전학습 W2V, RNN/LSTM/CNN 비교 실험은 좋으나 정확도를 계산할 때, Simgoid를 적용하지 않아 재실험이 필요하다.
    - <img width="400" height="250" alt="image" src="https://github.com/user-attachments/assets/35250287-d7a2-429e-9c3e-33491e21061a" />

- [ ]  **4. 회고를 잘 작성했나요?**
    - 주어진 문제를 해결하는 완성된 코드 내지 프로젝트 결과물에 대해
    배운점과 아쉬운점, 느낀점 등이 기록되어 있는지 확인
    - 전체 코드 실행 플로우를 그래프로 그려서 이해를 돕고 있는지 확인
    - 임베딩의 품질과 LSTM에 대한 통찰 등을 회고로 잘 남겨두었다.
    - <img width="400" height="100" alt="image" src="https://github.com/user-attachments/assets/e532de0a-46da-44e5-9910-de541b0e6ccd" />

- [ ]  **5. 코드가 간결하고 효율적인가요?**
    - 파이썬 스타일 가이드 (PEP8) 를 준수하였는지 확인
    - 코드 중복을 최소화하고 범용적으로 사용할 수 있도록 함수화/모듈화했는지 확인
    - 학습 루프는 모두 동일하기 때문에 함수화했으면 더 좋았을 것 같다.


# 회고(참고 링크 및 코드 개선)
- 모델 내부에 Sigmoid가 존재하지 않고, BCEWithLogitsLoss를 통해 학습했다. 그러면 정확도를 계산할 때, 별도로 시그모이드를 적용해야한다.
- pad_sequences_pre 함수는 주석과 동작이 일치하지 않는 부분이 존재한다.
- 주석에서는 앞에서 자른다고 되어있는데 코드 상에는 post-truncating 방식으로 작성되어있음. (padding은 pre-padding이 맞음)
```
# 리뷰어의 회고를 작성합니다.
# 코드 리뷰 시 참고한 링크가 있다면 링크와 간략한 설명을 첨부합니다.
# 코드 리뷰를 통해 개선한 코드가 있다면 코드와 간략한 설명을 첨부합니다.
```
