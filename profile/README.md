
## 📚 AIVLE Book Manager – 전체 프로젝트 소개

**AIVLE SCHOOL 6반 16조**가 개발한 도서 관리 웹 애플리케이션입니다.
이 프로젝트는 사용자가 도서를 등록하고, OpenAI DALL·E API를 통해 **책 표지를 자동 생성**할 수 있도록 구성된 **풀스택 웹 서비스**입니다.

---

### 📌 프로젝트 개요

| 구분    | 설명                                       |
| ----- | ---------------------------------------- |
| 프로젝트명 | AIVLE Book Manager                       |
| 목적    | 도서 등록/수정/조회 + AI 기반 커버 이미지 생성            |
| 주요 기능 | 도서 CRUD, DALL·E 3 기반 이미지 생성, 사용자 키 입력 방식 |
| 프론트엔드 | React + MUI (Vite 기반)                    |
| 백엔드   | Express.js (or Spring Boot 등)            |
| AI 연동 | OpenAI DALL·E API 사용                     |

---

### 🧑‍🤝‍🧑 팀 구성
| 이름      | 역할 요약                                                                         |
| ------- | ----------------------------------------------------------------------------- |
| **김신영** | 프론트엔드 API 구현 및 전체 코드 통합<br/>DALL·E API 연동 및 프롬프팅 설계<br/>GitHub 프론트엔드 리포지토리 관리 |
| **김범준** | 백엔드 API 명세 작성<br/>도서 생성·수정·삭제 구현<br/>CORS 오류 해결<br/>GitHub 백엔드 리포지토리 관리       |
| **김보성** | 백엔드 도서 **조회 기능** 구현 및 전체 코드 통합                                                        |
| **정은지** | 프론트엔드에서 **OpenAI API 연동 코드** 제공                                               |
| **정지원** | 프론트 UI **스케치 및 리팩토링**<br/>도서 **수정·삭제 기능** 구현                                  |
| **홍정희** | 프론트 도서 **생성 및 조회 기능** 구현                                                      |
| **김지현** | 와이어프레임을 기반으로 **프론트 UI 제작**<br/>(Material UI 사용)                               |
| **윤채연** | 전체 프로젝트 **기능 명세서 작성**                                                         |



---

### 🏗️ 디렉토리 구조

```
project-root/
├── frontend/           # React 기반 프론트엔드
│   └── README.md       # 프론트 전용 문서
├── backend/            # Node.js or Spring 기반 백엔드
│   └── README.md       # 백엔드 전용 문서
├── README.md           # ✅ 전체 프로젝트 설명 (이 파일)
```

---

### 🛠️ 기술 스택

| 구분       | 기술                                      |
| -------- | --------------------------------------- |
| Frontend | React, Vite, MUI, Axios                 |
| Backend  | Spring Boot, h2-console or postman       |
| AI API   | OpenAI DALL·E 3 (v1/images/generations) |
| 기타       | RESTful API, JSON, Git, GitHub          |

---

### 🔐 AI 기능 (DALL·E 3 이미지 생성)

* 사용자가 제목과 줄거리를 입력하면, 해당 내용을 바탕으로 **3D 스타일 책 표지 이미지**를 생성
* DALL·E 3 모델을 직접 호출 (`model: "dall-e-3"`)
* 사용자가 입력한 **OpenAI API 키**를 직접 사용 (보안상 서버에 저장 X)
* 생성된 이미지 URL을 도서 데이터에 포함해 저장

---

### 🧪 실행 방법

#### 1. 프론트엔드

```bash
cd frontend
npm install
npm run dev
```

#### 2. 백엔드

```bash
cd backend
npm install
npm run start
```

---

### 📄 하위 README 파일

| 위치                                         | 설명                       |
| ------------------------------------------ | ------------------------ |
| [frontend/README.md](./frontend/README.md) | UI 구조, OpenAI 연동, 사용자 흐름 |
| [backend/README.md](./backend/README.md)   | API 명세, DB 모델, 서버 구성 설명  |

---

### ✅ 프로젝트 특이사항 및 학습 포인트

* **텍스트 기반의 줄거리를 시각적 이미지로 변환**하는 창의적인 AI 사용 경험
* 프롬프트 설계와 결과물 간의 관계를 직접 조정하며 AI 활용 역량 강화
* 프론트/백 완전 분리형 구조와 API 통신 경험
* OpenAI API 키를 직접 입력받는 UX 고려 (보안 vs 편의성)
