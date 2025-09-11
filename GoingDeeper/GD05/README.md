# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 이규철
- 리뷰어 : 최은학


# PRT(Peer Review Template)
- [X]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 증강을 보수적으로 접근해 학습 데이터가 적었음에도 상당히 완성도 있는 문장이 생성되었다.
    - <img width="400" height="250" alt="image" src="https://github.com/user-attachments/assets/69c36ac3-229d-45fe-8426-b208607c5c02" />

- [X]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - nn.TransformerEncoderLayer, nn.TransformerDecoder를 불러와 attention weights를 리턴하도록 모델을 구성해 어텐션 맵이 시각화 되도록 구성
    - 증강할 때, 유사도의 threshold를 지정해 진짜 유사한 단어(토큰)이 선택되었을 때에만 증강을 적용
    - <img width="450" height="450" alt="image" src="https://github.com/user-attachments/assets/4380dd63-d077-4931-88e2-bd23dda84eae" />
    - <img width="300" height="500" alt="image" src="https://github.com/user-attachments/assets/6a581c48-f949-4d3e-b0d0-0bb8b0719e30" />
    
- [X]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**
    - 레이어 수에 따른 지표 변화, 보수적인 증강 등 여러 시도를 했다.


- [X]  **4. 회고를 잘 작성했나요?**
    - 회고를 코드와 동일한 순서로 작성해 흐름을 그대로 볼 수 있었다.
    - <img width="700" height="300" alt="image" src="https://github.com/user-attachments/assets/37b4e658-ebad-488e-971f-664a0339f724" />
        
- [X]  **5. 코드가 간결하고 효율적인가요?**
    - 이전에 코드를 리뷰했을 때에는 효율적이지 못했는데 상당히 함수화/모듈화가 잘 되어있다.
    - 다음 사진은 생성, 어텐션 맵 시각화를 각 단계별로 함수화가 되어있는 것을 볼 수 있다.
    - <img width="400" height="600" alt="image" src="https://github.com/user-attachments/assets/a7fa9fcb-8350-4705-aaeb-a7c7c47d9280" />




# 회고(참고 링크 및 코드 개선)
```
# 데이터가 너무 적어 validation을 나누면 제대로 진행이 되지 않을 것이라 생각했었음
# loss 그래프를 보면, 고정 lr로 학습했음에도 불구하고 과적합이 발생하지 않고 상당히 잘 학습되는 것을 볼 수 있음
```
- <img width="300" height="200" alt="image" src="https://github.com/user-attachments/assets/837e2df9-99d7-40b3-bf4d-dbda637d8806" />
