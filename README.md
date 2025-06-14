# 프로젝트명: BERT Fine-Tuning for Text Classification

## 개요

이 프로젝트는 사전 학습된 BERT 모델을 사용하여 CoLA (Corpus of Linguistic Acceptability) 데이터셋에 대해 문장의 문법적 타당성을 분류하는 텍스트 분류 모델을 학습하는 과정입니다. Jupyter Notebook 하나로 전체 과정이 정리되어 있으며, 토크나이징부터 모델 학습, 평가까지 포함되어 있습니다.

## 주요 내용

* CoLA 데이터셋 다운로드 및 전처리
* BERT tokenizer를 사용한 입력 텐서 구성
* Hugging Face의 'bert-base-uncased' 모델을 사용한 fine-tuning
* AdamW optimizer와 learning rate scheduler 설정
* 학습 루프 구성 (train/validation)
* 평가 지표: accuracy, loss, MCC (Matthew's Correlation Coefficient)

## 환경

* Python 3.x
* PyTorch
* Transformers (Hugging Face)
* Pandas
* 기타: tqdm, numpy 등

## 실행 방법

1. 필요한 패키지를 설치합니다.
    pip install transformers pandas torch wget
2. bert.ipynb 파일을 Jupyter Notebook에서 실행합니다.
3. 각 셀을 순서대로 실행하면서 데이터 전처리 → 모델 구성 → 학습 → 평가 과정을 따라가면 됩니다.

## 결과 요약

* validation accuracy: 약 82%
* validation loss: 약 0.55
* MCC 점수: 약 0.498

## 향후 개선 아이디어

* 다른 데이터셋(GLUE 등)으로 확장
* 하이퍼파라미터 튜닝
* Trainer API 사용으로 학습 로직 간결화
* 모델 저장 및 재사용 기능 추가
* 모델 경량화 시도 (pruning, quantization 등)

### 참고

본 프로젝트는 Hugging Face의 BERT 튜토리얼 및 GLUE benchmark를 참고하여 작성되었습니다.

