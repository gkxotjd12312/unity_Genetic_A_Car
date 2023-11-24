# unity_Genetic_A_Car
#인공지능 # 2D유니티 # 유전알고리즘 # 자율주행


## 📜 프로젝트 소개 
AI초입부분을 공부할때 알게된 유전알고리즘으로 가상 공간에서 간단한 자율주행 모델을 만들어봤습니다.
[다른 사람들이 만든거를 보고 저도 저만의 방식으로 하나 만들어 보고싶어서 라이브러리 없이 직접 하나하나 만들어 봤습니다.]

## ⌚ 개발 기간
* 2021.02 ~2021.05

## 👨🏿‍🤝‍👨🏿 제작 맴버
 - 하태성 : 가상 공간 제작, DNN모델 제작, Genetic학습알고리즘 제작

## 🛠 개발 환경
- C#     
- Unity 

# 🎥지금부터 설명을 시작하겠습니다.

![슬라이드1](https://github.com/gkxotjd12312/unitiy_Genetic_A_Car/assets/54784059/4f064b59-1054-4e33-b1a1-9647dfe1e0ce)
 - 자율주행 모델을 만들기 위한 가상 공간은 위에 보이는것처럼 좌우, 대각선, 정면에 있는 벽과의 거리를 Ray를 이용해 수집합니다. 수집한 데이터는 총 5개로 Input값으로 사용됩니다.
 - 학습공간은 총 3가지로 1단계부터 단계별로 어렵게 만들었고 마지막은 급 커브로 마무리를 했습니다.

![슬라이드2](https://github.com/gkxotjd12312/unitiy_Genetic_A_Car/assets/54784059/8d3b8ac0-64bd-43d9-9cad-b3122836de13)
 - 다음은 자동차의 DNN모델 제작부분입니다. 그림에서 보이는데로 DNN을 제작하였고, 활성화 함수같은 경우 기존에 사용하던 0,1만 출력하는 계단함수가 아닌 -1,0,1도 출력할수 있도록 제작하였습니다.

![슬라이드3](https://github.com/gkxotjd12312/unitiy_Genetic_A_Car/assets/54784059/bcf8e2f8-0350-447d-9d8e-6759b49aac56)
 - DNN모델을 학습 시키는 유전 알고리즘 같은 경우 자연 선택설을 기초로 한 생물의 정자생존 알고리즘입니다.
 - 저의 유전 알고리즘은 생물의 염색체 교차과정처럼 부모 유전자로부터 절반씩 유전 정보를 받고 약 10% 돌연변이화를 시킴으로써 부모 유전 정보에서 찾을 수 없는 최적의 값을 찾도록 제작하였습니다.

![슬라이드4](https://github.com/gkxotjd12312/unitiy_Genetic_A_Car/assets/54784059/ee901788-ef9d-460b-b7ed-35102025c268)
 - 첫 에피소드의 과정을 보여드리면 다음과 같습니다.
1) 처음에 각자 다른 DNN을 가진 10명을 Agent를 제작합니다.
2) 10명의 에이전트들은 그림과 같이 같은 공간에서 레이싱을 하게되고
3) 학습 공간에서 오랫동안 생존하며 멀리간 아이에게 높은 Reward를 주고 첫번째 에피소드는 끝이 납니다.

![슬라이드5](https://github.com/gkxotjd12312/unitiy_Genetic_A_Car/assets/54784059/0cfdcb9c-5486-4415-9149-bc58f74912ac)
 - 첫번째 에피소드가 끝이 나면 다음 에피소드에 사용할 에이전트10명을 다음과 같이 준비합니다.
 - 이후에 이전 에피소드처럼 레이싱을 반복하며 학습을 이어나갑니다.
1) Agent 1번 : 1등 유전자 그대로 가져온다.
2) Agent 2번 : 1등 유전자에 10% 돌연변이화만 시켜 가져온다.
3) Agent 3번~8번 : 1등부터 6등에 저가 만든 genetic_algorithm을 적용시켜 가져온다.
4) Agent 9번~10번 : 위와 같은 과정으로 얻기 힘든 데이터를 가져오기위해 완전히 새로운 Agent를 가져온다.

## 🎞 학습 동영상

https://github.com/gkxotjd12312/unitiy_Genetic_A_Car/assets/54784059/6328d501-a568-45ce-b92e-610c3b57441e

https://github.com/gkxotjd12312/unitiy_Genetic_A_Car/assets/54784059/eae1f4d2-3750-4ea8-af32-e8aaf6406023

https://github.com/gkxotjd12312/unitiy_Genetic_A_Car/assets/54784059/4d4c507b-b17f-490c-99ad-538d69a0aae6

https://github.com/gkxotjd12312/unitiy_Genetic_A_Car/assets/54784059/53e40c21-c191-41dd-be54-214df73baff7














