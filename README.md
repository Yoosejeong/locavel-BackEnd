# ✈️ LocaveL
> 현지인 정보 기반 여행 플랫폼 서비스
<div align="center">
  <img width = 900, src="https://github.com/user-attachments/assets/200e0183-5c9f-430d-99bc-5166cb9a7b96">
</div>

<br>
<br>
<br>

## Members

|                         김민지                         |                            김정효                            |                         문정욱                         |                          유세정                          |                        이상은                        |
|:------------------------------------------------------:|:------------------------------------------------------------:|:------------------------------------------------------:|:--------------------------------------------------------:|:----------------------------------------------------:|
|  <img src="https://github.com/qzzloz.png" width="250"> |   <img src="https://github.com/J-neat.png" width="250">   |  <img src="https://github.com/m020202.png" width="250">   | <img src="https://github.com/Yoosejeong.png" width="250">| <img src="https://github.com/KkomSang.png" width="250"> |
|                     Backend Developer                  |                      Backend Developer                       |                   Backend Developer                    |                    Backend Developer                     |                  Backend Developer                   |
| <center>[qzzloz](https://github.com/qzzloz)</center> | <center>[J-neat](https://github.com/J-neat)</center> | <center>[m020202](https://github.com/m020202)</center> | <center>[Yoosejeong](https://github.com/Yoosejeong)</center> | <center>[KkomSang](https://github.com/KkomSang)</center> |

<br>
<br>
<br>

## 아키텍처 구조
<div align="center">
  <img width = 900, src="https://github.com/user-attachments/assets/a3285b4e-9c44-4126-9384-2bada11f4f9b">
</div>

<br>
<br>
<br>

## 👤 Personal Contribution

> 유세정 (Yoosejeong) – Backend Developer

### 🛠️ 등급 시스템 기능 구현

- 유저의 로컬/여행객 등급을 조회하는 API 개발
- 장소 등록 및 리뷰 작성 시 등급 점수 자동 반영 로직 구현
- 매일 자정 기준으로 자동 점수 반영되는 스케줄러 작성
- 점수에 따른 등급 Enum(`IRON`, `BRONZE`, `SILVER` 등) 계산 및 적용 로직 개발

#### ✅ 주요 서비스 함수

| 기능 | 함수명 |
|------|--------|
| 유저 등급 조회 | `getUserGrade(Long userId)` |
| 로컬 등급 점수 갱신 | `updateLocalGrade(Long userId)` |
| 여행객 등급 점수 갱신 | `calculateTravelerGradeScore(Long userId, ReviewDTO request)` |
| 자정 기준 자동 점수 반영 | `updateMemberScoresDaily()` |
| 점수 → 등급 계산 | `calculateLocalGrade(int score)` |


<br>
<br>
<br>

## Service
<div align="center">
  <img width = 400, src="https://github.com/user-attachments/assets/8580ed3e-8fc2-4675-9ae9-ee9f8cc7d9fb">
  <img width = 400, src="https://github.com/user-attachments/assets/1da88121-92e1-476c-9794-47d1e674761a">
</div>

- 플레이스 등록 및 조회
- 현지인, 여행객 별 평점 확인

<div align="center">
  <img width = 400, src="https://github.com/user-attachments/assets/a5f5b483-a7b3-4351-8123-a0c230783fdc">
  <img width = 400, src="https://github.com/user-attachments/assets/10aa34b7-377a-44f9-ba05-7bc6afd26ce6">
</div>

- 관심 지역 및 내 지역의 추천 플레이스 조회

<div align="center">
  <!-- <img width = 400, src="https://github.com/user-attachments/assets/050441fb-610d-4a42-a668-5408db282d53"> -->
  <img width = 400, src="https://github.com/user-attachments/assets/d0b8b64e-12b3-49e8-a4f6-5e67c0322fab">
  <img width = 400, src="https://github.com/user-attachments/assets/f6f91f49-7859-4983-8c59-cad08d7695fc">
</div>

- 추천 플레이스 중 관심 있는 것은 위시리스트로 저장
- 등록한 플레이스와 리뷰에 따라 갱신되는 등급 시스템
