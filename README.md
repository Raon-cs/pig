# yolo활용을 위한 전처리
1. json 데이터 yolo활용을 위한 txt형태로 변환(convert2Yolo 활용)

2. 라벨링명 변경(1번에서 변환시 라벨링명이 제대로 수행되었을시 미실시해도 가능)

# yolo활용 가중치 학습(yolo test code)
1. 사용할 기본 가중치 선정(yolov7-tiny.pt(small), yolov7.pt(medium), yolov7-e6e.pt(large)
2. batch_size, epochs, data등 필요사항 입
 
 
# 학습한 가중치 활용 모델 테스트

1. 사용할 가중치 설정(--weights /파일경로/가중치이름.pt), 정확도 설정(--confg 0.x), 테스트 이미지 경로 설정(--source 이미지경), txt파일 저장(--save-txt)

# yolo txt파일 json으로 변환

1. logging라이브러리 및 importer 활용(변환할 이미지 및 txt파일 경로 설정, yoloclasses(라벨링명) 설정

2. 변환된 json 파일 저장
