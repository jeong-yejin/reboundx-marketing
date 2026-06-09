# AI-Marketing-Skills + GA4 MCP 결합 프롬프트 10선
> ReboundX 전용 | 데이터 기반 콘텐츠 제작 & 성과 최적화
> 사용법: `cd ~/Desktop/MKT/brands/reboundx` → `claude` 실행 후 프롬프트 입력

---

## 01. GA4 성과 기반 주간 콘텐츠 전략 수립

```
아래 두 작업을 순서대로 실행해줘.

Step 1 — GA4 MCP (Property ID: 520538981):
최근 7일간 콘텐츠 성과 데이터를 가져와줘.

요청 1 — 채널별 유입:
- dimensions: sessionDefaultChannelGroup, sessionSource
- metrics: totalUsers, sessions, engagementRate, conversions
- date_range: 최근 7일

요청 2 — 페이지별 성과:
- dimensions: pagePath
- metrics: screenPageViews, totalUsers, bounceRate, averageSessionDuration
- order_by: screenPageViews DESC
- limit: 15

요청 3 — 지역별:
- dimensions: country
- metrics: totalUsers, conversions
- limit: 10

Step 2 — content-ops 스킬:
GA4 데이터 분석 결과를 바탕으로 다음 주 콘텐츠 전략을 수립해줘.

brand-brief.md를 읽고 아래 내용을 작성:
1. 이번 주 데이터 인사이트 요약 (3줄)
2. 다음 주 채널별 콘텐츠 계획:
   - 트위터(X): 주 5회 (게시물별 카피 완성)
   - 텔레그램: 주 3회 (메시지 완성)
   - 블로그: 주 1회 (제목 + 구조)
3. 각 콘텐츠의 근거 (어떤 데이터 인사이트에 기반하는지 명시)
4. 이번 주 전환율이 높았던 채널에 가중치를 두어 배분
5. 이탈률이 높았던 페이지를 보완하는 콘텐츠 포함

outputs/data-driven-weekly-plan-2026-04-13.md로 저장해줘.
```

---

## 02. 퍼널 이탈 분석 기반 온보딩 카피 최적화

```
아래 두 작업을 순서대로 실행해줘.

Step 1 — GA4 MCP (520538981):
최근 30일간 온보딩 퍼널 데이터를 가져와줘.

요청 1 — 이벤트별 사용자 수:
- dimensions: eventName
- metrics: eventCount, totalUsers
- date_range: 최근 30일

요청 2 — 가이드 페이지 이탈률:
- dimensions: pagePath
- metrics: screenPageViews, bounceRate, averageSessionDuration, conversions
- dimension_filter: pagePath contains "/guide/"
- date_range: 최근 30일

요청 3 — 디바이스별 퍼널 차이:
- dimensions: deviceCategory, eventName
- metrics: eventCount, totalUsers
- date_range: 최근 30일

Step 2 — content-ops 스킬:
brand-brief.md를 읽고, GA4 퍼널 데이터에서 발견된 이탈 구간을 기반으로
온보딩 카피를 재작성해줘.

이탈이 높은 구간마다:
1. 현재 예상되는 이탈 원인 (데이터 기반)
2. 개선된 카피 2개 버전 (A/B)
   - 히어로 섹션, 거래소 연결 안내, 연결 완료 화면, 정산 알림 등
3. 모바일 특화 버전 (동남아 모바일 사용자 고려)
4. 각 카피의 기대 효과와 측정 방법

expert-panel로 전체 카피 품질 검증.
outputs/funnel-optimized-onboarding.md로 저장해줘.
```

---

## 03. 지역별 데이터 기반 차별화 콘텐츠 제작

```
아래 두 작업을 순서대로 실행해줘.

Step 1 — GA4 MCP (520538981):
최근 30일간 미국 vs 동남아 상세 데이터를 가져와줘.

요청 1 — 미국:
- dimensions: landingPage, sessionSource
- metrics: totalUsers, sessions, bounceRate, conversions
- dimension_filter: country = "United States"
- limit: 20

요청 2 — 동남아:
- dimensions: country, landingPage, deviceCategory
- metrics: totalUsers, sessions, bounceRate, conversions
- dimension_filter: country in ["Vietnam", "Thailand", "Indonesia", "Philippines"]
- limit: 20

요청 3 — 시간대별 활동:
- dimensions: hour, country
- metrics: activeUsers
- dimension_filter: country in ["United States", "Vietnam", "Thailand", "Indonesia", "Philippines"]
- date_range: 최근 7일

Step 2 — content-ops 스킬:
brand-brief.md를 읽고, 지역별 데이터 인사이트를 기반으로
미국과 동남아 각각에 최적화된 콘텐츠를 제작해줘.

미국 타겟 (영어):
1. 트위터 스레드 (5트윗) — 미국 유저가 가장 많이 방문하는 페이지 주제 기반
2. 레딧 포스트 초안 — 미국 유저 인게이지먼트율이 높은 토픽 기반
3. 게시 최적 시간 제안 (GA4 시간대 데이터 기반)

동남아 타겟 (영어, 간결한 문장):
1. 텔레그램 메시지 3개 — 동남아 유저가 많이 보는 페이지 주제 기반
2. 모바일 최적화 온보딩 메시지 — 모바일 이탈률 데이터 반영
3. 게시 최적 시간 제안 (GA4 시간대 데이터 기반)

outputs/region-specific-content-2026-04-08.md로 저장해줘.
```

---

## 04. 전환 이벤트 기반 Growth Engine 실험 설계

```
아래 두 작업을 순서대로 실행해줘.

Step 1 — GA4 MCP (520538981):
최근 30일간 전환 이벤트 상세 데이터를 가져와줘.

요청 1 — 전환별 채널:
- dimensions: eventName, sessionDefaultChannelGroup
- metrics: eventCount, totalUsers
- date_range: 최근 30일

요청 2 — 전환별 랜딩 페이지:
- dimensions: eventName, landingPage
- metrics: eventCount, totalUsers
- date_range: 최근 30일

요청 3 — 전환별 지역:
- dimensions: eventName, country
- metrics: eventCount, totalUsers
- limit: 20

Step 2 — growth-engine 스킬:
GA4 전환 데이터를 분석한 후, 전환율을 높이기 위한 A/B 실험 3개를 설계해줘.

실험 1: 랜딩 페이지 → 거래소 연결 전환율 최적화
- GA4에서 연결 전환율이 가장 낮은 랜딩 페이지 특정
- 해당 페이지의 히어로 카피 3개 variant 작성
- growth-engine create로 실험 생성

실험 2: 소셜 미디어 → 사이트 방문 전환율 최적화
- GA4에서 소셜 유입 대비 인게이지먼트가 가장 낮은 소스 특정
- 해당 채널의 CTA 3개 variant 작성
- growth-engine create로 실험 생성

실험 3: 지역별 전환율 격차 해소
- 미국 vs 동남아 전환율 차이가 큰 이벤트 특정
- 지역별 메시지 variant 작성
- growth-engine create로 실험 생성

각 실험의 가설, 변수, 측정 기준을 명확히 포함.
outputs/data-driven-experiments-2026-04-08.md로 저장해줘.
```

---

## 05. 정산 신뢰도 콘텐츠: 데이터 기반 메시지 최적화

```
아래 두 작업을 순서대로 실행해줘.

Step 1 — GA4 MCP (520538981):
정산 관련 페이지의 사용자 행동을 분석해줘.

요청 1 — 대시보드/정산 페이지 성과:
- dimensions: pagePath
- metrics: screenPageViews, totalUsers, averageSessionDuration, bounceRate
- dimension_filter: pagePath contains "dashboard" OR pagePath contains "settlement" OR pagePath contains "payout"
- date_range: 최근 30일

요청 2 — 재방문 사용자의 페이지 패턴:
- dimensions: pagePath, newVsReturning
- metrics: screenPageViews, totalUsers
- dimension_filter: newVsReturning = "returning"
- limit: 15

요청 3 — 연결 완료 후 행동:
- dimensions: pagePath
- metrics: screenPageViews, averageSessionDuration
- date_range: 최근 30일

Step 2 — content-ops 스킬:
brand-brief.md의 사용자 상태 3번(정산 구조를 신뢰하지 못하는 사용자)을 읽고,
GA4 데이터 인사이트를 반영해서 정산 신뢰도 콘텐츠를 제작해줘.

데이터에서 발견된 패턴 반영:
- 재방문 사용자가 가장 많이 보는 페이지 = 불안감의 지표
- 대시보드 체류 시간이 길면 = 정산 확인에 시간 소요
- 이탈률이 높은 정산 관련 페이지 = 정보 부족 또는 신뢰 부족

제작할 콘텐츠:
1. 대시보드 내 마이크로카피 개선안 (데이터 기반)
2. "정산 완료율 XX%" 같은 실제 데이터를 활용한 트윗 3개
3. 텔레그램 FAQ 업데이트 (데이터에서 발견된 주요 의문점 기반)
4. 정산 프로세스 설명 인포그래픽 스크립트 (5장)

expert-panel로 전체 신뢰 구축 효과 검증.
outputs/data-driven-trust-content-2026-04-08.md로 저장해줘.
```

---

## 06. 실시간 캠페인 효과 측정 + 즉시 콘텐츠 조정

```
이 프롬프트는 캠페인/콘텐츠 발행 직후(30분~2시간 후) 사용해줘.

Step 1 — GA4 MCP (520538981):
실시간 리포트를 실행해줘.

요청 1 — 현재 활성 사용자:
- realtime report
- dimensions: unifiedScreenName
- metrics: activeUsers

요청 2 — 유입 소스:
- realtime report
- dimensions: sessionSource
- metrics: activeUsers

요청 3 — 국가별:
- realtime report
- dimensions: country
- metrics: activeUsers

Step 2 — content-ops 스킬:
실시간 데이터를 분석하고 즉시 조정이 필요한 사항을 판단해줘.

판단 기준:
- 평소 대비 트래픽 급증 → 추가 콘텐츠로 모멘텀 활용
- 평소 대비 반응 미미 → 메시지 수정 또는 추가 채널 게시
- 특정 지역에서 반응이 집중 → 해당 지역 타겟 추가 메시지

즉시 실행 가능한 액션:
1. 트래픽 급증 시: 후속 트윗 2개 + 텔레그램 리마인더 1개 즉시 작성
2. 반응 미미 시: 원본 메시지의 프레이밍을 바꾼 대체 카피 3개 작성
3. 지역 집중 시: 해당 지역 맞춤 메시지 2개 작성

결과를 화면에 출력 (긴급 대응이므로 파일 저장보다 즉시 실행 우선).
필요하면 outputs/campaign-realtime-2026-04-08.md로 저장.
```

---

## 07. 월간 성과 리포트 + 다음 달 전략 자동 생성

```
아래 작업을 순서대로 실행해줘.

Step 1 — GA4 MCP (520538981):
이번 달 전체 데이터를 가져와줘.

요청 1 — 일별 트렌드:
- dimensions: date
- metrics: totalUsers, newUsers, sessions, conversions, engagementRate
- date_range: 이번 달 1일~오늘

요청 2 — 채널별 성과:
- dimensions: sessionDefaultChannelGroup
- metrics: totalUsers, sessions, conversions
- date_range: 이번 달

요청 3 — 지역별 성과:
- dimensions: country
- metrics: totalUsers, conversions
- limit: 15

요청 4 — 전환 이벤트별:
- dimensions: eventName
- metrics: eventCount, totalUsers
- date_range: 이번 달

요청 5 — 상위 페이지:
- dimensions: pagePath
- metrics: screenPageViews, bounceRate, conversions
- order_by: screenPageViews DESC
- limit: 20

Step 2 — content-ops 스킬:
brand-brief.md와 outputs/ 폴더의 기존 전략 파일을 참고해서
팀 공유용 월간 마케팅 성과 리포트를 작성해줘.

포함 항목:
1. Executive Summary (5줄 이내)
2. KPI 대시보드 (표 형식)
   - 총 유저 수 / 신규 유저 / 세션 수 / 전환 수 / 인게이지먼트율
   - 전월 대비 증감률 (전월 데이터가 없으면 추세만 표시)
3. 채널별 성과 분석 (유입 대비 전환 효율 순으로 정렬)
4. 지역별 성과 분석 (미국 vs 동남아 비교)
5. 전환 퍼널 분석 (이벤트별 단계 이탈률)
6. 콘텐츠 성과 하이라이트 (가장 효과적이었던 콘텐츠/캠페인)
7. 개선이 필요한 영역 (데이터 근거 포함)
8. 다음 달 전략 제안:
   - 채널별 가중치 조정
   - 콘텐츠 유형 믹스 변경
   - 지역별 투자 배분
   - 우선 실행 액션 TOP 5

outputs/monthly-report-2026-04.md로 저장해줘.
```

---

## 08. 레퍼럴 프로그램 성과 분석 + 캠페인 최적화

```
아래 두 작업을 순서대로 실행해줘.

Step 1 — GA4 MCP (520538981):
최근 30일간 레퍼럴 관련 데이터를 가져와줘.

요청 1 — 레퍼럴 이벤트:
- dimensions: eventName, date
- metrics: eventCount, totalUsers
- dimension_filter: eventName contains "referral" OR eventName contains "share"
- date_range: 최근 30일

요청 2 — 레퍼럴 유입 트래픽:
- dimensions: sessionSource, sessionMedium
- metrics: totalUsers, sessions, conversions
- dimension_filter: sessionMedium = "referral"
- date_range: 최근 30일

요청 3 — 레퍼럴 유입 사용자의 행동:
- dimensions: landingPage
- metrics: totalUsers, bounceRate, averageSessionDuration, conversions
- dimension_filter: sessionMedium = "referral"
- limit: 15

Step 2 — content-ops + growth-engine 스킬:
GA4 레퍼럴 데이터를 분석하고 레퍼럴 캠페인을 최적화해줘.

분석:
1. 레퍼럴 링크 공유 이벤트 트렌드 (증가/감소/정체)
2. 레퍼럴 유입 사용자의 전환율 (직접 유입 대비)
3. 어떤 레퍼럴 소스가 가장 효과적인지
4. 레퍼럴 유입 사용자의 이탈 포인트

최적화 액션:
A. 레퍼럴 공유를 유도하는 메시지 3개 variant (growth-engine 실험 설계)
B. 레퍼럴 유입 사용자 전용 랜딩 페이지 카피
C. 텔레그램 레퍼럴 캠페인 메시지 (동남아 타겟)
D. 레퍼럴 성과 대시보드 UX 카피 개선안

outputs/referral-optimization-2026-04-08.md로 저장해줘.
```

---

## 09. 거래소별 성과 비교 + 가이드 콘텐츠 우선순위 결정

```
아래 두 작업을 순서대로 실행해줘.

Step 1 — GA4 MCP (520538981):
최근 30일간 거래소별 가이드 페이지 성과를 가져와줘.

요청 1 — 거래소 가이드 페이지:
- dimensions: pagePath
- metrics: screenPageViews, totalUsers, bounceRate, averageSessionDuration, conversions
- dimension_filter: pagePath contains "/guide/signup/" OR pagePath contains "/exchanges/"
- date_range: 최근 30일

요청 2 — 거래소 페이지 유입 채널:
- dimensions: pagePath, sessionDefaultChannelGroup
- metrics: totalUsers, sessions
- dimension_filter: pagePath contains "/guide/" OR pagePath contains "/exchanges/"

요청 3 — 거래소 페이지 디바이스별:
- dimensions: pagePath, deviceCategory
- metrics: totalUsers, bounceRate
- dimension_filter: pagePath contains "/guide/"

Step 2 — content-ops 스킬:
brand-brief.md의 파트너 거래소 목록과 GA4 데이터를 결합해서
거래소별 콘텐츠 우선순위를 결정하고 가이드 콘텐츠를 최적화해줘.

거래소 성과 매트릭스:
| 거래소 | 페이지뷰 | 전환수 | 이탈률 | 상태 | 액션 |

상태 분류:
- 🟢 고트래픽 + 고전환: 유지 및 강화
- 🟡 고트래픽 + 저전환: 카피/UX 개선 시급
- 🟠 저트래픽 + 고전환: 유입 확대 집중
- 🔴 저트래픽 + 저전환: 근본 원인 파악 필요

각 상태별 액션:
1. 🟡 거래소: 가이드 페이지 카피 재작성 (이탈 원인 해소)
2. 🟠 거래소: 해당 거래소 홍보 트윗 3개 + 텔레그램 소개 메시지
3. 🔴 거래소: 개선 전략 제안 (콘텐츠? 포지셔닝? UX?)

outputs/exchange-performance-optimization-2026-04-08.md로 저장해줘.
```

---

## 10. 종합 Growth Dashboard: 데이터 + 실험 + 콘텐츠 통합 뷰

```
아래 작업을 순서대로 실행해줘.

Step 1 — GA4 MCP (520538981):
핵심 성과 데이터를 한 번에 수집해줘.

요청 1 — 이번 주 vs 지난 주:
- dimensions: date
- metrics: totalUsers, newUsers, conversions, engagementRate
- date_range: [{"start_date": "14daysAgo", "end_date": "8daysAgo"}, {"start_date": "7daysAgo", "end_date": "today"}]

요청 2 — 채널별 전환 효율:
- dimensions: sessionDefaultChannelGroup
- metrics: totalUsers, conversions
- date_range: 최근 7일

요청 3 — 실시간 현황:
- realtime report
- metrics: activeUsers

Step 2 — growth-engine 스킬:
현재 실행 중인 모든 실험의 상태를 확인해줘.
- experiment-engine.py list (전체)
- 실험별 현재 상태, 데이터 포인트 수, 트렌딩 방향

Step 3 — content-ops 스킬:
GA4 데이터 + 실험 상태를 종합해서 Growth Dashboard를 생성해줘.

대시보드 형식:

## 📊 ReboundX Growth Dashboard — [날짜]

### 핵심 지표 (WoW 비교)
| 지표 | 이번 주 | 지난 주 | 변화 |
|------|---------|---------|------|

### 채널 효율 랭킹
| 채널 | 유입 | 전환 | 전환율 | 추세 |
|------|------|------|--------|------|

### 실행 중인 실험
| 실험 ID | 변수 | 상태 | 리딩 variant | 신뢰도 |
|---------|------|------|-------------|--------|

### 이번 주 승리 (데이터 기반)
- ...

### 이번 주 경고 (데이터 기반)
- ...

### 다음 주 최우선 액션 3가지
1. ...
2. ...
3. ...

outputs/growth-dashboard-2026-04-08.md로 저장해줘.
```

---

## 사용 팁

- **실행 순서**: GA4 데이터를 먼저 수집 → 분석 → 스킬로 콘텐츠 생성 (데이터가 콘텐츠를 결정)
- **주간 루틴**: 01 → 06(캠페인 발행 후) → 10 순서로 매주 실행
- **월간 루틴**: 07번을 매월 마지막 주에 실행
- **즉시 대응**: 06번은 캠페인 발행 30분~2시간 후 실행하면 실시간 최적화 가능
- **Expert Panel 추가**: 모든 콘텐츠 생성 후 "expert panel this"를 추가하면 품질 검증까지 자동화
- **날짜 자동화**: "오늘 날짜를 파일명에 자동으로 넣어줘"로 실행 시점 기준 저장
