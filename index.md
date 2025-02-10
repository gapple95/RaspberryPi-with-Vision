# 라즈베리파이 4 Vision AI 강의 커리큘럼

## 1. 강의 개요 및 준비 (Introduction & Setup)
### 1.1 라즈베리파이 개요 및 Vision AI 적용 사례
- 라즈베리파이의 특징과 활용 분야
- Vision AI가 적용될 수 있는 실제 사례 분석

### [실습 1] 라즈베리파이 설정 및 환경 구축
- Raspberry Pi OS 설치 및 초기 설정 (Wi-Fi, SSH, VNC 설정)
- Python, OpenCV, TensorFlow Lite 설치
- 라즈베리파이 카메라 모듈 활성화 및 테스트

## 2. OpenCV를 활용한 기본 Vision AI 구현
### 2.1 OpenCV 기초 및 이미지 처리 개념
- OpenCV의 역할과 기본 기능
- 영상 처리의 핵심 개념 (필터링, 엣지 검출 등)

### [실습 2] OpenCV로 실시간 카메라 스트리밍
- OpenCV를 이용해 카메라에서 실시간 영상 출력
- 이미지 필터 적용 (GrayScale, Canny Edge Detection)
- 라즈베리파이에서 프레임 속도 확인 및 최적화

### 2.2 얼굴 인식 기술 개요
- 얼굴 검출과 인식의 원리
- 다양한 얼굴 인식 알고리즘 (Haar Cascade, DNN)

### [실습 3] 얼굴 인식 시스템 만들기
- Haar Cascade를 활용한 얼굴 감지
- OpenCV DNN을 활용한 실시간 얼굴 인식
- 카메라로 얼굴을 인식하면 박스를 그리는 기능 추가

## 3. TensorFlow Lite를 활용한 AI 모델 배포
### 3.1 TensorFlow Lite 개요 및 모델 변환
- TensorFlow Lite의 개념과 동작 방식
- Pre-trained 모델을 변환하여 활용하기

### [실습 4] TensorFlow Lite 모델 실행하기
- TFLite MobileNet 모델을 다운로드하고 변환
- 이미지 입력 및 객체 분류 결과 출력
- Raspberry Pi에서 MobileNet 속도 테스트

### 3.2 실시간 객체 탐지 개념
- 객체 탐지 모델의 원리 및 활용 방법
- MobileNet SSD vs YOLO 비교

### [실습 5] 실시간 객체 탐지 모델 적용
- COCO Dataset 기반 MobileNet SSD 모델 실행
- 카메라 영상을 실시간으로 분석하고 객체 감지
- 감지된 객체에 따라 특정 액션 실행 (예: 사람 감지 시 LED 켜기, 비프음 or 특정 소리 내기)

## 4. YOLO를 활용한 실시간 객체 탐지
### 4.1 YOLO 개념 및 경량화 모델 적용
- YOLO 모델의 원리와 작동 방식
- Tiny 모델과 Nano 모델의 차이점

### [실습 6] YOLOv5-Nano 모델 변환 및 실행
- YOLOv5 Nano 모델을 TFLite로 변환
- ONNX에서 TFLite 변환 후 라즈베리파이에서 실행
- YOLO를 이용해 실시간 카메라 객체 탐지

### 4.2 Edge TPU 가속 적용
- Google Coral Edge TPU의 개념과 장점
- TPU와 CPU/GPU 비교

### [실습 7] Edge TPU 가속 적용
- Google Coral Edge TPU를 연결하고 속도 테스트
- YOLO 및 MobileNet 모델을 Edge TPU에서 실행
- 속도 비교 및 최적화 방법 확인

## 5. 라즈베리파이를 활용한 AI IoT 프로젝트
### 5.1 AI 기반 IoT 프로젝트 개요
- IoT와 AI를 결합한 사례 분석
- AIoT의 핵심 기술

### [실습 8] AI 기반 스마트 감시 시스템 구축
- OpenCV + TensorFlow Lite로 침입자 감지 시스템 개발
- 특정 객체(사람) 감지 시 이메일/SMS 알림 전송
- 감지된 객체를 저장하고 로그 관리

### 5.2 OCR 기술 개요 및 활용 사례
- OCR 기술의 동작 방식과 응용 사례
- 번호판 인식 시스템의 원리

### [실습 9] OCR을 활용한 번호판 인식
- OpenCV와 Tesseract OCR을 활용해 차량 번호판 인식
- YOLO 모델과 결합하여 번호판 추출 후 문자 인식
- 인식된 번호판 정보를 파일로 저장

## 6. 실전 프로젝트 (AI 모델 배포 및 활용)
### 6.1 Flask 기반 AI 서비스 개요
- Flask를 활용한 웹 기반 AI 서비스 구축 방법
- AI 모델을 API 형태로 배포하는 방법

### [실습 10] Flask 기반 AI 웹 서비스 구축
- Flask + OpenCV로 AI API 만들기
- 웹 브라우저에서 실시간 카메라 스트리밍 및 객체 탐지 실행
- API로 실시간 Vision AI 데이터를 전달

### 6.2 실시간 데이터 스트리밍 개념 및 활용
- 실시간 데이터 처리의 개념과 필요성
- Kafka를 활용한 데이터 스트리밍 사례

### [실습 11] 실시간 데이터 스트리밍 (Kafka + 클라우드 연동)
- Kafka를 활용하여 실시간 객체 탐지 데이터 전송
- Google Cloud / AWS IoT와 연동하여 AI 데이터를 클라우드에 저장
- 실시간 스트리밍 대시보드 만들기

## 최종 목표
- 라즈베리파이에서 AI 모델을 직접 실행하며 학습
- OpenCV, TensorFlow Lite, YOLO 등을 실습을 통해 익히기
- IoT 및 클라우드와 연계된 AI 프로젝트 경험하기
- 최적화된 AI 시스템을 구현하여 실전 활용 가능하도록 학습
