# Right?Left?
2022/Spring/NLP/FinalProject

- 팀 구성
  - 20102112 박하백


- 작품 이름
  - 오른쪽?왼쪽? 정치성향 판독기


- 소개, 특징
  - 역대 미국 대통령(바이든-프랭클린 루즈벨트)의 연설, 인터뷰, 편지 같은 자료를 모아 모델을 학습시켰다. 자료 출처: (https://www.presidency.ucsb.edu/)
데이터의 수는 약 10,000 개. 
  - feature은 content_lst로, 위의 자료에 대한 본문의 내용이 저장되어있다. list 형태.
  - target은 party_lst에, 자료와 관련된 대통령이 어느 쪽 정당인지 0과 1로 표현되어 있다(0: Democractic, 1: Republican). list 형태.
  - 모델은 sklearn의 SVM를 이용하였다.
  - 모델 학습시에 Bag of Words를 이용하여 feature를 처리한다.
  - 학습된 모델은 model.pkl 로 저장되어 있다. (vectorizer, classifier) = model
  - 소스파일(ipynb)을 제외한 _lst나 model.pkl 등은 모두 pickle 라이브러리를 이용하여 저장하였다. 로드하여 쓸 때도 pickle을 써야한다.

- 모델 평가
  - Validation set approach와 Cross Validation을 이용하여 모델이 데이터를 잘 학습했는지 평가하였다.
  - Validation set approach 결과:
    - <img width="751" alt="ValidationSet" src="https://user-images.githubusercontent.com/74465964/170869938-0748a6c9-66af-4bae-8d68-b1e2c9f5d9b2.png">
  - Cross Validation 결과:


- 기능
  - RightLeftApp 에서 학습한 모델을 가지고 놀 수 있다.
  - 임의의 글을 입력하면 그 글이 republican 한지, democratic 한지 판단해준다.


- 데모
  - https://youtu.be/ZNwH5zgO5Ok

