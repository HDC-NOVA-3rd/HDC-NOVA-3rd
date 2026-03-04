<div align="center">

# 🏠 NOVA — 스마트 아파트 통합관리 플랫폼

**IoT와 AI를 결합한 차세대 스마트 아파트 통합관리 플랫폼**

입주민 앱과 관리자 웹을 연동하여 주거 환경 제어 및 단지 운영을 효율화하는 올인원 시스템

</div>

---

## 📌 주요 기능

| 기능 | 설명 |
|------|------|
| 🏡 **홈 IoT 제어** | MQTT 기반 LED·FAN 실시간 제어, 온·습도 모니터링, 스케줄·모드 자동화 |
| 🤖 **AI 챗봇 & 음성 비서** | RAG 기반 아파트 수칙 Q&A + "하이 노바" 호출어 음성 제어 (Gemini + Pinecone) |
| 🔥 **화재 감지 자동화** | 가스·온도 센서 → 위험 판정 → 관제 알림 → 시설 자동 차단 |
| 📅 **시설 예약 & QR 출입** | 커뮤니티 시설 예약 + QR 스캔 물리적 출입 통제 + Push 알림 |
| 🏢 **관리자 대시보드** | 세대·민원·관리비 관리, 관제 모니터링 (QueryDSL + Stateless OTP 보안) |
| 📱 **입주민 앱** | OAuth 간편 로그인, 공지사항, 민원 확인, 관리비 고지서 PDF 조회 |

---

## 🛠 Tech Stack

### Frontend & App

![React](https://img.shields.io/badge/React-19.2-61DAFB?logo=react&logoColor=white)
![React Native](https://img.shields.io/badge/React_Native-0.81-61DAFB?logo=react&logoColor=white)
![Expo](https://img.shields.io/badge/Expo-54-000020?logo=expo&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-7.2-646CFF?logo=vite&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5.9-3178C6?logo=typescript&logoColor=white)

### Backend

![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.5.9-6DB33F?logo=springboot&logoColor=white)
![Java](https://img.shields.io/badge/Java-17-ED8B00?logo=openjdk&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?logo=springsecurity&logoColor=white)
![QueryDSL](https://img.shields.io/badge/QueryDSL-5.0-0769AD)
![Swagger](https://img.shields.io/badge/Swagger-OpenAPI-85EA2D?logo=swagger&logoColor=black)

### Database & Real-time

![MariaDB](https://img.shields.io/badge/MariaDB-10.6-003545?logo=mariadb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-7.0-DC382D?logo=redis&logoColor=white)
![Mosquitto](https://img.shields.io/badge/Mosquitto-MQTT-3C5280?logo=eclipsemosquitto&logoColor=white)
![Pinecone](https://img.shields.io/badge/Pinecone-Vector_DB-000000?logo=pinecone&logoColor=white)

### AI & Infra

![Gemini](https://img.shields.io/badge/Google_Gemini-AI-4285F4?logo=googlegemini&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Compose-2496ED?logo=docker&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?logo=grafana&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?logo=nginx&logoColor=white)

---

<!-- ============================================================
  📸 시각화 자료 가이드 (이미지 추가 후 주석 제거)
  ============================================================

  아래 섹션들에 시각화 자료를 추가하세요.
  이미지는 레포 내 docs/images/ 폴더를 만들어 저장하는 것을 권장합니다.

  추천 시각화 자료:
  1. 시스템 아키텍처 다이어그램 (전체 구조도)
  2. 앱 스크린샷 (홈 IoT, 챗봇, 시설 예약 등 주요 화면 3~4장)
  3. 관리자 웹 스크린샷 (대시보드, 민원 관리, 관제 화면 등 2~3장)
  4. 화재 감지 자동화 흐름도
  5. AI 챗봇 파이프라인 다이어그램 (Rule 기반 분기 → LLM/RAG 흐름)
  6. CI/CD 파이프라인 다이어그램
  7. 성능 개선 비교 그래프 (Before/After: 476ms → 53ms)
  8. ERD (Entity-Relationship Diagram)
  9. IoT 하드웨어 구성 사진
  10. 데모 영상 GIF (앱 조작 → IoT 반응)

  이미지 삽입 예시:
  ![시스템 아키텍처](docs/images/architecture.png)
  ![앱 메인화면](docs/images/app-main.png)

  GIF 삽입 예시:
  ![데모](docs/images/demo.gif)
  ============================================================ -->

## 🖼 시스템 아키텍처

> 📍 *시스템 아키텍처 다이어그램을 추가해 주세요.*
>
> 입주민 앱(React Native) → Nginx(HTTPS) → Spring Boot API ↔ MariaDB / Redis / Pinecone
>
> Arduino 센서 → MQTT(Mosquitto) → Spring Boot → 관리자 웹(React) / Push 알림

## 📱 서비스 화면

> 📍 *앱 & 웹 스크린샷을 추가해 주세요.*
>
> | 입주민 앱 | 관리자 웹 |
> |-----------|-----------|
> | 홈 IoT 제어 화면 | 관제 대시보드 |
> | AI 챗봇 화면 | 민원 관리 화면 |
> | 시설 예약 화면 | 관리비 관리 화면 |

---

# 프로젝트 계획서

## 1. 프로젝트 개요

* **프로젝트명**: IoT와 AI를 결합한 스마트 아파트 통합관리 플랫폼 (NOVA)
* **목표**: 입주민 앱과 관리자 웹을 연동하여 주거 환경 제어 및 단지 운영을 효율화하는 올인원 시스템 구축
* **기간**: 2026년 1월 - 2026년 3월

## 2. 프로젝트 일정

* **분석 및 설계**: 1주차 - 요구사항 수집 및 시스템 아키텍처 설계
* **개발**: 2~5주차 - 기능별 스프린트 개발 및 하드웨어(Arduino) 연동
* **테스트 및 배포**: 6주차 - Redis 기반 성능 최적화 및 CI/CD 배포 자동화

---

## 3. 팀 구성

## TEAM 파이브가이즈

| 이름                      | 역할              | GitHub Stats                                                                                                                                         | 주요 담당 업무                                                                                                                                                        |
| ----------------------- | --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **안창석**<br/> | Team Leader         | <a href="https://github.com/AhnCSK"><img src="https://github-readme-stats.vercel.app/api?username=AhnCSK&show_icons=true&theme=default" height="140"/></a> | 🔹 관리자 인증 시스템 및 보안 로직 구현<br/>🔹 민원 및 고지서 관리(PDF/Excel) 구현<br/>🔹 QueryDSL 기반 DB 조회 성능 최적화<br/>🔹 관리자 전용 웹 대시보드 구현<br/>🔹 앱 민원/고지서 확인 구현                         |
| **이희원**                 | AI & Design     | <a href="https://github.com/heewonn09"><img src="https://github-readme-stats.vercel.app/api?username=heewonn09&show_icons=true&theme=default" height="140"/></a> | 🔹 AI 파이프라인 설계 및 총괄 관리<br/>🔹 Gemini, OpenRouter 기반 챗봇 구축<br/>🔹 Pinecone 활용 RAG 파이프라인 구축<br/>🔹 앱 챗봇 UI 구현<br/>🔹 서비스 GUI 및 물리 구조물 설계                          |
| **양준길**                 | Infra & Backend | <a href="https://github.com/wnsrlf0721"><img src="https://github-readme-stats.vercel.app/api?username=wnsrlf0721&show_icons=true&theme=default" height="140"/></a> | 🔹 CI/CD 파이프라인 및 Docker Compose 구축<br/>🔹 JWT 및 OAuth 2.0 기반 로그인 시스템 구현<br/>🔹 시설 예약, QR 출입 시스템, FCM 푸시 알림 구현<br/>🔹 부하 테스트 및 API 성능 병목 개선<br/>🔹 출입 관리 디바이스 구현 |
| **천경신**                 | AI & IoT        | <a href="https://github.com/sthasq"><img src="https://github-readme-stats.vercel.app/api?username=sthasq&show_icons=true&theme=default" height="140"/></a> | 🔹 화재 및 가스 감지 로직 및 MQTT 토픽 총괄 설계 및 브로커 구축<br/>🔹 Hugging Face 기반 음성인식 아키텍처 구현<br/>🔹 안전 관제 대시보드 및 공지사항 웹/앱 기능 개발<br/>🔹 MQTT 디바이스 제어 연동 및 AI 스피커 구현<br/>🔹 웹 인터페이스 디자인      |
| **최우영**                 | IoT & Hardware  | <a href="https://github.com/eddy0417"><img src="https://github-readme-stats.vercel.app/api?username=eddy0417&show_icons=true&theme=default" height="140"/></a> | 🔹 디바이스 상태 API 및 환경 센서 데이터 연동<br/>🔹 사용자 설정 모드 스케줄러(Automation) 구현<br/>🔹 홈/디바이스 제어 UI 및 기능 구현<br/>🔹 IoT 물리 구조물 설계 및 하드웨어 구축<br/>🔹 OpenWeather API 연동         |


# 요구사항 정의서

## 1. 기능적 요구사항

* **사용자 관리**: 관리자 세대 등록 기반 입주민 회원가입 및 OAuth 간편 로그인
* **홈 IoT 제어**: MQTT 기반 실시간 기기 제어(LED, FAN) 및 온·습도 스케줄링
* **커뮤니티 예약**: 시설 예약 알림, QR 스캔을 통한 물리적 출입 통제 연동
* **지능형 인터페이스**: "하이 노바" 호출어 기반 음성 제어 및 RAG 챗봇 연동
* **안전 대응**: 가스/온도 센서 화재 감지 시 관리자 관제 알림 및 시설 자동 차단

## 2. 비기능적 요구사항

* **응답 시간**: 외부 API 호출 구간 Redis 캐싱 적용으로 로그인 응답성 확보
* **성능**: 1,000명 이상의 동시 접속 환경에서 실시간 기기 상태 동기화 유지
* **보안**: 관리자 시스템 접근을 위한 Stateless OTP 및 권한 분리 적용

---

# WBS

## 1. 프로젝트 분석

* 요구사항 수집 및 유즈케이스 정의
* 클라우드 인프라 및 네트워크 토폴로지 설계
* 하드웨어 제어 프로토콜(MQTT) 정의

## 2. 시스템 개발

* **Backend**: Spring Boot 기반 API 서버 및 QueryDSL 검색 최적화
* **Frontend**: React 기반 관리자 대시보드 및 React Native 입주민 전용 앱
* **AI**: Gemini 기반 RAG 파이프라인 및 Whisper STT 음성 비서 구현

## 3. 테스트 및 배포

* **성능 테스트**: k6/JMeter를 활용한 부하 테스트 및 Redis 지표 확인
* **배포**: GitHub Actions를 통한 Docker 이미지 빌드 및 서버 자동 배포
* **모니터링**: Prometheus/Grafana를 활용한 가용성 모니터링 구축

---

# 모델 정의서

## 1. 데이터 모델

* **사용자 정보 (User Entity)**
* `user_id` (PK), `email`, `role` (ADMIN, USER), `apt_unit`


* **기기 제어 (Device Entity)**
* `device_id` (PK), `type`, `current_status`, `target_value`


* **예약 로그 (Reservation Entity)**
* `res_id` (PK), `facility_id`, `user_id`, `qr_hash`



## 2. 객체 모델

* **AI 챗봇 객체**
* 속성: `query_text`, `embedding_vector`, `retrieved_docs`
* 메소드: `searchVectorDB()`, `generateNaturalResponse()`



---

# 성능 평가 결과서

## 1. 테스트 환경

* **인프라**: AWS EC2 c5.large (Docker 가상화)
* **DB**: MariaDB 10.6, Redis 7.0, Pinecone
* **도구**: Grafana Dashboard

## 2. 테스트 결과

* **응답 시간 (p95)**: 외부 날씨 API 지연 문제를 Redis 캐싱으로 극복
* 개선 전: **476ms** → 개선 후: **53ms** (**약 9배 향상**)


* **실시간성**: MQTT 제어 명령 지연 100ms 이내 유지 성공
* **AI 정확도**: RAG 도입 후 아파트 수칙 답변 정확도 95% 달성

## 3. 성능 개선 필요 사항

* 대규모 트래픽 대비 MQTT 클러스터링 구성 필요
* 지속적인 DB 인덱싱 최적화 및 슬로우 쿼리 모니터링

---

# 최종 보고서

## 1. 프로젝트 개요

* **목표**: IoT 실시간 제어와 AI 지능형 상담이 결합된 차세대 스마트 아파트 관리 플랫폼
* **기간**: 2026년 1월 - 2026년 3월

## 2. 주요 성과

* 입주민 앱과 관리자 웹의 실시간 데이터 연동 및 동기화 완성
* STT/TTS 기반 음성 인터페이스 및 RAG 챗봇 서비스 상용 수준 구현
* 화재 센서-알림-시설 차단으로 이어지는 안전 자동화 시나리오 구축

## 3. 향후 개선 사항

* 확장성을 고려한 MSA(Microservices Architecture)로의 점진적 전환
* 입주민 편의를 위한 관리비 자동 정산 및 단지 내 중고거래 기능 추가

---

# 회고

## 1. 잘된 점

* **협업**: Git Flow와 PR 체크리스트를 통해 코드 품질 및 개발 속도 균형 확보
* **최적화**: 데이터 기반으로 병목 지점을 파악하고 Redis로 성능을 직접 개선한 경험

## 2. 개선할 점

* **초기 설계**: 하드웨어 연동 시의 물리적 예외 상황을 설계 단계에서 더 보완할 필요 있음
* **테스트**: 하드웨어 실기기 연동 테스트 시나리오를 더 체계화해야 함

## 3. 교훈

* **명확한 목표**: 사용자 여정(User Journey)을 먼저 정의한 것이 효율적인 개발의 핵심이었음
* **기술 적합성**: 실시간성은 MQTT, 고성능은 Redis 등 문제 해결에 최적인 기술 스택 선정의 중요성 체감

---

# 🚀 Getting Started

## 사전 요구사항

- **Java 17**, **Node.js 20+**, **Docker & Docker Compose**
- **Arduino IDE** (IoT 하드웨어 연동 시)
- **Expo CLI** (`npm install -g expo-cli`) — 모바일 앱 개발 시

## 백엔드 실행

```bash
cd backend
cp src/main/resources/config/secrets.yaml.example src/main/resources/config/secrets.yaml
# secrets.yaml에 API 키 설정 후
./gradlew bootRun
```

## 프론트엔드 (관리자 웹) 실행

```bash
cd frontend
npm install
npm run dev
```

## 모바일 앱 실행

```bash
cd android
npm install
npx expo start
```

## Docker Compose (인프라 전체)

```bash
cd backend/docker
docker-compose up -d
```

---

# 📋 발표 대본 팩트시트 (Fact Sheet)

발표 대본에서 언급된 주요 기술적 주장을 코드베이스 기준으로 검증한 결과입니다.

## ✅ 검증 완료 (코드에서 확인됨)

| # | 발표 내용 | 검증 결과 | 근거 |
|---|----------|----------|------|
| 1 | React 기반 관리자 웹 | ✅ 확인 | `frontend/package.json` — React 19.2 + Vite 7.2 |
| 2 | React Native 입주민 앱 | ✅ 확인 | `android/package.json` — React Native 0.81 + Expo 54 |
| 3 | Spring Boot 백엔드 | ✅ 확인 | `backend/build.gradle` — Spring Boot 3.5.9, Java 17 |
| 4 | QueryDSL 검색 최적화 | ✅ 확인 | `backend/build.gradle` — querydsl-jpa 5.0.0 |
| 5 | Spring Security 보안 | ✅ 확인 | `backend/build.gradle` — spring-boot-starter-security |
| 6 | MQTT (Mosquitto) 실시간 제어 | ✅ 확인 | `backend/docker/docker-compose.yml` — mosquitto 서비스, 포트 1883/9001 |
| 7 | Redis 캐싱 | ✅ 확인 | `backend/build.gradle` + `docker-compose.yml` — Redis Alpine |
| 8 | MariaDB 데이터베이스 | ✅ 확인 | `backend/build.gradle` — mariadb-java-client |
| 9 | Gemini AI 모델 | ✅ 확인 | `backend/build.gradle` — spring-ai-starter-model-google-genai |
| 10 | Pinecone 벡터 DB (RAG) | ✅ 확인 | `backend/.../chat/service/PineconeClient.java` |
| 11 | OAuth 2.0 로그인 | ✅ 확인 | `backend/build.gradle` — spring-boot-starter-oauth2-client |
| 12 | JWT 인증 | ✅ 확인 | `backend/build.gradle` — jjwt 0.12.6 |
| 13 | Stateless OTP 관리자 인증 | ✅ 확인 | `backend/.../auth/otp/StatelessOtpServiceImpl.java` — HmacSHA256, 6자리, 5분 유효 |
| 14 | "하이 노바" Wake Word | ✅ 확인 | `raspberry/voice_assistant/하이-노바_ko_raspberry-pi_v4_0_0/` — Picovoice Porcupine 모델 |
| 15 | QR 출입 시스템 | ✅ 확인 | `android/.../QRCodeModal.tsx` (생성) + `raspberry/facility/qr_cam.py` (스캔) |
| 16 | OpenWeather API 연동 | ✅ 확인 | `backend/.../weather/service/OpenWeatherService.java` |
| 17 | Swagger API 문서 | ✅ 확인 | `backend/build.gradle` — springdoc-openapi 2.8.13 |
| 18 | Docker Compose 배포 | ✅ 확인 | `backend/docker/docker-compose.yml` — 8개 서비스 구성 |
| 19 | Prometheus/Grafana 모니터링 | ✅ 확인 | `docker-compose.yml` — prometheus + grafana + loki + promtail |
| 20 | EAS 모바일 앱 배포 | ✅ 확인 | `android/eas.json` — Expo Application Services 설정 |
| 21 | k6 부하 테스트 | ✅ 확인 | `backend/load-test/` — weather-test.js, reservation-test.js 등 |

## ⚠️ 수정 필요 (발표 대본과 실제 코드 차이)

| # | 발표 내용 | 실제 코드 | 권장 수정 |
|---|----------|----------|----------|
| 1 | "Firebase Push 알림" (슬라이드 #3) | Expo Notifications SDK 사용 (`expo-notifications`), Firebase FCM 직접 사용 아님 | → **"Push 알림"** 또는 **"Expo Push 알림"**으로 수정 |
| 2 | "Whisper STT 모델" (슬라이드 #4) | HuggingFace API를 통한 원격 Whisper 추론 (`openai/whisper-large-v3-turbo`), 로컬 Whisper 아님 | → **"HuggingFace 기반 Whisper STT"**로 수정하면 더 정확 |
| 3 | "GitHub Actions CI/CD" (슬라이드 #11) | `.github/workflows/` 디렉토리 없음, CI/CD 워크플로우 미구성 | → CI/CD 워크플로우 추가 필요 또는 발표에서 **"Docker Compose 기반 배포 자동화"**로 수정 |

## ❓ 검증 불가 (증빙 자료 필요)

| # | 발표 내용 | 비고 |
|---|----------|------|
| 1 | p95 응답시간 476ms → 53ms (9배 개선) | 부하 테스트 스크립트는 존재하나, 결과 데이터가 레포에 없음 → **Grafana 스크린샷 추가 권장** |
| 2 | RAG 도입 후 정확도 95% | 정확도 측정 방법론 및 결과 데이터 없음 → **테스트 결과 문서화 권장** |
| 3 | 1,000명 동시 접속 환경 | 부하 테스트 시나리오에서 확인 필요 → **k6 테스트 결과 리포트 추가 권장** |
| 4 | MQTT 명령 지연 100ms 이내 | 지연 측정 데이터 없음 → **Prometheus 메트릭 스크린샷 추가 권장** |

---










