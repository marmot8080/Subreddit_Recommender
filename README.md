# Subreddit_Recommender

사용자가 입력한 글(Title, Body)을 분석하여, 해당 글을 올리기에 가장 적절한 **서브레딧(Subreddit)을 추천해주는 NLP 모델**입니다.
Reddit의 방대한 커뮤니티 생태계에서 사용자가 자신의 관심사에 맞는 서브레딧을 쉽게 찾을 수 있도록 돕는 것을 목표로 합니다.

## Key Features (핵심 기능)

### 1. Text Preprocessing (텍스트 전처리)
* **Cleaning:** url 제거, 특수문자 및 불용어(Stopwords) 제거.
* **Normalization:** 텍스트 소문자 변환, 표제어 추출(Lemmatization) 등을 통해 노이즈 감소.

### 2. Feature Extraction & Modeling
* **Vectorization:** 입력된 텍스트를 모델이 이해할 수 있도록 벡터화 수행.
    * *Method:* TF-IDF
* **Classification Model:** 다중 클래스 분류(Multi-class Classification) 모델을 사용하여 서브레딧 확률 예측.
    * *Model:* Logistic Regression

### 3. Top-N Recommendation
* 모델이 예측한 확률값을 바탕으로, 가장 적합한 **상위 N개**의 서브레딧을 추천합니다.

---

## Dataset

[Reddit API 호출](https://github.com/marmot8080/Reddit_API)을 통해 데이터를 수집할 수 있습니다.
수집된 데이터셋은 [여기](https://drive.google.com/file/d/1XETBbqQW-ZJT3fW5rXYcV65aoLgGxX-5/view?usp=sharing)에서 다운받을 수 있습니다.

---

## Environment (개발 환경)

* **Language:** Python 3.13.5

---

## Usage (실행 방법)

### 1. 패키지 설치
필요한 라이브러리를 설치합니다.
```bash
pip install -r requirements.txt
```
