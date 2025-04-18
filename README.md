# BitcoinPricePrediction
## 👥 Team Members
<table>
  <tr align="center">
    <td width="150px">
      <a href="https://github.com/isshoman123" target="_blank">
        <img src="https://avatars.githubusercontent.com/isshoman123" alt="isshoman123" />
      </a>
    </td>
    <td width="150px">
      <a href="https://github.com/dongsinwoo" target="_blank">
        <img src="https://avatars.githubusercontent.com/dongsinwoo" alt="dongsinwoo" />
      </a>
    </td>
    <td width="150px">
      <a href="https://github.com/espada105" target="_blank">
        <img src="https://avatars.githubusercontent.com/espada105" alt="espada105" />
      </a>
    </td>
  </tr>
  <tr align="center">
    <td>
      김재원
    </td>
    <td>
      신동우
    </td>
      <td>
      홍성인
    </td>
  </tr>
</table>

# Claude 3.7 Sonnet

### 주요 기능

- **데이터 통합**: OHLCV(시가, 고가, 저가, 종가, 거래량) 데이터와 공포 & 탐욕 지수 및 시가총액 지표 결합
- **기술적 지표**: RSI, MACD, 볼린저 밴드 등 15개 이상의 기술적 지표 계산
- **하이브리드 딥러닝**: 최적의 시계열 예측을 위해 GRU와 LSTM 네트워크 결합
- **하이퍼파라미터 최적화**: 최적의 모델 구성을 위한 단계적 튜닝 구현
- **종합적 평가**: 기본 RMSE를 넘어선 다양한 지표를 활용한 모델 평가
- **방향성 예측**: 절대 값뿐만 아니라 가격 움직임 방향 정확도에 중점
- **시각화**: 모델 성능 및 예측 분석을 위한 광범위한 시각화 도구 제공

### 프로젝트 구조

- **데이터 처리**: 데이터 로드, 전처리 및 특성 엔지니어링을 위한 함수
- **모델 구축**: 하이브리드 GRU+LSTM 아키텍처 정의
- **훈련 & 튜닝**: 훈련 및 하이퍼파라미터 최적화 구현
- **평가**: 종합적인 평가 지표 및 시각화 도구
- **예측**: 미래 가격 예측을 위한 함수

### 데이터 파이프라인

1. **데이터 수집**:
   - Yahoo Finance에서 비트코인 가격 역사 데이터
   - alternative.me API에서 공포 & 탐욕 지수
   - 유통 공급량 기반 시가총액 추정

2. **특성 엔지니어링**:
   - 기술적 지표(RSI, MACD, 볼린저 밴드 등)
   - 시간적 특성(요일, 월, 분기)
   - 가격 모멘텀 특성(1일, 7일, 30일 수익률)
   - 변동성 지표(30일 표준편차)

3. **데이터 전처리**:
   - 누락된 값 처리
   - 이상치 처리
   - MinMaxScaler를 사용한 특성 스케일링
   - 시계열 모델을 위한 시퀀스 생성

### 모델 아키텍처
#### 하이브리드 딥러닝 모델
- **GRU 계층**: 효율적인 계산으로 단기 패턴 포착
- **LSTM 계층**: 가격 데이터의 장기 의존성 모델링
- **배치 정규화**: 훈련 안정성과 수렴성 개선
- **드롭아웃 계층**: 과적합 방지
- **완전 연결 계층**: 최종 회귀 출력

### 하이퍼파라미터 튜닝

1. **초기 탐색**: 주요 아키텍처 결정에 대한 빠른 평가
2. **미세 조정**: 최상의 초기 구성 주변에 대한 세부 검색

튜닝된 주요 하이퍼파라미터
- GRU 유닛: 32, 64, 128
- LSTM 유닛: 64, 128, 256
- 드롭아웃 비율: 0.2, 0.3, 0.4
- 학습률: 0.001, 0.0005, 0.0001
- 배치 크기: 16, 32, 64
- 옵티마이저: Adam, RMSprop

### 평가 지표

1. **기본 정확도 지표**:
   - RMSE (Root Mean Squared Error)
   - MAE (Mean Absolute Error)
   - MAPE (Mean Absolute Percentage Error)
   - R² (결정 계수)

2. **방향성 정확도**:
   - 전체 방향 정확도(상승/하락 움직임)
   - 상승 움직임 정확도
   - 하락 움직임 정확도

3. **고급 지표**:
   - Theil의 U 통계량(단순 예측과 비교)
   - 복합 점수 시스템(여러 지표에 걸쳐 0-5 척도)

### 시각화

1. **시계열 플롯**:
   - 실제 vs. 예측 가격
   - 시간 경과에 따른 잔차 분석

2. **산점도 분석**:
   - 실제 vs. 예측 산점도와 회귀선
   - 변동성 vs. 오차 상관관계

3. **오차 분석**:
   - 잔차 분포 히스토그램
   - 잔차의 자기상관 함수 플롯

4. **미래 예측**:
   - 과거 가격 및 미래 예측 시각화
   - 불확실성 범위(선택적)

### 필요 라이브러리

- Python 3.8+
- TensorFlow 2.x
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- yfinance
- ta (기술 분석 라이브러리)
- statsmodels

# ChatGPT
### 주요 기능
- **데이터 통합**: 
- **기술적 지표**:
- **하이브리드 딥러닝**:
- **하이퍼파라미터 최적화**:
- **종합적 평가**:
- **방향성 예측**:
- **시각화**:

### 프로젝트 구조

- **데이터 처리**: 
- **모델 구축**: 
- **훈련 & 튜닝**: 
- **평가**: 
- **예측**: 

### 데이터 파이프라인

1. **데이터 수집**:
2. **특성 엔지니어링**:
3. **데이터 전처리**:

### 모델 아키텍처
### 하이퍼파라미터 튜닝
### 평가 지표
### 시각화
### 필요 라이브러리


# DeepSeek
### 주요 기능
- **데이터 통합**: 
- **기술적 지표**:
- **하이브리드 딥러닝**:
- **하이퍼파라미터 최적화**:
- **종합적 평가**:
- **방향성 예측**:
- **시각화**:

### 프로젝트 구조

- **데이터 처리**: 
- **모델 구축**: 
- **훈련 & 튜닝**: 
- **평가**: 
- **예측**: 

### 데이터 파이프라인

1. **데이터 수집**:
2. **특성 엔지니어링**:
3. **데이터 전처리**:

### 모델 아키텍처
### 하이퍼파라미터 튜닝
### 평가 지표
### 시각화
### 필요 라이브러리

# Gemini
### 주요 기능
- **데이터 통합**: 
- **기술적 지표**:
- **하이브리드 딥러닝**:
- **하이퍼파라미터 최적화**:
- **종합적 평가**:
- **방향성 예측**:
- **시각화**:

### 프로젝트 구조

- **데이터 처리**: 
- **모델 구축**: 
- **훈련 & 튜닝**: 
- **평가**: 
- **예측**: 

### 데이터 파이프라인

1. **데이터 수집**:
2. **특성 엔지니어링**:
3. **데이터 전처리**:

### 모델 아키텍처
### 하이퍼파라미터 튜닝
### 평가 지표
### 시각화
### 필요 라이브러리
