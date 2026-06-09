# GA4 MCP 활용 프롬프트 10선
> ReboundX 전용 | GA4 Property ID: 520538981
> 사용법: `cd ~/Desktop/MKT/brands/reboundx` → `claude` 실행 후 프롬프트 입력

---

## 01. 주간 트래픽 소스별 성과 리포트

```
GA4 MCP를 사용해서 ReboundX(Property ID: 520538981)의
최근 7일간 트래픽 소스별 성과를 분석해줘.

데이터 요청:
- dimensions: sessionDefaultChannelGroup, sessionSource, sessionMedium
- metrics: sessions, totalUsers, newUsers, engagedSessions, engagementRate, averageSessionDuration, conversions
- date_range: 최근 7일

분석 항목:
1. 채널별(organic / referral / social / direct / paid) 유입량 순위
2. 채널별 인게이지먼트율 비교
3. 채널별 전환 발생 현황
4. 전주 대비 변화가 큰 채널 하이라이트
5. 소셜 미디어 세부 소스 분석 (twitter, telegram, reddit 등)

인사이트:
- 가장 효율적인 채널 (유입 대비 전환율 기준)
- 개선이 필요한 채널과 구체적 액션 제안
- 이번 주 콘텐츠 방향에 반영할 포인트

research/ga4-weekly-traffic-{오늘 일자 YYYY-MM-DD}.md로 저장해주고 노션 데이터베이스에 업로드해줘.
```

---

## 02. 페이지별 사용자 행동 분석

```
GA4 MCP로 ReboundX(520538981)의
최근 14일간 페이지별 사용자 행동을 분석해줘.

데이터 요청:
- dimensions: pagePath, pageTitle
- metrics: screenPageViews, totalUsers, averageSessionDuration, bounceRate, engagementRate
- date_range: 최근 14일
- order_by: screenPageViews 내림차순
- limit: 30

분석 항목:
1. 상위 10개 페이지 트래픽 및 체류 시간
2. 이탈률이 60% 이상인 페이지 특정 + 원인 추정
3. 거래소 가이드 페이지(/en/guide/signup/*)별 성과 비교
4. Perpdex 비교 페이지(/en/perpdex) 사용 패턴
5. 랜딩 페이지 → 가이드 페이지 → 연결 완료로 이어지는 흐름 파악

개선 제안:
- 이탈률 높은 페이지별 카피/구조 개선 방향
- 체류 시간이 긴 페이지의 성공 요인 분석
- 내부 링크 구조 최적화 제안

research/ga4-page-behavior-2026-04-08.md로 저장해줘.
```

---

## 03. 지역별 유입 및 전환 비교 (미국 vs 동남아)

```
GA4 MCP로 ReboundX(520538981)의
최근 30일간 지역별 성과를 비교 분석해줘.

데이터 요청 1 — 국가별 개요:
- dimensions: country
- metrics: totalUsers, newUsers, sessions, engagementRate, conversions
- date_range: 최근 30일
- limit: 20

데이터 요청 2 — 미국 세부:
- dimension_filter: country = "United States"
- dimensions: region, city
- metrics: totalUsers, sessions, conversions
- limit: 15

데이터 요청 3 — 동남아 4개국 세부:
- dimension_filter: country in ["Vietnam", "Thailand", "Indonesia", "Philippines"]
- dimensions: country, deviceCategory
- metrics: totalUsers, sessions, engagementRate, conversions

분석:
1. 미국 vs 동남아 전체 비교 (유입량, 전환율, 인게이지먼트)
2. 동남아 국가별 순위 및 특성
3. 디바이스별 차이 (동남아 모바일 비중 확인)
4. 각 지역에 최적화된 콘텐츠 전략 제안

research/ga4-region-comparison-2026-04-08.md로 저장해줘.
```

---

## 04. 전환 퍼널 분석

```
GA4 MCP로 ReboundX(520538981)의
최근 30일간 전환 퍼널을 분석해줘.

데이터 요청 — 이벤트별 사용자 수:
- dimensions: eventName
- metrics: eventCount, totalUsers
- date_range: 최근 30일

주요 추적 이벤트 (brand-brief.md 기준):
- page_view (랜딩)
- 거래소 연결 시작 이벤트
- 거래소 연결 완료 (UID 연결 포함)
- 첫 정산 확인
- 레퍼럴 링크 공유

분석:
1. 각 단계별 사용자 수와 단계 간 이탈률 계산
2. 가장 큰 이탈이 발생하는 구간 특정
3. 이탈 구간별 원인 추정:
   - UX 문제 (너무 복잡한 단계)
   - 메시지 문제 (가치 제안이 불명확)
   - 신뢰 문제 (정산 구조 불신)
   - 기술 문제 (KYC, UID 연결 실패)
4. 각 이탈 구간별 개선 제안 (우선순위 순)

research/ga4-funnel-2026-04-08.md로 저장해줘.
```

---

## 05. 실시간 트래픽 모니터링

```
GA4 MCP의 realtime report를 사용해서
ReboundX(520538981)의 현재 실시간 트래픽 상황을 확인해줘.

데이터 요청:
- dimensions: unifiedScreenName (현재 활성 페이지)
- metrics: activeUsers
- 추가: country별 실시간 사용자 수

확인 항목:
1. 현재 접속 중인 사용자 수
2. 가장 많이 보고 있는 페이지 TOP 5
3. 실시간 국가별 분포
4. 특이 사항 (평소 대비 급증/급감 여부)

캠페인 실행 후 효과 확인용:
- "방금 트윗/텔레그램 공지를 올렸는데 반응이 오고 있는지 확인해줘"
- 게시 후 30분~1시간 후에 실행하면 즉각적인 트래픽 반응 체크 가능

결과를 간단히 요약해줘 (파일 저장 불필요, 화면에 출력).
```

---

## 06. 디바이스 및 브라우저별 UX 이슈 탐지

```
GA4 MCP로 ReboundX(520538981)의
최근 14일간 디바이스/브라우저별 성과를 분석해줘.

데이터 요청 1 — 디바이스:
- dimensions: deviceCategory
- metrics: totalUsers, sessions, bounceRate, engagementRate, averageSessionDuration, conversions
- date_range: 최근 14일

데이터 요청 2 — 브라우저:
- dimensions: browser
- metrics: totalUsers, bounceRate, engagementRate
- limit: 10

데이터 요청 3 — 모바일 운영체제:
- dimensions: operatingSystem, deviceCategory
- metrics: totalUsers, bounceRate
- dimension_filter: deviceCategory = "mobile"

분석:
1. 모바일 vs 데스크톱 전환율 차이
2. 특정 브라우저에서 이탈률이 비정상적으로 높은 경우 탐지
3. 동남아 타겟 특성 반영: 모바일 최적화 수준 평가
4. UX 개선이 필요한 디바이스/브라우저 조합 특정

개선 제안:
- 모바일 전환율이 데스크톱보다 현저히 낮은 경우 → 모바일 UX 개선 포인트
- 특정 브라우저 이슈 → 기술팀 전달용 요약

research/ga4-device-analysis-2026-04-08.md로 저장해줘.
```

---

## 07. 유입 키워드 및 검색 성과 분석

```
GA4 MCP로 ReboundX(520538981)의
최근 30일간 검색 유입 성과를 분석해줘.

데이터 요청 1 — 오가닉 검색:
- dimensions: sessionSource, sessionMedium, landingPage
- metrics: sessions, totalUsers, engagementRate, conversions
- dimension_filter: sessionMedium = "organic"
- date_range: 최근 30일
- limit: 30

데이터 요청 2 — 랜딩 페이지별 오가닉 성과:
- dimensions: landingPage
- metrics: sessions, bounceRate, averageSessionDuration, conversions
- dimension_filter: sessionMedium = "organic"
- order_by: sessions 내림차순
- limit: 20

분석:
1. 오가닉 검색으로 가장 많이 유입되는 페이지 TOP 10
2. 검색 유입 후 전환으로 이어지는 페이지 특정
3. 검색 유입은 높지만 이탈률도 높은 페이지 (콘텐츠 미스매치 의심)
4. 거래소 가이드 페이지별 검색 유입 비교

SEO 전략 제안:
- 강화해야 할 랜딩 페이지 (유입 있고 전환도 좋은)
- 개선해야 할 랜딩 페이지 (유입은 있으나 이탈 높은)
- 신규 콘텐츠 제작이 필요한 키워드 영역

research/ga4-search-performance-2026-04-08.md로 저장해줘.
```

---

## 08. 신규 vs 재방문 사용자 행동 비교

```
GA4 MCP로 ReboundX(520538981)의
최근 30일간 신규 vs 재방문 사용자 행동을 비교해줘.

데이터 요청 1 — 신규 vs 재방문 개요:
- dimensions: newVsReturning
- metrics: totalUsers, sessions, engagementRate, averageSessionDuration, conversions
- date_range: 최근 30일

데이터 요청 2 — 신규 사용자 유입 채널:
- dimensions: newVsReturning, sessionDefaultChannelGroup
- metrics: totalUsers, conversions
- dimension_filter: newVsReturning = "new"

데이터 요청 3 — 재방문 사용자 행동:
- dimensions: newVsReturning, pagePath
- metrics: screenPageViews, averageSessionDuration
- dimension_filter: newVsReturning = "returning"
- limit: 15

분석:
1. 신규 vs 재방문 전환율 차이
2. 신규 사용자가 가장 많이 유입되는 채널
3. 재방문 사용자가 가장 많이 보는 페이지 (정산 확인 대시보드인지?)
4. 신규 → 재방문 전환에 성공하는 사용자의 특성

인사이트:
- 신규 사용자 온보딩 메시지 최적화 방향
- 재방문 유도를 위한 리텐션 전략 제안
- 재방문 사용자를 레퍼럴로 전환시키는 전략

research/ga4-new-vs-returning-2026-04-08.md로 저장해줘.
```

---

## 09. 주간 전환 트렌드 추적

```
GA4 MCP로 ReboundX(520538981)의
최근 8주간 주간 전환 트렌드를 추적해줘.

데이터 요청:
- dimensions: week (또는 date를 주 단위로 그룹핑)
- metrics: totalUsers, newUsers, conversions, engagementRate
- date_range: 최근 56일 (8주)
- order_by: date 오름차순

추가 요청 — 주간별 채널 분포:
- dimensions: week, sessionDefaultChannelGroup
- metrics: totalUsers, conversions
- date_range: 최근 56일

분석:
1. 주간별 유입/전환 추이 그래프 (텍스트 기반 차트)
2. 전환율이 급증/급감한 주 특정 + 원인 추정
3. 채널별 주간 트렌드 (성장 중인 채널 vs 하락 중인 채널)
4. 계절성 또는 이벤트 연동 패턴 발견 여부

전략 반영:
- 전환율이 높았던 주의 콘텐츠/캠페인 활동 역추적
- 하락 추세인 경우 대응 액션 플랜
- 다음 4주 예상 트렌드와 목표 설정

research/ga4-weekly-trend-2026-04-08.md로 저장해줘.
```

---

## 10. 커스텀 이벤트 및 전환 설정 점검

```
GA4 MCP로 ReboundX(520538981)의
현재 설정된 커스텀 디멘션, 메트릭, 이벤트를 점검해줘.

실행할 도구:
1. get_property_details (Property ID: 520538981)
   → 프로퍼티 기본 설정 확인
2. get_custom_dimensions_and_metrics (Property ID: 520538981)
   → 커스텀 디멘션/메트릭 목록 확인
3. list_property_annotations (Property ID: 520538981)
   → 주석(annotation) 확인

점검 항목:
1. brand-brief.md에 명시된 주요 전환 이벤트가 GA4에 실제로 설정되어 있는지 확인:
   - 거래소 연결 완료 (UID 연결 포함)
   - 첫 정산 확인
   - 레퍼럴 링크 공유
2. 누락된 커스텀 이벤트가 있는지 체크
3. 추가로 트래킹하면 유용할 이벤트 제안:
   - 거래소 선택 단계
   - KYC 가이드 페이지 도달
   - 에어드랍 계산기 사용
   - Perpdex 비교 페이지 인터랙션
4. 주석에 기록된 캠페인/이벤트 히스토리 정리

결과를 research/ga4-setup-audit-2026-04-08.md로 저장해줘.
```

---

## 사용 팁

- **Property ID**: ReboundX GA4 = `520538981` (brand-brief.md에 명시)
- **날짜 자동화**: "오늘 날짜를 파일명에 넣어줘"로 실행 시점 기준 저장
- **실시간 확인**: 캠페인/게시물 발행 직후 05번 프롬프트로 즉시 반응 확인
- **주간 루틴**: 01, 04, 09번은 매주 월요일 실행 추천
- **월간 루틴**: 03, 08, 10번은 매월 초 실행으로 전략 리뷰에 활용
