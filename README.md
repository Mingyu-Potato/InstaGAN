<div>
real_A_img(실제 볼트 이미지)와 real_B_img(실제 볼트 빠짐 이미지)와 각각의 이미지의 마스크를 이용하여, real_A_img의 마스크 부분은 real_B_img의 마스크 부분으로 새로 생성해내고, real_B_img의 마스크 부분은 real_A_img의 마스크부분으로 새로 생성해냅니다. 그 결과는 아래 그림과 같습니다.
</div><br>

<div align="center"><img src="https://user-images.githubusercontent.com/91408214/215037360-e9921ebb-bfb4-4455-a9fb-4ec9cae7f61a.png"></div>
<div align="center"><span><b>500 epoch의 결과 이미지</b></span></div><br><br>

<div align="center"><img width="450px" src="https://user-images.githubusercontent.com/91408214/215037383-e76e950c-abfb-4f54-bd38-68b6a6a6673e.png"></div>
<div align="center"><span><b>real_A_img(볼트) 사진으로부터 fake_B_img(모델이 만든 볼트 빠진 사진) 생성</b></span></div><br><br>
