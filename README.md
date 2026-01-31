# 한국 주식시장과 경제지표 간 상관관계 분석
> 서울 부동산 매매가 회귀분석을 중심으로

## 1. 프로젝트 개요
최근 2-3년간 국내 주식 투자 관심 증가와 20-30대의 투자 참여 확대 배경에서,
주가지수(코스피/코스닥)와 주요 경제지표(미국 지수, 금리, 비트코인, 서울 부동산 매매가)의 관계를 분석한다.

**Research Questions**
- 코스피/코스닥과 주요 경제지표의 상관관계는 어떠한가?
- 연령대별 보유주식수/주주수와 지수는 관계가 있는가?
- 서울 부동산 매매가와 주식지수는 어떤 관계를 보이는가?

## 2. 데이터
- 기간: 2018-07 ~ 2022-06
- 변수
  - KOSPI, KOSDAQ
  - S&P 500, NASDAQ
  - Bitcoin price
  - Base rate (KR / US)
  - Seoul house transaction price
  - Age-group stock holdings / shareholders
- 데이터프레임
  - df_1: 연도별 보유주식수/주주수 비율 + 연령
  - df_2: 월별 지수/지표(코스피, 코스닥, S&P500, 나스닥, 비트코인, 서울 매매가, 한/미 기준금리)
  - df_3: 연도별 코스피/코스닥 + 연령별 보유주식수
  - df_4: 연도별 코스피/코스닥 + 연령별 주주수

## 3. 방법론
- Trend visualization
- Correlation: Spearman correlation
- Regression: OLS regression + VIF
- Sub-analysis: Seoul 7 regions regression

## 4. 핵심 결과
- (Correlation) KOSPI/KOSDAQ/S&P500/NASDAQ/BTC는 강한 상관을 보임.
- (Age) 20~30대 보유주식수는 지수와 유의미한 차이가 크지 않음.
- (Regression) OLS+VIF 기준으로 '매매가_서울' 변수만 유의미하게 관측됨.
- (Reverse check) 매매가_서울을 종속변수로 두었을 때 KOSPI/KOSDAQ은 유의미하지 않음.
- (Regional) 서울 7개 권역 회귀에서 서북권/동남권의 계수 차이가 관측됨.
