## :pig: 앙돈

---

### 실시간 양돈 재고관리를 위한 뭉침에 강건한 양돈 객체검출 모델 개발

### 2022 과학기술·공공 AI데이터 분석활용 경진대회 참가


## 👩‍👩‍👧‍👧 역할

---

`팀장`
<br/>
`Yolov7 이용 모델 학습 및 평가` : Yolov7 가중치 확인(e6e,tiny,x,w6,e6,d6) 및 학습 이미지 확보, 학습, 평가

## 🔗 프로젝트 개요

---

### 💡 기획 배경

 2022 과학기술·공공 AI데이터 분석활용 경진대회 참가를 위해 주제에 대하여 확인하던중 평소에 관심이 있던 이미지 분야 객체식별 관련 문제를 확인하였고 이전에 예전 기법중 하나인 
 MASK-RCNN 기법을 사용해본 이후 그때 확인하고 사용해보지 않았던 Yolov7을 활용해보고 싶어서 경진대회에 참가를 희망하였으며 이미지 분야에서 기초라고 할 수 있는 객체식별을 먼저
 해보고 싶은 마음이 들어서 경진대회에 참가하였습니다.
 또한 사진에서 객체를 식별하는 경우 학습시키는 이미지만 다르게 한다면 동일한 모델과 방식으로 다른 객체식별들도 해볼수 있다고 판단하여 해당 프로젝트를 진행하기 위해 팀원을 모집하고
 해당 프로젝트를 진행해 보았습니다.

### 📅 프로젝트 진행 기간

2022.09.21 ~ 2022.11.16

## 🖇️ 주요 내용

---

### 📝 Yolov7 모델 사용을 위한 전,후처리
- 학습 데이터 = 최초이미지(돼지 이미지 4583장 + 돼지 외 동물 이미지 906장)에 대하여 Roboflow를 통한 이미지 증식(x3) 및 Cutout적용 이미지 활용하여 총 16467장 학습에 활용
- 검증 데이터 = 돼지 이미지 817장 및 라벨 데이터
- 이미지 데이터 경로를 저장할 list로 정리 및 txt파일로 저장
- 또한 기존에 제공된 라벨데이터의 경우 라벨명이 미설정되어있는 데이터들이 있어 모든 라벨 데이터명 Pig로 수정
- convert2Yolo모듈 활용 제공된 라벨데이터(Json)을 Yolo에서 학습 가능한 형태인 txt파일로 변환
- ROboflow에서 제공하는 다양한 방식 활용(이미지 증식, Cutout적용 등)

- logging 및 importer을 활용하여 Yolov7에서 검증용 이미지에서 추출한 txt 라벨링 파일 json으로 변환


### 📝 Yolov7 모델 학습

- Robotflow에서 데이터 받아오는 형태로 테스트 진행(파일을 직접 구글 드라이브에 업로드할 필요가 없어서 학습하는데 시간이 많이 절약)
- Robotflow 미 사용시 학습 하기 위한 소수의 이미지만을 활용하여 학습 및 테스트도 병행 진행
- batch, epochs 수정하며 최적의 정확도 확인
- 20번 이상의 학습 및 검증과정 진행

## ⚒️ 협업 환경

---

### Cooperation & Communication

- Colab
- Goolgle drive
- Slack

### 성능평가 및 테스트 결과정리
- 성능평가 그래프
 -![성능평가](https://github.com/Raon-cs/pig/assets/108639467/a90a8b36-ec7f-4282-98ba-161fd310561e)

<br/>

- 테스트 결과정리
 - ![테스트 결과정리](https://github.com/Raon-cs/pig/assets/108639467/c4c2c998-f639-48e6-a970-d995af8360c7)
