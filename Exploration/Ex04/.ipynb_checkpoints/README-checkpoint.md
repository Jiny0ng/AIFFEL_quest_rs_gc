# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 이규철
- 리뷰어 : 박범찬


# PRT(Peer Review Template)
- [x]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 문제에서 요구하는 최종 결과물이 첨부되었는지 확인
        - 중요! 해당 조건을 만족하는 부분을 캡쳐해 근거로 첨부
            - 각 시각화 이미지 분류 및 비교가 잘 되어 있음
    <img width="596" height="643" alt="image" src="https://github.com/user-attachments/assets/f5953a84-ac65-44dd-aab5-62c2d74eef32" />

    
- [x]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 해당 코드 블럭을 왜 핵심적이라고 생각하는지 확인
    - 해당 코드 블럭에 doc string/annotation이 달려 있는지 확인
    - 해당 코드의 기능, 존재 이유, 작동 원리 등을 기술했는지 확인
    - 주석을 보고 코드 이해가 잘 되었는지 확인 
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
    <img width="761" height="160" alt="image" src="https://github.com/user-attachments/assets/b8b17e4f-a896-4854-ab29-4b66e35833a3" />

        
- [x]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**
    - 문제 원인 및 해결 과정을 잘 기록하였는지 확인
    - 프로젝트 평가 기준에 더해 추가적으로 수행한 나만의 시도, 
    실험이 기록되어 있는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
    <img width="618" height="400" alt="image" src="https://github.com/user-attachments/assets/a69f9474-31e4-4b6c-afb2-5de1a8b4e3e0" />

        
- [x]  **4. 회고를 잘 작성했나요?**
    - 주어진 문제를 해결하는 완성된 코드 내지 프로젝트 결과물에 대해
    배운점과 아쉬운점, 느낀점 등이 기록되어 있는지 확인
    - 전체 코드 실행 플로우를 그래프로 그려서 이해를 돕고 있는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
     <img width="763" height="401" alt="image" src="https://github.com/user-attachments/assets/92a24c52-11ee-4de2-82b7-58130f6db7fa" />

        
- [x]  **5. 코드가 간결하고 효율적인가요?**
    - 파이썬 스타일 가이드 (PEP8) 를 준수하였는지 확인
    - 코드 중복을 최소화하고 범용적으로 사용할 수 있도록 함수화/모듈화했는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
    <img width="624" height="262" alt="image" src="https://github.com/user-attachments/assets/503c70a0-5de2-490d-8a43-4876e06eede0" />


# 회고(참고 링크 및 코드 개선)

- DeepLab v3를 기반으로 춤추는 사람 이미지와 카페트 위에 누워 있는 고양이 이미지에 대해 객체 분할을 수행하였다.
    - 다양한 이미지(블러, 오버레이, 마스킹, 병합) 등의 경우들을 실험하고 도출함

- 발생하는 문제에 대한 해결책 제시
    - 디코더 모듈을 포함한 DeepLab v3+ 모델을 사용함으로써 개선할 수 있음
    - DeepLab v3+는 기존 구조에 디코더 모듈을 추가하고, 저수준 피처와 고수준 피처를 결합하여 보다 정밀한 경계 복원이 가능
    - 실제 사용 환경에 맞춘 도메인 특화 데이터셋을 구성하고 이를 기반으로 사전학습된 모델을 파인튜닝하는 접근 방식 제안

- 시각화 구성
    - 원본 이미지와 합성 이미지 간의 비교군을 보기 쉽게 시각화함
<img width="787" height="549" alt="image" src="https://github.com/user-attachments/assets/d4140146-57c5-4fee-843b-53f60c766bb1" />
