# 이력서 (Resume)

<div align="center">

# 이상준 (Sangjun Lee)
### **Edge AI & Industrial Systems Engineer**

[![Email](https://img.shields.io/badge/Email-will115%40kau.kr-blue?style=flat-square&logo=mail.ru)](mailto:will115@kau.kr)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-0A66C2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/sangjun-lee-000885404/?isSelfProfile=true)
[![GitHub](https://img.shields.io/badge/GitHub-willjun0115-181717?style=flat-square&logo=github)](https://github.com/willjun0115)

</div>

---

## 📌 About Me (소개)

> **"하드웨어 제약 환경부터 분산 인프라, 엣지 AI 추론 및 센서 통신까지 엔드투엔드로 연결하는 엔지니어"**

- **Edge AI & 분산 시스템 엔지니어링**: 마이크로컨트롤러(ESP32) 및 임베디드 SBC(라즈베리파이) 기반 데이터 파이프라인부터 경량 쿠버네티스(K3s) 고가용성 엣지 클러스터, 연합학습(Federated Learning) 인프라까지 전 과정을 설계·구축한 경험이 있습니다.
- **센서 융합 및 산업용 무선 프로토콜 설계**: 헬리콥터 수상 비행 안전을 위한 UWB AoA 기반 초정밀 거리·고도 측정 시스템(AC/DC)으로 **2025 Boeing Day 학술대회 1등**을 수상하는 등 현장 중심의 공학적 문제 해결력을 증명했습니다.
- **탄탄한 CS 및 컴퓨터통신 기초 체력**: **전체 평점 4.03 / 4.5 (백분율 95.3%, 우수졸업 Magna Cum Laude 요건 충족)**로 딥러닝, 분산망, 시스템프로그래밍 등 정보통신공학 전공 코어 과목에서 최상위권 성취도를 유지해 왔습니다.
- **수치로 증명하는 성능 최적화 집착**: 클라우드 전송 대비 RTT 지연 시간을 **약 2.5배(94μs → 37~39μs) 단축**하고, ViT/ConvNeXt 이기종 앙상블을 통한 분류 정확도 극대화, PostgreSQL 백업 데몬셋 설계 등 정량적 성과 창출에 집중합니다.

---

## 🎓 Education (학력)

- **한국항공대학교 (Korea Aerospace University)**
  - **학부/전공**: AI융합대학 항공전자정보공학부 정보통신공학전공
  - **재학 기간**: 2021.03 ~ 2027.02 (졸업예정)
  - **학점**: **4.03 / 4.5** (총 122학점 취득 / 백분율: **95.30 / 100**) *(우수졸업 Magna Cum Laude 요건 충족)*
  - **주요 전공 수강 이력**:
    - **AI / SW**: 딥러닝(A+), 시스템프로그래밍(A+), AI융합 Capstone Design I(A+), 캡스톤디자인 II(A+), SW융합설계(A+), 객체지향프로그래밍(A+), 컴퓨터프로그래밍(A+), 멀티미디어공학(A+), 자료구조(A0), 컴퓨팅적사고와문제해결(A+)
    - **네트워크 / 하드웨어**: 컴퓨터정보통신망(A+), 데이터통신(A+), 디지털논리회로(A+), 디지털시스템설계(A+), 기초회로및디지털실험(A+), 전자회로실험(A+), 마이크로프로세서(B+)

---

## 🛠 Tech Stack (기술 스택)

| 분야 | 기술 및 도구 |
| :--- | :--- |
| **Edge AI & Computer Vision** | **PyTorch** (ARM64 Cross-build), **Flower** (flwr, 연합학습), Hierarchical LSTM Autoencoder, ConvNeXt, ViT (EVA02, DeiT3), OpenCV, NumPy, Scikit-learn |
| **Edge Infra & Orchestration** | **K3s** (경량 쿠버네티스), **containerd**, **MetalLB** (VIP 로드밸런싱/Failover), Docker, Linux (Ubuntu 24.04 LTS / Raspbian OS), Shell Scripting |
| **IoT, Wireless & Embedded** | **ESP32 MCU**, **Raspberry Pi 4 / 5**, **UWB / AoA**, **MQTT**, **TCP/UDP Socket Programming**, ThingsBoard IoT Platform |
| **Backend & Database** | **PostgreSQL**, **MySQL**, **Apache Tomcat**, JSP, SQLite |
| **Tools & Collaboration** | Git, GitHub, VS Code, Linux CLI, PowerPoint (기술 제안서) |

---

## 🚀 Key Projects (핵심 프로젝트)

### 1. FedEdgeFactory : 엣지 클러스터 기반 스마트 팩토리 연합학습 시스템
*모터 센서 실시간 이상 감지 및 무중단 고가용성 분산 AI 인프라 구축*
- **진행 기간**: 2025.09 ~ 2026.06 (한국항공대학교 종합설계 / Capstone Design)
- **수행 역할**: 팀 프로젝트 (시스템 아키텍처 설계, 엣지 클러스터 인프라 구축, 이상 감지 모델 개발)
- **핵심 기술**: K3s, MetalLB, containerd, ESP32, Raspberry Pi 4/5, PyTorch, Flower, ThingsBoard, MQTT, PostgreSQL

#### 문제 정의 및 개발 목표
- 기존 중앙 클라우드 전송 방식은 **대규모 센서 데이터 전송에 따른 네트워크 대역폭 낭비, 물리적 RTT 지연, 공정 데이터 보안 노출** 문제 발생.
- 공장 현장(Edge)에서 밀리초 단위 초저지연으로 모터 설비 이상을 감지하고, 네트워크 단절 시에도 자체 작동하는 고가용성(HA) 연합학습 엣지 클러스터 개발.

#### 핵심 구현 내용
- **고가용성 K3s 엣지 클러스터 및 네트워크 이중화**:
  - Raspberry Pi 4/5 혼합 노드 환경에서 K3s 클러스터(Master 1, Worker 4) 구축 및 MetalLB 기반 가상 IP(VIP) 로드밸런싱 구성.
  - Pod 비정상 종료 시 워커 노드로 자동 이관(Failover) 및 노드 재가동 시 원복되는 Self-Healing 자동화 파이프라인 수립.
  - PostgreSQL 데이터 실시간 압축 및 대기 노드 동기화 DaemonSet 에이전트(`tb_backup.py`) 구현으로 단일 장애점(SPOF) 원천 배제.
- **계층형 LSTM Autoencoder 및 연합학습(FL) 파이프라인**:
  - AI HUB 대전시 기계시설물 시계열 데이터(233만 건) 활용.
  - 글로벌 특징을 추출하는 공통 Encoder와 노드별 특화 복원을 담당하는 개별 Decoder 구조의 **Hierarchical LSTM Autoencoder** 모델 설계.
  - ARM64 환경 최적화 PyTorch 크로스빌드 및 **Flower (FedAvg)** 기반 분산 가중치 집계 파이프라인 구축.
  - 장비별 노이즈 및 동적 부하 변동에 강인한 동적 임계치(`Threshold = Mean + 0.8σ`) 알고리즘 적용.
- **IoT 엔드포인트 수집 및 파이프라인 연동**:
  - ESP32 MCU 기반 스마트 플러그 노드(8대)에서 실시간 전력 데이터 생성 및 MQTT(Port 1883) 전송.
  - ThingsBoard 대시보드 실시간 관제 및 TCP 소켓 기반 실시간 추론 스트리밍 구축.

#### 정량적 성과
- **RTT 지연 시간 2.5배 단축**: Cloud 전송 대비 지연 시간을 **약 2.4~2.5배 단축** (94μs → 37~39μs).
- **중앙 네트워크 부하 경감**: 원시 센서 데이터 대신 주기적 가중치만 전송하여 클라우드 네트워크 부하 $R/t$배 경감 및 처리량 $O(N) \rightarrow O(M)$ 단축.
- **현장 독립 Fail-Safe 검증**: 외부 인터넷망 완전 단절 테스트 환경에서도 현장 로컬 클러스터 내부에서 즉각적인 모터 제어권 유지.

---

### 2. UWB AoA 기반 헬리콥터 정밀 거리·고도 측정 시스템
*해상/담수 작업 시 기존 센서 한계를 극복하는 투하형 센서 볼 및 무선 측위 시스템*
- **진행 기간**: 2025.10 ~ 2025.11 (2025 Boeing Day 학술대회 **1등 수상작**)
- **수행 역할**: 팀 프로젝트 (시스템 아키텍처 제안, 무선 측위 및 센서 융합 알고리즘 설계, 기술 제안서 작성 및 발표)
- **핵심 기술**: UWB (Ultra-Wideband), AoA (Angle of Arrival), Gyroscope Sensor Fusion, System Engineering

#### 문제 정의 및 개발 목표
- 헬리콥터의 산불 진화 담수(Water Pickup) 및 해상 인명 구조 시, 수면 반사로 인한 **LiDAR 오차**, 도플러 효과로 인한 **RADAR 왜곡**, 로터 하강풍(Downwash)과 습도로 인한 **기압고도계 신뢰성 저하**로 치명적 추락 사고 빈발.
- 가혹한 수면 환경에서도 센티미터 단위의 정밀한 고도 및 거리를 실시간으로 산출할 수 있는 차세대 무선 측위 시스템 고안.

#### 핵심 구현 내용
- **수면 투하형 센서 볼(Hy-Ball) & UWB AoA 메커니즘**:
  - 헬기에서 수면으로 투하되는 센서 볼(Hy-Ball)과 기체 간의 초광대역(UWB) 신호 비행시간(ToF)을 통해 정밀 직선 거리($d$) 측정.
  - 다중 안테나 위상차(Phase Difference) 기반 **AoA(도착각)** 기법을 결합하여 기체 기준 볼의 앙각(Elevation Angle, $\theta$)을 실시간 추정.
- **자이로스코프 기반 기체 자세 보정 알고리즘**:
  - 기체의 롤(Roll), 피치(Pitch) 흔들림으로 인한 각도 왜곡을 실시간 자이로 센서 데이터와 융합 보정하여 절대 수직 고도($h = d \cdot \sin(\theta_{corrected})$) 도출.
- **체계적 시스템 엔지니어링 및 안전성 시나리오 수립**:
  - 센서 볼 투하 → UWB 페어링 → 실시간 고도 추정 → 안전 담수/철수 4단계 운영 시나리오 및 통신 페일세이프 구조 정립.

#### 주요 성과
- **2025 Boeing Day 교내 학술대회 1등 수상** (보잉 및 한국항공대학교 주관).
- 글로벌 항공우주 기업 심사위원단으로부터 실현 가능성과 산업 현장 안전성 개선 효과에서 최고 점수 획득.

---

### 3. CIFAR-100 Vision Architecture 벤치마킹 및 앙상블 시스템
*제한된 컴퓨팅 환경에서 최신 CNN vs. ViT 모델 비교 분석 및 가중합 앙상블 파이프라인*
- **진행 기간**: 2026.04 ~ 2026.06 (딥러닝 텀프로젝트)
- **수행 역할**: 팀 프로젝트 (모델 실험 파이프라인 구축, 성능/연산량 벤치마크, 앙상블 전략 수립)
- **핵심 기술**: PyTorch, ConvNeXt, ViT (EVA02, DeiT3, MaxViT), Data Augmentation, Ensemble

#### 핵심 구현 및 분석 내용
- **최신 비전 백본 아키텍처별 특성 비교 실험**:
  - CNN 기반(ConvNeXt), Attention 기반(EVA02, DeiT3), 하이브리드(MaxViT)를 모델 스케일(Tiny, Small, Base, Large)별로 동일 환경에서 체계적 비교.
  - 32x32 저해상도 이미지 특성상 패치 분할 시 공간 세부 정보가 손실되는 ViT의 한계와, 로컬 수용영역(Receptive Field)을 보존하는 ConvNeXt의 특성을 실험적으로 규명.
- **이기종 모델 가중합 앙상블(Weighted Ensemble)**:
  - 단일 모델 최고 성능(ConvNeXt-Large 95.24%, DeiT3-Large 95.10%)을 기반으로, CNN의 지역적 특징과 ViT의 전역적 문맥 정보를 상호 보완하는 가중합 앙상블 기법 설계.
  - 모델별 추론 신뢰도 기반 가중치 튜닝을 통해 일반화 성능 향상 및 오분류율 대폭 저감.

---

### 4. 실시간 주식 정보 및 모의 투자 HTS 웹 서비스
*분산 데이터베이스 및 비동기 인터페이스 기반 실시간 금융 모의 거래 시스템*
- **진행 기간**: 2025.09 ~ 2025.12 (SW융합설계 텀프로젝트)
- **수행 역할**: 팀 프로젝트 (시스템 아키텍처 설계, 분산 DB 스키마 구축, 서버 비즈니스 로직 개발)
- **핵심 기술**: Linux (Ubuntu), Apache Tomcat 8, JSP, Java, MySQL, ApexCharts, JavaScript

#### 핵심 구현 내용
- **기능별 DB 분리 아키텍처 설계**:
  - 데이터 결합도를 낮추고 동시 처리 성능을 확보하기 위해 사용자(UserDB), 시세(StockDB), 거래(TradeDB)로 데이터베이스 스키마를 분리 설계.
- **실시간 주가 차트 및 비동기 거래 체결 로직**:
  - ApexCharts 라이브러리를 연동하여 캔들스틱(시가/고가/저가/종가) 실시간 시각화 구현.
  - 세션 기반 사용자 인증 및 가상 주문 트랜잭션의 정합성을 보장하는 체결 비즈니스 로직 작성.

---

## 🏆 Honors & Activities (수상 및 대외활동)

- **2025 Boeing Day 교내 학술대회 1등 (최우수상)**
  - 주최: 한국항공대학교 / 보잉 (The Boeing Company)
  - 수상 일자: 2025.11
  - 내용: UWB AoA 및 센서 볼을 결합한 헬리콥터 정밀 거리·고도 측정 시스템 제안 및 1위 수상
- **2025 동계 NASA-BOEING 글로벌 탐방 프로그램 이수**
  - 주관: 한국항공대학교 국제교류처
  - 기간: 2026.01.12 ~ 2026.01.16 (이수증 발급: 2026.02.11)
  - 내용: 미국 항공우주국(NASA) 및 보잉(Boeing) 본사/생산기지 현장 탐방을 통한 최첨단 우주항공 시스템 엔지니어링, 안전 공학 및 글로벌 테크 트렌드 분석

---

## 📜 Certificates & Languages (자격증 및 어학)

- **OPIc IM1** (ACTFL / 2026.09)
- **한국사능력검정시험 2급** (국사편찬위원회 / 2024.08.22)

