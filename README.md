## custom dataset을 사용한 yolo object detection
yolo v5 모델을 사용한 custom object dection으로 개발 환경은 구글 코랩을 사용하였습니다.

## 데이터 수집
[roboflow.com](https://roboflow.com/)에서 제공해주는 Oxford Pets Dataset을 사용하였습니다.

## 데이터 가공
데이터셋에 포함되어 있는 data.yaml 파일의 경로를 수정해주었습니다.

## 모델 학습
```
!python train.py --img 416 --batch 16 --epochs 50 --data '/content/drive/My Drive/yolo_custom_model_training/custom_dataset/data.yaml' --cfg ./models/yolov5s.yaml --weights yolov5s.pt --name my_pet_yolov5s_results
```
yolov5s.pt를 사용하여 50번의 학습을 진행하였습니다.

## 결과 이미지
![result of yolo custom obeject detection](https://user-images.githubusercontent.com/61677941/115151551-4c4d0d00-a0a8-11eb-9029-be56a005c22b.jpg)

얼굴이 두눈과 함께 코, 입이 고루 잘 나와있는 사진은 예측을 잘하였지만 얼굴의 반 정도가 안 보이는 사진에 대해서는 부족한 모습을 보였습니다. 
