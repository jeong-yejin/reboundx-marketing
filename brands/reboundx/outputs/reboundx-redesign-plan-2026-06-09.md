# ReboundX 개편안 기획 초안 — 페인포인트 개선 + 고체류 섹션 강화

작성 2026-06-09 · GA4 property 520538981 · 페이지 28일 / 트렌드 7일 / 채널 28일

## 1. 개요 — 현재 지표 (사실)

- **7일 DAU**: 평균 81명 (06-02~08 전일 기준), 피크 105 (06-08). 06-09 진행 중(34, 제외).
- **신규 비율**: DAU의 약 70%가 신규. 높음.
- **유입 채널**: Direct 66.1% / Organic Search 15.4% / Referral 7.2% / Organic Social 6.7%.
- **전체 이탈률**: 14.5% (낮음).
- **트래픽 집중**: `/en` 6,012뷰(일 ~215) = 2위 point-calculator(919뷰)의 6.5배.

## 2. 데이터 분석 (사실)

페인포인트 후보 (트래픽 높고 이탈 높음):

- `/en/perpdex/point-calculator` — 919뷰 / 이탈 31.3% / 체류 90초
- `/en/exchanges` — 820뷰 / 이탈 22.0% / 체류 29초
- `/en/funding` — 418뷰 / 이탈 22.0% / 체류 38초
- `/en/perpdex` — 256뷰 / 이탈 18.6% / 체류 31초
- `/en` — 6,012뷰 / 이탈 16.7% / 체류 14초

이탈 규모 근사 (뷰 곱하기 이탈률, 랭킹용): `/en` 약 1,004 > point-calculator 약 288 > exchanges 약 180 > funding 약 92.

고체류(develop) 후보:

- `/en/terminal-exchange` — 체류 486초 / engagement 98.7% / 193뷰
- `/en/terminal-mypage/asset` — 체류 455초 / engagement 93.3% / 145뷰
- `/en/terminal-mypage/overview` — 체류 215초 / 159뷰
- `/en/terminal-mypage/exchanges` — 체류 211초 / 152뷰

온보딩: `/en/onboarding/service-guide` 327뷰 / 19초, `/en/onboarding/exchange-selection` 176뷰 / 16초 — 트래픽 있고 체류 짧음.

## 3. 우선순위 판단 (판단)

스펙 기준 적용: 신규 70% 이면 "첫 경험 우선" 발동. 트래픽 높고 이탈 높음 이면 point-calculator·exchanges·funding. 트래픽 집중 이면 `/en`.

옵션 / 트레이드오프:

- **A. /en 첫 화면 + 온보딩** — 절대 이탈 최대(약 1,004), 신규 70% 직격. 단 원인 분산.
- **B. point-calculator** — 이탈률 최고(31.3%), 단일 도구라 수정면 명확, 빠른 승. 단 절대 손실은 홈의 4분의 1.
- **C. terminal 계열 develop** — 가치 최고(체류 200~486초)이나 도달 적음(200뷰 미만), 성장 기여 작음.

**권장**: P1 = A, P2 = B, P3 = C.

**기각 조건**: 전환 목표가 terminal 도달이면 C가 P1로 올라간다. 전환 이벤트 데이터 필요(이번 쿼리 미포함).

## 4. 기획 내용 (판단)

### 스트림 1 — 페인포인트 (P1·P2)

- `/en` 첫 화면: 신규 70% 첫 진입점. 가치 제안 + 다음 액션 1개를 above-the-fold 고정. 이탈 16.7% 에서 목표 12%.
- `/en/onboarding/` 흐름: 체류 16~19초 는 빠른 통과. 완료인지 이탈인지 스텝별 이벤트로 분해.
- `/en/perpdex/point-calculator`: 이탈 31.3% 원인 분해(첫 입력 마찰 / 로딩 / 모바일). 목표 20%.

### 스트림 2 — 고체류 develop (P3)

- terminal-exchange, terminal-mypage(asset·overview·exchanges): 핵심 가치면. 기능 확장 + `/en`·exchanges·point-calculator 에서 이 페이지로 가는 동선 추가.
- 가정: terminal·mypage 계열은 로그인 게이트라 도달 적음. **기각 조건**: 비게이트면 강화가 아니라 발견(SEO·내부링크) 문제다.

## 5. 성공 지표

- `/en` 이탈 16.7% 에서 12% (28일)
- point-calculator 이탈 31.3% 에서 20%
- terminal 계열 진입 세션 증가 (퍼널 동선 후)
- 측정: GA4 `pagePath` 곱하기 `bounceRate` / 진입경로
- **미보유**: 전환 이벤트(가입·거래소 연동). 최종 성공은 전환으로 묶어야 함, 목표 이벤트 지정 필요.

## 6. 진행 전 검증 필요

1. terminal·mypage 계열 로그인 게이트 여부 (스트림 2 방향 결정)
2. point-calculator 31% 이탈이 빠른 답 후 만족 이탈인가 마찰인가 (세션 기록 / 스크롤 depth)
3. 디바이스 분포 — 이번 쿼리 미포함. 모바일 이탈이 다르면 우선순위 흔들림
4. 전환 목표 이벤트 정의
