# 🏥 Hansol AI-powered Medical Operations System

> AI 기술과 클라우드 인프라 기반 무중단 스마트 병원 ERP 플랫폼

<br>

## 📌 프로젝트 소개

LangChain + OpenAI API 기반 AI 자동 근무 스케줄 생성과 클라우드 인프라를 적용한 스마트 병원 ERP 플랫폼입니다.  
Docker + Jenkins CI/CD 파이프라인과 AWS EKS 기반 무중단 배포를 구축하였습니다.

- **기간** : 2026.03 ~ 2026.05
- **역할** : 팀원 · 분석/개발 (팀 프로젝트)
- **Repository** :
  - Backend (Spring) : [final_spring](https://github.com/novolunteer/final_spring)
  - Frontend (React) : [final_react](https://github.com/novolunteer/final_react)
  - AI Server (Python) : [final_python](https://github.com/novolunteer/final_python)

<br>

## 🛠 기술 스택

| 분류 | 기술 |
|------|------|
| Backend | Java, Spring Boot, Spring Security, JWT, JPA |
| Frontend | React, JavaScript, TailwindCSS |
| AI | Python, FastAPI, LangChain, OpenAI API |
| Database | MySQL, Redis, Elasticsearch |
| Infra | Docker, Jenkins, Kubernetes, AWS (EC2 · RDS · EKS · S3 · CloudWatch) |

<br>

## 👩‍💻 담당 기능

| 기능 | 설명 |
|------|------|
| AI 근무 스케줄 생성 | LangChain + OpenAI API + FastAPI 연동, 과별 지침 기반 자동 스케줄 생성 |
| 인사관리 | 직원·부서 CRUD, Spring Security + JWT 역할별 이중 권한 처리 |
| React 공통 레이아웃 | 공통 레이아웃 및 라우팅 설계, 근무·수술 스케줄 UI 구현 |
| CI/CD 파이프라인 | Docker + Jenkins 파이프라인 구축, 무중단 배포 자동화 |
| AWS 인프라 | CloudWatch 리소스 모니터링 및 알림 설정, EKS 클러스터 구성 |
| DB 설계 | 전체 DB 설계 및 ERD 작성, MySQL · Redis · Elasticsearch 연동 |

<br>

## 🔍 주요 구현 상세

### 1. AI 자동 근무 스케줄 생성

LangChain + OpenAI API를 FastAPI 서버와 연동하여 부서별 지침을 기반으로 AI가 자동으로 근무 스케줄을 생성합니다.  
Spring Boot에서 FastAPI로 요청을 전달하고 결과를 받아 DB에 저장합니다.

<img src="https://github.com/user-attachments/assets/18253c94-b8d0-463d-b862-afcdb1a731a8" width="700">

<img src="https://github.com/user-attachments/assets/4807bacc-2910-4e17-afaf-2d3fa2a17800" width="700">

<br>

### 2. Docker + Jenkins CI/CD 파이프라인

Docker 이미지 빌드 → ECR 푸시 → EKS 배포까지 Jenkins 파이프라인으로 자동화하였습니다.  
GitHub Actions(Frontend)와 Jenkins(Backend) 이중 CI/CD 파이프라인을 구성하였습니다.

**Jenkins**

<img src="https://github.com/user-attachments/assets/51b2a9c3-6ec5-470e-8e68-86ad6bdf064a" width="300">

**GitHub Actions**

<img src="https://github.com/user-attachments/assets/7bcf0318-6b01-452e-b8a0-9338f61d1832" width="700">

<br>

### 3. AWS CloudWatch 모니터링

EC2 인스턴스(app, bastion, elasticsearch, jenkins, redis)의 CPUUtilization을  
CloudWatch 커스텀 대시보드에 통합하여 실시간 리소스 모니터링 및 알림을 구성하였습니다.

<img src="https://github.com/user-attachments/assets/a80b046c-717b-4b18-a283-4ec0b867bfdf" width="700">

<br>

## 📊 ERD

**사용자 / 인증 / 직원 / 부서**

<img src="https://github.com/user-attachments/assets/0d2d0317-1c2d-4b15-b01e-02f2bf91b4a0" width="700">

**진료 / 예약 / 수술 / 접수 / 수납**

<img src="https://github.com/user-attachments/assets/df3c3bd1-576e-4f3c-a5e3-18d2d6de086d" width="500">

**근무일정 / 채팅**

<img src="https://github.com/user-attachments/assets/7fc79ef6-df9e-4c3c-87e0-9db0b10f7146" width="700">

<br>

## 🏗 시스템 아키텍처

<img src="https://github.com/user-attachments/assets/c7844236-9cc4-49f2-8048-13cd69c11a50" width="700">

<br>

## ☁ AWS 아키텍처

<img src="https://github.com/user-attachments/assets/d778a5da-3ce0-4b4e-8fca-f2fcc72fb9f5" width="700">
