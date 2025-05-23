# 자립준비청년의 독립을 위한 최적의 입지선정 🗺️📍

본 프로젝트는 데이터 분석 경진대회 우수상 활동으로 2022.09.27 ~ 2022.12.08 기간 내 진행한 프로젝트 입니다.

주제는 <b>'자립준비청년의 독립을 위한 최적의 입지 선정'</b>으로 선정하였습니다.

여기서 자립준비 청년이란, 부모가 없거나 양육하기에 적당하지 않아 아동복지시설, 위탁 가정에서 보호되다가 원가정으로 복귀하지 못하고 만 18세 이후 연령도래로 보호종료되는 청년을 말합니다.


팀명 : 예아(Yeah-A) - 예린이와 아이들

팀원 : 👨🏻‍💻강현구, 👩🏻‍💻서주현, 👩🏻‍🔬이서영(팀장), 👩🏼‍🎨임예린

주제 : 자립준비청년의 독립을 위한 최적 입지선정

제안 : 자립준비청년들이 완전한 독립을 이루기까지 머무는 시설, 거처를 구당 하나씩 제안 



## ✔️ 프로젝트 배경
**○ 연장보호종료 자립준비청년 비율 증가**
- 2018년 이후 연장보호종료 자립준비청년의 비율이 급격하게 증가
- 2020년, 연장보호종료  자립준비청년 비율이 57.8%로 이들을 위한 대책 마련 시급

**○ 자립 지원 체계 추진 대책이 필요함**
- 보호가 종료되어 사회로 나오는 자립준비 청년들은 경제적 어려움과 주거문제로 큰 어려움을 겪고 있음
- 대상자 이관 기준이 부재하고 정보시스템을 기반으로 제도적으로 이관되지 않음

**○ 주거 환경 보완 필요**
- LH 들어가기 힘듦.
- 적절한 주거 위치 추천을 함으로써 생활/ 경제적인 부담을 줄여줄 수 있음
- 자립준비청년들은 주거문제 및 주거 비용 문제를 68%가 개인이 부담해야 함
- 전체 자립준비청년 2명 중 1명도 나라에서 지원하는 주택에서 지낼 수 없음 
- 보호종료 아동 주거 자립지원시설은3 % 에 불가


- 보호종료아동이 주거할만한 지역 추천 필요
- 이에 따라 최적의 입지 선정 및 적합한 지역을 다양한 요소들의 분석을 통해 제안



## ✔️ 프로젝트 구현 방법
### 1. 데이터 수집
경제 적합성
- 시장/마트 물가 (서울특별시 물가정보)
- 부동산 전월세가 (서울 열린 데이터 광장)
- 서울시 착한 가격 업소 (서울특별시 물가정보)

교통 접근성
- 버스 정류장 (서울 빅데이터 캠퍼스)

위치 적합성
- 아동복지시설 현황(서울특별시)
- 행정동 경계 (국가공간정보포털)
- 서울시 주요시설 (서울 빅데이터 캠퍼스)
- 도서관 (서울 빅데이터 캠퍼스)
- 서울시 월세 매물 데이터 (네이버 부동산)



### 2. 입지 대상 동 선정

**1️⃣ 현황 분석**
- 탐색적 자료 분석(EDA)
- 주성분 분석

**2️⃣ 군집 분석**
- K-means Clustering
- 과적합 방지를 위한 상관계수가 가장 높은 요인 제거
  • k-means 결과의 시각화를 통해 과적합이 일어나지 않고 후보 행정동을 가장 많이 포함하는 클러스터링 선택
  
  • 최종 행정동 선정
 

 
### 3. 보호종료청소년을 위한 최적 입지 선정

**1️⃣ 공간 최적화 모델**

**MCLP와 P-median**

**2️⃣ 구별 물가 현황 파악 및 동별 월세 현황 파악**
- Choroleth Map (단계 구분도)


- 두 알고리즘을 본 프로젝트에 맞게 수정하여 적용
- 행정동 내 입지후보군, 수요지점 (버스, 보건시설, 고아원) 위치 데이터, 월세, 물가 데이터 활용
- AHP 분석을 통한 수요지점별 선호도 가중치 * 수요지점별 개수 가중치 활용
- 두 알고리즘에서 공통으로 선정된 최적 입지 몇곳 선정



### 4. 입지선정지수 도출
**1️⃣ 입지 선정 후보지와 물가 데이터로 경제성 고려**
- 자립 준비 청년의 경제적 부담을 줄이기 위한 낮은 물가의 입지 선별
- 소비가 많은 달걀, 돼지고기 가격 비교와 물가 데이터의 평균값을 시각화


**2️⃣ 클러스터링 + MCLP**
- 동별 전세 가격 시각화를 통해 추천 입지 중 경제적 부담을 완화시킬 수 있는 최적 입지 선별
- 서울시 도서관과 착한가격업소를 수요 포인트로, 보육원을 인풋으로 선정하여 분석 진행


### 5. 최종 입지 결정

세부 선정 과정 : 현재 월세 매물 데이터 이용 🔜 세부적인 위치, 가격대 선정
