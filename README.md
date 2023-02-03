## Introduction
드론으로부터 촬영된 송전철탑에서 볼트의 빠짐 여부를 검출하려 했다. 그런데 볼트가 빠져있는 데이터는 많지 않기 때문에 InstaGAN을 통한 Data Augmentation을 시도하였다.
<br><br>

## Method
1. 송전철탑 이미지로부터 볼트 부분만 label 처리된 json data를 이용하여, 볼트 부분을 crop하여 볼트 이미지를 생성하였다.
2. InstaGAN을 이용하여 볼트가 있는 사진으로부터 볼트가 빠진 사진을 생성해내었다.

## Result
real_A_img(실제 볼트 이미지)와 real_B_img(실제 볼트 빠짐 이미지)와 각각의 이미지의 마스크를 이용하여, real_A_img의 마스크 부분은 real_B_img의 마스크 부분으로 새로 생성해내고, real_B_img의 마스크 부분은 real_A_img의 마스크부분으로 새로 생성해냅니다. 그 결과는 아래 그림과 같습니다.

<div align="center"><img src="https://user-images.githubusercontent.com/91408214/215037360-e9921ebb-bfb4-4455-a9fb-4ec9cae7f61a.png"></div>
<div align="center"><span><b>500 epoch의 결과 이미지</b></span></div><br><br>

<div align="center"><img width="450px" src="https://user-images.githubusercontent.com/91408214/215037383-e76e950c-abfb-4f54-bd38-68b6a6a6673e.png"></div>
<div align="center"><span><b> 볼트 이미지를 이용해서 InstaGAN 모델이 볼트 빠짐 이미지 생성</b></span></div><br><br>

## Conclusion
trainset에 대해서는 실제 볼트가 빠져있는 것처럼 볼트가 빠진 사진을 잘 생성했지만, testset에는 trainset의 송전철탑 색상, 볼트 모양 등 여러 환경이 testset의 결과 이미지에서도 일부 나타나는 과적합 현상이 발생해서 아쉬운 부분도 있었다.
