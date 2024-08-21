# LLM을 이용한 제안서 자동 작성 프로그램
![image](https://github.com/user-attachments/assets/9afed112-6acd-4168-8e87-3c7e9774bc13)
>

</br>

# 1. 개요
## 💡 프로젝트 소개
### LLM을 이용한 제안서 자동작성 프로그램
  - 제안요청서를 업로드하면 제안요청서를 각 섹션으로 분리한다.
  - 제안요청서에 제시된 제안서의 총 매수와 사업목적에 맞게 목차를 생성한다.
  - 목차가 마음에 들지 않다면 사용자의 개입으로 목차를 요구사항에 맞게 변경할 수 있다.
  - 생성된 목차의 세부주제와 제안요청서의 요구사항에 맞게 각 섹션당 알맞는 내용을 응답한다.
  - 각 소주제에 대한 내용을 채팅창에서 수정도 가능하고 질문도 가능하다.

</br>

## 💡 제안배경
- 제안요청서에 따라 제안서를 작성하는 방식은 비슷하지만 매번 새로운 주제, 새로운 아이디어를 창조해야하기 때문에 다른 부분에 신경쓰기가 어려워서 제안됐다.

- > 제안서(1부) 작성 외주 = 약 5000만원 , 현재 제안서 작성 인건비 = 약 3000만원/ 제안서 작성 인건비 절약 가능
  
</br>

# 2. 사용 언어
| 구분         | 내용               |
|--------------|-------------------|
| 사용 언어    | <img src="https://img.shields.io/badge/Python-F80000?style=for-the-badge&logo=python&logoColor=white"> <img src="https://img.shields.io/badge/HTML-239120?style=for-the-badge&logo=html5&logoColor=white" />|
| DB  | <img src="https://img.shields.io/badge/Chroma-F80000?style=for-the-badge&logo=chroma&logoColor=black" />|
| API |![image](https://github.com/user-attachments/assets/1d019b72-a680-46db-9a93-4c8ce99ff338)![image](https://github.com/user-attachments/assets/49900c24-368e-41f1-98fd-fa86924a8706)
| BACK-END  |  <img src="https://img.shields.io/badge/Python-F80000?style=for-the-badge&logo=python&logoColor=white">|
| storage   | <img src="https://techrecipe.co.kr/wp-content/uploads/2020/08/200824_Google-Drive_001.jpg" width="100">|
| 라이브러리| ![image](https://github.com/user-attachments/assets/2c480a08-4b8c-4bfc-8ca4-839fa7014d80) ![image](https://github.com/user-attachments/assets/28c337d6-69cc-458f-89fe-093a1bd92037)|
| IDE   | ![image](https://github.com/user-attachments/assets/768ad5f8-acb4-4361-86a8-cb760f0fcd92)
|

</br>

# 3. 기능



## 3.1 목차생성
![image](https://github.com/user-attachments/assets/1a8b6d95-3992-4652-ab87-27336c9426da)


- Pdf 파일을 업로드한다.
- 제안요청서에 제시된 제안서 총매수와 사업목적등의 섹션을 파싱하여 LLM이 목차를 생성한다.

</br>

## 3.2 목차 재생성

![image](https://github.com/user-attachments/assets/78b439f8-f12d-4bef-b158-90fce9f77b6e)
![image](https://github.com/user-attachments/assets/399634bf-24ae-4840-ba79-f97b38040b57)
![image](https://github.com/user-attachments/assets/fc9d30d9-4245-4588-9601-cdbb90d24c36)



- 생성된 목차를 기반으로 사용자가 개입하여 목차를 수정할 수 있다.
- 목차가 맘에 들면 목차 확정 버튼을 누른다.


</br>

## 3.3 제안서 작성

![image](https://github.com/user-attachments/assets/7bd6fb77-1b4c-42c0-bce6-138ea3a040a0)



  - 목차 확정을 누르면 소주제를 기반으로한 카드 섹션들이 소주제 갯수대로 생성된다.
  - 각 하나의 카드 섹션마다 소주제에 맞는 알맞은 응답이 Stream형식으로 생성된다.

</br>

## 3.4 채팅 (제안서에 대한 질문)
![image](https://github.com/user-attachments/assets/03417fe0-828b-4bb3-aa5d-131970fca39f)




  - 카드섹션에 대한 응답을 확인한다.
  - 응답 내용중 그 섹션에 대해서만으로 질문이 가능하다.

</br>

## 3.5 채팅 (작성된 제안서 수정)

![image](https://github.com/user-attachments/assets/e0d7b2da-d481-4638-89f0-1e385de7e02c)


  - 이미 작성되었던 제안서가 마음에 들지않으면 다시 작성해달라고 할 수 있다.


</details>

# 4. 트러블 슈팅
### 📍 모델 문제

<details>
<summary><b> 자세히 보기</b></summary>
  
#### 문제 상황
  - 오픈소스 모델(Llama3) 의 응답이 느리고 기대에 미치지 못함.

#### 해결 시도
  - 모델 파인튜닝, 퓨샷 학습, 벡터데이터베이스 RAG 등 다양한 에이전트를 붙혀놔도 성능이 썩 좋지않았다.

#### 해결 방안
  - 클로드 API 사용

</details>

</br>

### 📍 모델 파인튜닝 및 GGUF 파일 변환

<details>
<summary><b> 자세히 보기</b></summary>

#### 문제 상황
  - LLM 모델들이 대부분 용량이 어마어마해서 파인튜닝 시 GPU가 터짐. 

#### 해결 시도
  - unsloth 사용 -> unsloth를 사용할 수 있는 모델들이 정해져있어서 내가 사용하는 모델에는 적용 불가
  - 모델 양자화 -> 양자화와 LoRA를 사용해 학습후 GGUF 변환 하기전 양자화 하기전 모델과 병합후 GGUF파일변환 후 다시 양자화 

#### 해결 방안
  - 모델 양자화 -> 양자화와 LoRA를 사용해 학습후 GGUF 변환 하기전 양자화 하기전 모델과 병합후 GGUF파일변환 후 다시 양자화 


</details>

</br>

# 5. 개발 기간
## 개발 기간
> - 전체 개발 기간 : 2024-07-16 ~ 2024-08-21

# 6. 팀원소개

<table>
  <tr>
    <td align="center"><img src="https://github.com/KIMGUUNI/A_EyeF/assets/118683437/278b105e-c98e-4238-a8b3-0a6a54cd0908" width="140" height="180" /></td>

  </tr>
  <tr>
    <td align="center"><strong>김찬혁</strong></td>
  </tr>
  <tr>
    <td align="center"><b>개인프로젝트</b></td>
  </tr>
  <tr>
    <td align="center"><a href="https://github.com/chanhyuckkim" target='_blank'>github</a></td>
  </tr>
</table>

</br>

