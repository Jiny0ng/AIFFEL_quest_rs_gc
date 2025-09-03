# DKTC (<b>D</b>ataset of <b>K</b>orean <b>T</b>hreatening <b>C</b>onversations)

본 데이터셋은 [TUNiB](http://tunib.ai)이 [2021 인공지능 그랜드 챌린지](https://www.ai-challenge.kr/) 4차대회 음성인지 트랙에 참가하기 위해 자체적으로 제작한 데이터셋입니다. 이 챌린지는 임의의 대화 음성 파일을 놓고 그 대화의 성격을 위협 세부 클래스 4개 또는 일반 대화 중 하나로 예측하는 과제였습니다. 여느 대회와는 달리 주최측이 샘플 외에 별도로 학습 데이터를 제공하지 않아 참가팀이 스스로 데이터를 만들어야 했습니다. 

이번에 공개하는 데이터는 학습 데이터와 테스트 데이터로 나뉘어 있습니다. 학습 데이터는 '협박', '갈취', '직장 내 괴롭힘', '기타 괴롭힘' 등 4개 클래스가 약 1천 개 정도씩의 대화로 이루어져 있고, 테스트 데이터는 '협박', '갈취', '직장 내 괴롭힘', '기타 괴롭힘', '일반 대화' 등 5개 클래스가 100개씩의 대화로 이루어져 있습니다. 학습 데이터 중 빠져 있는 '일반 대화'는 [AI Hub](https://aihub.or.kr/)의 여러 대화 데이터셋에서 내려받아 학습에 활용할 수 있습니다. 어떤 일반대화 데이터를 모으고 학습에 활용하느냐 하는 것도 중요한 학습 전략이 될 수 있습니다.

- **알고리즘**
  
| 분야        | 사용된 모델                   |
| ----------- | ----------------------------- |
| Transformer   | mBERT, KoBERT, KLUE-BERT, GPT-1 |


- **학습 데이터 head**
<img width="547" height="729" alt="image" src="https://github.com/user-attachments/assets/55453207-015e-4a27-a463-4705a50ceab7" />


## 원본 데이터셋

|클래스|Class Num|Train|Test |
|:----:|:------:|:------:|:------------:|
|협박 |00| 896    | 100   |
|갈취  |01|981     | 100 |
|직장 내 괴롭힘  |02|979     |100|
|기타 괴롭힘 |03|1,094      |100|
|일반 |04| - |100|

## 튜닝 Train 데이터셋

**preprocessing 과정**
- train의 label 정수로 바꾸고 결측치, 중복 있는 행 제거
- label 별 분포 확인
- label 별 텍스트 길이 확인, 전체 텍스트 길이 확인
- label 별 분포의 평균과 전체 텍스트 길이를 통해 일상대화의 갯수와 텍스트의 길이 지정
- 생성한 텍스트를 train 데이터에 추가
- 자세한 train data 정제 과정은 EDA data에 README 참고
  
|클래스|Class Num|Train|
|:----:|:------:|:------:|
|협박 |00| 896    |
|갈취  |01|981     |
|직장 내 괴롭힘  |02|979     |
|기타 괴롭힘 |03|1,094      |
|일반 |04| 1,075 |

## Member

|Leader, Modeling|Modeling|EDA|EDA|
|:----:|:---:|:-----:|:---:|  
|**[Gyucheol Lee <br> 이규철](https://github.com/9cheol2)**|**[Bumchan Park <br> 박범찬](https://github.com/bumcoding)**|**[Chanwoong kim <br> 김찬웅](https://github.com/chanwoong0503)**|**[Hyoungill Kim <br> 김형일](https://github.com/nagu78)**|

## Source
  
[AIFFEL_DLThon_DKTC_online14](https://www.kaggle.com/competitions/aiffel-dl-thon-dktc-online-14/overview).
