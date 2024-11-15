# LLM 기반 지능형 제안서 자동 생성 시스템
![image](https://github.com/user-attachments/assets/f8ffb005-e09b-495e-b0f2-6e4a7a3edc15)

## 목차
1. [프로젝트 개요](#1-프로젝트-개요)
2. [기술 스택](#2-기술-스택)
3. [핵심 기능](#3-핵심-기능)
4. [기술적 도전과 해결 방안](#4-기술적-도전과-해결-방안)
5. [개발 기간간](#5-개발-기간)
6. [개발자 정보](#6-개발자-정보)

# 1. 프로젝트 개요
## 💡 혁신적 제안서 자동화 솔루션
본 프로젝트는 최첨단 대규모 언어 모델(LLM)을 활용하여 기업의 제안서 작성 프로세스를 획기적으로 개선하는 지능형 시스템입니다. 이 솔루션은 다음과 같은 고급 기능을 제공합니다:

- 제안요청서 자동 분석 및 섹션별 최적화 분리
- 고도화된 알고리즘을 통한 맞춤형 제안서 구조 생성
- 사업 목적 및 요구사항에 최적화된 동적 목차 시스템
- AI 기반 섹션별 컨텐츠 자동 생성 및 실시간 스트리밍
- 대화형 인터페이스를 통한 지능적 내용 수정 및 개선
-  실시간 웹소켓 기반 공동 작업
- AI 기반 이미지 생성 및 통합


## 💡 혁신의 필요성
현대 비즈니스 환경에서 고품질 제안서의 중요성은 날로 증가하고 있습니다. 그러나 전통적인 제안서 작성 방식은 다음과 같은 문제점을 안고 있습니다:

- 반복적이면서도 매번 새로운 창의성을 요구하는 모순적 특성
- 높은 인적 자원 소모와 시간 비용 (제안서 1부당 약 3,000만원의 인건비)
- 외주 의존도 증가로 인한 과도한 비용 발생 (외주 제작 시 약 5,000만원/부)

본 시스템은 이러한 문제를 해결하고, 제안서 작성 프로세스의 효율성과 품질을 동시에 향상시키는 것을 목표로 합니다.
https://img.shields.io/badge/Stable%20Diffusion-FF6B6B?style=for-the-badge&logo=stability-ai&logoColor=white
# 2. 기술 스택
| 구분         | 사용 기술               |
|--------------|-------------------|
| 프론트엔드    | <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white"> <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white"> <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"> |
| 백엔드        | <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"> <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white"> <img src="https://img.shields.io/badge/SQLAlchemy-FF0000?style=for-the-badge&logo=sqlite&logoColor=white"> |
| 데이터베이스  | <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white"> <img src="https://img.shields.io/badge/Chroma-4285F4?style=for-the-badge&logo=google-chrome&logoColor=white">|
| API 통합     |<img src="https://img.shields.io/badge/Claude-FF9900?style=for-the-badge&logo=openai&logoColor=white"> <img src="https://img.shields.io/badge/Gemini-333333?style=for-the-badge&logo=google&logoColor=white"> <img src="https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white"> <img src="https://img.shields.io/badge/Stable%20Diffusion-FF6B6B?style=for-the-badge&logo=stability-ai&logoColor=white"> |
| 클라우드 저장소 |<img src="https://img.shields.io/badge/AWS%20S3-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white"> <img src="https://techrecipe.co.kr/wp-content/uploads/2020/08/200824_Google-Drive_001.jpg" width="100">|
| 핵심 라이브러리 |<img src="https://img.shields.io/badge/LangChain-FF66CC?style=for-the-badge&logo=codeforces&logoColor=white"> <img src="https://img.shields.io/badge/PyMuPDF-4285F4?style=for-the-badge&logo=python&logoColor=white"> <img src="https://img.shields.io/badge/pptx-FFB6C1?style=for-the-badge&logo=microsoft-powerpoint&logoColor=white">|
| 개발 환경     | ![image](https://github.com/user-attachments/assets/768ad5f8-acb4-4361-86a8-cb760f0fcd92) |

# 3. Database ERD
데이터베이스 ERD는 [여기](docs/database-erd.md)에서 확인할 수 있습니다

# 3. 핵심 기능

## 3.1 AI 기반 지능형 목차 생성
![image](https://github.com/user-attachments/assets/a3eb4f7b-161f-46a9-9ee5-90e04ef05fad)
- 고급 자연어 처리 기술을 활용한 PDF 문서 자동 분석
- 제안요청서의 핵심 요구사항 및 사업 목적 등 추출을 통한 최적화된 목차 구조 생성

## 3.1.1 제안요청서 지능형 요약 및 데이터베이스 통합
![image](https://github.com/user-attachments/assets/7b0810e1-f202-4abf-af7e-5432d74c26e1)
- 고도화된 텍스트 요약 알고리즘을 통한 제안요청서 핵심 내용 추출
- 사용자 검증 기반의 지능형 데이터베이스 저장 시스템

## 3.1.2 목차 구성 로직 상세 분석
![image](https://github.com/user-attachments/assets/ed7e4ee1-c950-4e13-b16a-d3a757e810db)
![image](https://github.com/user-attachments/assets/940c66bb-b1b3-49a2-8692-c676908c3ac4)
- 딥러닝 기반 목차 구성 논리 시각화 시스템
- 사용자 피드백을 반영한 실시간 목차 최적화 알고리즘
- 산업별, 분야별 최적 목차 구조 학습 및 추천 기능

## 3.2 동적 목차 재구성 시스템
![image](https://github.com/user-attachments/assets/41332e38-9790-414f-bf80-f17b224c2628)
![image](https://github.com/user-attachments/assets/e71f0faf-5fb9-40c9-99ed-7c98202f848a)
- 사용자 인터랙션 기반 실시간 목차 조정 기능
- AI 추천 시스템을 통한 최적 구조 제안
- 목차 변경에 따른 전체 제안서 구조 자동 최적화

## 3.3 AI 기반 제안서 컨텐츠 자동 생성
![image](https://github.com/user-attachments/assets/ec241188-fe51-4141-9836-dd2a6a304975)
![image](https://github.com/user-attachments/assets/8246799e-d5cb-4136-89c3-3f7324b9b2eb)
![l_288923124_1067_fcd7ebcc5e8e1522d0a8ffefc0904772](https://github.com/user-attachments/assets/c1037f48-b0da-4964-a9a9-8ad8c3f754f2)

- 목차 기반 섹션별 맞춤형 컨텐츠 실시간 생성
- 고급 자연어 생성 모델을 활용한 전문적이고 설득력 있는 내용 작성
- 동적 헤드카피 생성 시스템을 통한 섹션별 핵심 메시지 강조
- 사용자 친화적 카드 인터페이스를 통한 직관적 내용 관리
- AI 이미지 생성 및 검색 시스템
  - Stable Diffusion을 활용한 맞춤형 이미지 생성
  - 키워드 기반 이미지 크롤링 및 S3 저장 시스템
  - 생성된 이미지의 프롬프트 및 검색 키워드 실시간 표시

## 3.4 대화형 AI 기반 제안서 최적화
![image](https://github.com/user-attachments/assets/e01dca51-389b-4ae6-8349-b2f408c42b88)
- 컨텍스트 인식 AI 채팅봇을 통한 지능형 질의응답 시스템
- 제안서 전체 맥락을 고려한 정확하고 일관된 정보 제공
- 사용자 피드백 기반 실시간 학습 및 컨텐츠 개선

## 3.5 AI 지원 제안서 실시간 편집 시스템
![image](https://github.com/user-attachments/assets/37864854-8cb1-4d46-91bd-91fddc8aa217)
![image](https://github.com/user-attachments/assets/3a1f9f9e-4128-4454-ad03-e6ac57498be4)

- 자연어 처리 기반 사용자 요구사항 정확한 해석 및 반영
- 컨텐츠 품질 향상을 위한 AI 제안 시스템
- 편집 이력 관리 및 버전 제어를 통한 안정적인 문서 관리
- 실시간 협업 기능을 통한 팀 단위 제안서 작성 지원
  - WebSocket 기반 실시간 공동 편집 시스템
  - 동일 계정 사용자 간 실시간 문서 동기화
  - 변경 사항 실시간 반영 및 충돌 방지 시스템

# 4. 기술적 도전과 해결 방안
### 📍 LLM 성능 최적화

<details>
<summary><b> 상세 내용 보기</b></summary>
  
#### 도전 과제
  - 오픈소스 LLM(Llama3)의 성능 및 응답 속도 개선 필요성

#### 시도한 접근법
  - 모델 파인튜닝, 퓨샷 학습, 벡터 데이터베이스 기반 RAG(Retrieval-Augmented Generation) 등 다양한 최적화 기법 적용

#### 최종 해결책
  - Claude API 도입을 통한 고성능 LLM 활용
  - 자체 개발 프롬프트 엔지니어링 기법을 통한 응답 품질 향상
  - 하이브리드 접근법: 로컬 경량 모델과 클라우드 기반 고성능 모델의 최적 조합

</details>

### 📍 대규모 언어 모델의 효율적 학습 및 배포

<details>
<summary><b> 상세 내용 보기</b></summary>

#### 도전 과제
  - 대용량 LLM의 학습 및 배포 시 하드웨어 리소스 한계 극복 

#### 시도한 접근법
  - unsloth 등 모델 최적화 라이브러리 활용 검토
  - 다양한 모델 압축 및 양자화 기법 실험

#### 최종 해결책
  - LoRA(Low-Rank Adaptation) 기반 효율적 모델 학습 구현
  - GGUF(GPT-Generated Unified Format) 변환을 통한 모델 최적화
  - 단계적 양자화 프로세스 도입: 
    1) 초기 학습 
    2) LoRA 적용 
    3) 원본 모델과 병합 
    4) GGUF 변환 
    5) 최종 양자화

</details>

### 📍 토큰 제한 극복을 위한 고급 텍스트 처리

<details>
<summary><b> 상세 내용 보기</b></summary>

#### 도전 과제
  - LLM의 입출력 토큰 제한으로 인한 대용량 제안요청서 처리 어려움

#### 시도한 접근법
  - 문서 분할 및 청크 처리 기법 적용
  - 다중 패스 처리 방식 검토

#### 최종 해결책
  - 고급 자연어 처리 기술을 활용한 지능형 문서 분할 알고리즘 개발
  - 섹션별 컨텍스트 인식 파싱 시스템 구축
  - 계층적 요약 기법을 통한 핵심 정보 추출 및 재구성
  - 동적 토큰 할당 시스템을 통한 효율적 리소스 관리

</details>

# 5.  개발 기간
- 전체 개발 기간: 2024-07-08 ~ 2024-10-24



# 6. 개발자 정보

<table>
  <tr>
    <td align="center"><img src="https://github.com/KIMGUUNI/A_EyeF/assets/118683437/278b105e-c98e-4238-a8b3-0a6a54cd0908" width="140" height="180" /></td>
  </tr>
  <tr>
    <td align="center"><strong>김찬혁 (Chan-Hyeok Kim)</strong></td>
  </tr>

</table>
