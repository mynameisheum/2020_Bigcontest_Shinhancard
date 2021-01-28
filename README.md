# 2020_Bigcontest_Shinhancard
Shinhancard_data_analysis_and_recommend_Characteristic


## 목적
- 2020년 빅콘테스트의 주제: 다양한 데이터를 활용하여 감염병(코로나)로 인한 소비/경제/행동 변화에 따른 사회적 영향분석,예측 모델링을 통한 서비스 아이디어와 PoC 제시
- 제시된 5가지 실제 데이터중 여러가지 feature를(columns) 골고루 가진 신한카드의 매출데이터를 선택 
- 실제 신한카드 매출데이터를 통해 코로나 이전과 이후의 차이를 비교
- 특히 features중 MCT_CAT_CD(품목코드)를 통해 SEX_CD(성별), AGE_CD(나이),등을 통해 적절한 전처리 후 clustering하여 선호도 분류
- 그중 MCT_CAT_CD엔 23개로 분류된 품목코드를 상관관계를 분석하여 p_value 0.05기준, 상관계수가 0.6 이상인 품목코드를 합쳐 총 10개로 자체적 차원축소 시도(전처리과정중..)
![남성 품목 상관계수](https://github.com/mynameisheum/2020_Bigcontest_Shinhancard/blob/main/picture%20storage/%EB%82%A8%EC%84%B1%EA%B8%B0%EC%A4%80%20%ED%92%88%EB%AA%A9%EC%BD%94%EB%93%9C%EB%B3%84%20%EC%83%81%EA%B4%80%EA%B3%84%EC%88%98%20%ED%99%95%EC%9D%B8.png?raw=true)

- (ex.적절한 전처리후 남성 기준 데이터로 Multi-Dimensional-Scaling(MDS)를 통해 cluster가 잘 분포되었음을 확인)
![남성cluster](https://github.com/mynameisheum/2020_Bigcontest_Shinhancard/blob/main/picture%20storage/%EB%82%A8%EC%84%B1%EA%B8%B0%EC%A4%80-clustering%20by%20Multi-Dimensional%20Scaling(MDS).png?raw=true)

### 데이터
- 신한매출데이터의 columns
-(STD_DD(날짜), GU_CD(구 코드),DONG_CD(동 코드),MCT-cAT_CD(품목코드),SEX_CD(성별코드), AGE_CD(나이코드),USE_CNT(품목사용횟수 코드),USE_AMT(총가격 코드)
- 2537754개의 row data
-(개인정보 보호로 인해 실제 데이터의 head(100)만 data를 업로드 해놓음)

### 프로토 타입
-https://kang9366.github.io/bigcontest/POC%20html/home.html
- (예시)
![그레이하운드](https://github.com/mynameisheum/2020_Bigcontest_Shinhancard/blob/main/picture%20storage/%EA%B7%B8%EB%A0%88%EC%9D%B4%ED%95%98%EC%9A%B4%EB%93%9C.png?raw=true)

### 의의
- python을 배운지 얼마 안되 서툰 실력으로 프로젝트를 시행함
- 실제 데이터를 다룰수 있는 좋은 기회였음
- 특히 DataFrame과 전처리 과정의 중요성을 알수 있었음
