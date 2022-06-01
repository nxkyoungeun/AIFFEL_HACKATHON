# AIFFEL 해커톤
AIFFEL 에서 진행한 자유주제 해커톤입니다.
***
# 🪴업사이클링 브랜드 및 제품 추천
## 목차
[1. 팀원 구성 및 역할](#팀원-구성-및-역할)<br>
[2. 프로젝트 배경](#프로젝트-배경)<br>
[3. 프로젝트 소개](#프로젝트-소개)<br>
[4. 추천시스템](#추천시스템)<br>

***
### 팀원 구성 및 역할
* 팀명 : Re미티드에디션
* 팀원 & 역할
  | 팀원 | 역할 |
  | :---: | :---: |
  | 노경은 | 데이터 전처리, 모델 구성 |
  | 유동린 | 데이터 수집, 데이터 시각화, 웹페이지 구성 |
  | 우성아 | 참고 자료 수집 |
* 해커톤 기간 : 2022. 05. 03 ~ 2022. 06. 09


### 프로젝트 배경
환경문제가 대두되고 있는 요즘 업사이클링에 대한 대중들의 관심은 높아졌으나 업사이클링 브랜드는 비교적 알려지지 못했다.  
업사이클링 브랜드 중 가장 유명한 브랜드는 스위스 브랜드인 '[프라이탁](https://ko.wikipedia.org/wiki/%ED%94%84%EB%9D%BC%EC%9D%B4%ED%83%81)'이라고 생각한다.  
국내에도 이와 비슷한 다양한 브랜드가 존재한다. 대중들에게 업사이클링과 국내브랜드를 알리기 위해 이 프로젝트를 기획했다.  
대중들이 해당 추천시스템을 통해 국내 업사이클링 브랜드를 알게되고 제품을 선택할 때 도움이 되기를 바란다.


### 프로젝트 소개
1. 데이터 수집
- 업사이클링 브랜드별로 표시하고 있는 데이터 형식들이 다르기 때문에 스크래핑 후 전처리 작업이 더 오래 걸릴 것이라 예상했다.
- 의류 이커머스인 무신사에서 업사이클링 아이템을 구매한 사용자들의 구매내역을 수집하였다.
2. 선정 대상
- 업사이클링 아이템은 가방류, 의류, 모자로 한정한다.
- 위 아이템을 구매한 사용자의 구매후기를 수집했다.
3. 컬럼 소개
- 사이트, 사용자이름(ID), 색상, 소재, 종류, 별점, 성별(구매자), 가격, 무늬, 업사이클링브랜드(0과 1, 이름), 웹사이트주소
4. 데이터 분석
- 색상
![image](https://user-images.githubusercontent.com/97087253/171132821-133896c3-ab84-42e5-8697-96c619a9b3a0.png)
- 소재
![image](https://user-images.githubusercontent.com/97087253/171340475-86b206ee-cac5-486f-8dab-9cdef2df6e51.png)
- 성별
![image](https://user-images.githubusercontent.com/97087253/171132950-700ddb6c-644d-4aec-8f6b-566d181eec05.png)
- 가격
![image](https://user-images.githubusercontent.com/97087253/171340681-f4457cf1-bf26-4365-83ed-e6f0064db59c.png)
- 무늬 여부
![image](https://user-images.githubusercontent.com/97087253/171340718-5a583d4e-8c0c-4ec9-a572-c02a0294d9ad.png)

5. 추천시스템 종류(시도한 것들)
- 뉴럴 네트워크 임베딩
- 로지스틱 회귀분류
- 코사인유사도


### 추천시스템
1. 데이터 전처리
- 색상
- 소재
- 가격
2. 모델
-

3. 추천시스템 결과물  
a. 사용자의 최근 구매 정보를 입력  
    구매 정보: 색상, 소재, 종류, 별점, 성별, 가격, 무늬여부  
     -> 마지막에 구매 정보를 추가  
b. 모델 실행  
c. 결과 도출: 업사이클링 브랜드 추천 or 비슷한 유저가 구매한 업사이클링 제품 추천  
d. 결과에 대한 만족도를 물어본다. -> 만족함을 선택한다. -> 추천한 업사이클링 브랜드를 데이터에 추가한다. -> 새로운 유저의 정보를 얻을 수 있다.
[reference-참고 웹페이지](https://western-sky.tistory.com/60?category=847883#%E2%9C%A8%EA%B5%AC%ED%98%84-%EA%B2%B0%EA%B3%BC)
