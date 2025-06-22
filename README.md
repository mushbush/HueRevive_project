# HueRevive_project

> model url: https://colab.research.google.com/drive/188jh_xwRQrSkT5VYd-9_xnS_We4GHjnE


## 📌 프로젝트 제목


> AI프로젝트 강의 기말 프로젝트
> 
> ' 딥러닝을 활용한 흑백 사진 컬러 복원 AI '


## 🎯 프로젝트 목표


![image](https://github.com/user-attachments/assets/b5158a79-be21-4ba5-8b3d-b75608e1ae38)


- 흑백 이미지의 컬러화에 대한 수요 증가
- 사진의 컬러화로 이미지의 상황에 대한 시각적 이해도, 몰입도 및 생동감 상승
- 수작업 컬러화 작업을 AI로 진행하며 쉽고 빠르고 편리하고 금전적 부담 감소
- 최대한 현실감 있고 인간의 시선과 비슷하도록 복원하는 것이 목표


## ⚙️ 프로젝트 진행 과정


### flowchart
![image](https://github.com/user-attachments/assets/79d41b45-e585-468c-a711-682f438358e8)


---


### dataset
![image](https://github.com/user-attachments/assets/af0eff0c-caae-4a0f-bdaa-b213757d30b3)

- 데이터는 해당 데이터 셋에서 일부를 사용하여 color 1,500 / gray 1,500 / test 150 / validation 200 장을 사용함.


---


### model
![image](https://github.com/user-attachments/assets/f42449f4-b486-45fd-ab6d-801680140dbd)

- 프로젝트에 사용한 모델은 Dacon의 '이미지 색상화 및 손실 부분 복원 AI 경진 대회'의 baseline 코드에서 시작하였으며,
이후 프로젝트를 진행하며 목표에 맞도록 코드를 추가함.


- 모델은 U-net generator + PatchGAN Discriminator인 Pix2Pix


- 과정에 따라 A, B, C의 총 3개의 모델 제공
- B, C 모델은 A 모델을 기반으로 하여 시각적 품질 향상을 위해 추가로 하이퍼파라미터를 조정함.


![image](https://github.com/user-attachments/assets/878f1720-e8e0-40b3-b01a-55ac90bceb3e)
![image](https://github.com/user-attachments/assets/0267cf7c-a9fa-4631-b7d7-6e382b93859f)
![image](https://github.com/user-attachments/assets/6a705fd5-7c93-42a1-a2d0-7324f19a6a08)


---


### 세 모델 결과값 비교


![image](https://github.com/user-attachments/assets/e4d8051d-1c3c-4eb9-85c7-a5ac84e566d8)


## 🛠 개선할 점

1. 풍경에 몰린 학습용 데이터


![image](https://github.com/user-attachments/assets/a85dbf5e-faad-45c3-84c7-750e6145b710)


- 흑백 풍경 이미지는 결과가 괜찮게 나옴
- 학습 이미지에 적은 인물, 동물, 식물은 색이 제대로 나오지 않음


2. 튀는 일부 색감


![124](https://github.com/user-attachments/assets/64456f3d-5e84-4e02-a1fa-7fa2f459e5c3)


- 일부 색상에 대해서 공격적으로 사용하며 특정 색이 깨져서 나옴
- 하이퍼파라미터 값의 세밀한 조정과 학습률에 대한 각각의 조정이 추가적으로 필요함
