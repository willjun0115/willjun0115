# 이력서 (Resume)

<div align="center">

# 이상준 (Sangjun Lee)
### **Edge AI & Industrial AI System Engineer**

[![Email](https://img.shields.io/badge/Email-will115%40kau.kr-blue?style=flat-square&logo=mail.ru)](mailto:will115@kau.kr)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-0A66C2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/sangjun-lee-000885404/?isSelfProfile=true)
[![GitHub](https://img.shields.io/badge/GitHub-willjun0115-181717?style=flat-square&logo=github)](https://github.com/willjun0115)

</div>

---

## 📌 About Me (소개)

> **"하드웨어 제약 환경부터 분산 인프라, 엣지 AI 추론까지 엔드투엔드로 연결하는 엔지니어"**

- **Edge AI & 시스템 엔지니어링 역량**: 마이크로컨트롤러(ESP32) 및 소형 SBC(라즈베리파이) 환경에서의 센서 데이터 수집부터 경량 쿠버네티스(K3s) 기반 고가용성 엣지 클러스터 구축, 연합학습(Federated Learning) 파이프라인 개발까지 전 과정을 주도적으로 구현했습니다.
- **탄탄한 CS 및 통신 기본기**: 4.03/4.5 학점(백분율 95.3%)으로 정보통신공학 전공 지식(네트워크, 분산 시스템, 시스템 프로그래밍, 딥러닝)을 심도 있게 습득했으며, 이를 실제 스마트 팩토리 설비 이상 감지 시스템에 성공적으로 적용했습니다.
- **수치로 증명하는 최적화 집착**: 클라우드 전송 대비 네트워크 지연(RTT)을 **약 2.5배(94μs → 37~39μs) 단축**하고, 분산 가중치 집계를 통해 중앙 대역폭 부하를 획기적으로 경감시키는 등 정량적 성과를 만들어내는 데 강점이 있습니다.

---

## 🎓 Education (학력)

- **한국항공대학교 (Korea Aerospace University)**
  - 학과: AI융합대학 항공전자정보공학부 정보통신공학전공
  - 기간: 2021.03 ~ 2027.02 (졸업예정)
  - **학점: 4.03 / 4.5 (백분율: 95.30 / 100)** *(우수졸업 Magna Cum Laude 요건 충족)*
  - **주요 수강 과목**:
    - **AI / SW**: 딥러닝(A+), 시스템프로그래밍(A+), AI융합 Capstone Design I(A+), 캡스톤디자인 II(A+), SW융합설계(A+), 객체지향프로그래밍(A+), 컴퓨터프로그래밍(A+), 멀티미디어공학(A+), 자료구조(A0)
    - **네트워크 / 하드웨어**: 컴퓨터정보통신망(A+), 데이터통신(A+), 디지털논리회로(A+), 디지털시스템설계(A+), 전자회로실험(A+), 마이크로프로세서(B+)

---

## 🛠 Tech Stack (기술 스택)

| 분야 | 기술 및 도구 |
| :--- | :--- |
| **Edge AI & ML** | **PyTorch** (ARM64 Cross-build), **Flower** (flwr, 연합학습), Hierarchical LSTM Autoencoder, 시계열 이상 탐지, Python, NumPy, Pandas |
| **Edge Infra & DevOps** | **K3s** (경량 쿠버네티스), **containerd**, **MetalLB** (VIP 로드밸런싱), Docker, Linux (Ubuntu 24.04 LTS / Raspbian OS), Bash/Shell Script |
| **IoT & Network Protocols**| **ESP32 MCU**, **Raspberry Pi 4 / 5**, **MQTT**, **TCP/UDP Socket Programming**, ThingsBoard IoT Platform |
| **Database & Tools** | **PostgreSQL**, **SQLite**, Git, GitHub, VS Code, Linux CLI |

---

## 🚀 Key Projects (핵심 프로젝트)

### **FedEdgeFactory : 엣지 클러스터 기반 스마트 팩토리 연합학습 시스템**
*모터 센서 실시간 이상 감지 분산형 AI 인프라 구축*
- **진행 기간**: 2025.09 ~ 2026.06 (한국항공대학교 종합설계 / Capstone Design)
- **수행 역할**: 팀 프로젝트 (시스템 아키텍처 설계, 엣지 클러스터 인프라 구축, 이상 감지 모델 개발)
- **주요 기술**: K3s, MetalLB, ESP32, Raspberry Pi 4/5, PyTorch (ARM64), Flower, ThingsBoard, MQTT, PostgreSQL

#### 1. 문제 정의 및 목표
- 기존 중앙 클라우드 집중형 시스템은 대규모 센서 데이터 전송 시 **대역폭 낭비, 네트워크 지연(Latency), 민감 공정 데이터 보안 취약점**이 발생함.
- 공장 현장(Edge)에서 초저지연으로 이상을 감지하고, 네트워크 장애 시에도 독립 운영 가능한 고가용성(HA) 분산 연합학습 시스템 개발을 목표로 설정.

#### 2. 핵심 수행 내용
- **엣지 인프라 및 네트워크 이중화 로드밸런싱**:
  - Raspberry Pi 4/5 혼합 노드로 K3s 클러스터(Master 1, Worker 4) 구성 및 MetalLB를 통한 고가용성 가상 IP(VIP) 로드밸런싱 구축
  - 노드 장애 시 Pod를 서브 노드로 자동 이관(Failover)하고, 복구 시 원복하는 Self-Healing 파이프라인 자동화
  - PostgreSQL 데이터 실시간 압축 및 대기 노드 동기화 DaemonSet 에이전트(`tb_backup.py`) 구현으로 무중단 서비스 체계 완성
- **시계열 이상 탐지 AI 모델 및 연합학습(FL) 파이프라인**:
  - AI HUB 대전시 기계시설물 시계열 데이터(233만 건) 활용
  - 공통 Encoder(특징 추출)와 노드별 Decoder(복원)로 분리된 **Hierarchical LSTM Autoencoder** 모델 설계
  - ARM64 환경에 최적화된 PyTorch 크로스빌드 및 **Flower (FedAvg)** 프레임워크 기반 분산 가중치 집계 파이프라인 구축
  - 설비별 노이즈 및 동적 부하 변동에 강인한 동적 임계값(`Threshold = Mean + 0.8σ`) 로직 적용
- **IoT 엔드포인트 수집 및 파이프라인 연동**:
  - ESP32 MCU 기반 가상 스마트 플러그 노드(8대)에서 실시간 전력 데이터 생성 및 MQTT(Port 1883) 전송
  - ThingsBoard 플랫폼 대시보드 시각화 및 TCP Socket(Port 5005) 기반 실시간 추론 스트리밍 파이프라인 구축

#### 3. 정량적 성과 및 기대효과
- **지연 시간 2.5배 단축**: Cloud Only 구조 대비 RTT 지연 시간을 **약 2.4~2.5배 단축** (94μs → 37~39μs)
- **트래픽 및 비용 절감**: 원시 데이터 대신 주기적 가중치만 전송하여 클라우드 네트워크 부하 $R/t$배 경감 및 처리량 $M/N$배 축소
- **Fail-Safe 보장**: 외부 인터넷 단절 상황에서도 현장 로컬 클러스터 내에서 즉각적인 이상 제어권 유지

---

## 🏆 Honors & Activities (수상 및 대외활동)

- **2025 Boeing Day 교내 학술대회 1등 수상**
  - 주최: 한국항공대학교 / 보잉(Boeing)
  - 수상 일자: 2025년 11월
- **NASA-BOEING 글로벌 탐방 프로그램 이수**
  - 주관: 한국항공대학교 국제교류처
  - 기간: 2026.01.12 ~ 2026.01.16 (이수증 발급: 2026.02.11)
  - 내용: 미국 항공우주국(NASA) 및 보잉(Boeing) 본사/생산기지 현장 탐방을 통한 글로벌 항공우주 및 시스템 엔지니어링 첨단 기술 분석

---

## 📜 Certificates (자격증)

- **한국사능력검정시험 2급** (국사편찬위원회 / 2024.08.22)
- **OPIc IM1** (ACTFL / 2026.09)
