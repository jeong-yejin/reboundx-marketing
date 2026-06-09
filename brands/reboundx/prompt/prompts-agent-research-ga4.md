# Agent-Research + GA4 MCP 결합 프롬프트 10선
> ReboundX 전용 | 외부 리서치 + 내부 데이터를 결합한 분석 & 전략
> 사용법: `cd ~/Desktop/MKT/brands/reboundx` → `claude` 실행 후 프롬프트 입력

---

## 01. 경쟁사 동향 + 자사 트래픽 변화 상관 분석

```
아래 두 작업을 병렬로 실행해줘.

작업 A — Agent-Research:
트위터에서 "crypto rebate" "fee cashback" "trading rebate" 키워드로
최근 14일간 경쟁 플랫폼(tethermax, tradeback 등)의 게시물과 캠페인을 수집해줘.
각 플랫폼별 게시물 수, 주요 메시지, 프로모션 내용 정리.

작업 B — GA4 MCP (Property ID: 520538981):
동일한 14일간 ReboundX의 일별 데이터를 가져와줘.
- dimensions: date, sessionDefaultChannelGroup
- metrics: totalUsers, newUsers, sessions, conversions
- date_range: 최근 14일

두 데이터를 결합해서 분석:
1. 경쟁사가 대형 캠페인을 실행한 날 → ReboundX 트래픽에 영향이 있었는지 (유입 감소?)
2. 경쟁사 메시지와 ReboundX 메시지의 포지셔닝 비교
3. 경쟁사 캠페인에 대응할 수 있는 즉시 실행 가능한 카운터 콘텐츠 3개
4. 경쟁사가 놓치고 있는 포인트 중 ReboundX가 선점할 수 있는 것

outputs/competitive-vs-traffic-{오늘 날짜 YYYY-MM-DD}.md로 저장해줘.
```

---

## 02. Perp DEX 시장 뉴스 + 관련 페이지 트래픽 반응 분석

```
아래 두 작업을 병렬로 실행해줘.

작업 A — Agent-Research:
최근 7일간 Perp DEX 관련 주요 뉴스를 수집해줘.
- Hyperliquid, variational, edgeX 등 주요 Perp DEX 뉴스
- ReboundX 파트너(GRVT, Lighter, edgeX, Variational) 관련 뉴스
- 에어드랍 발표, 토큰 상장, 거래량 급증 이벤트

작업 B — GA4 MCP (520538981):
같은 7일간 Perpdex 관련 페이지 트래픽을 가져와줘.
- dimensions: date, pagePath
- metrics: screenPageViews, totalUsers, engagementRate
- dimension_filter: pagePath contains "/perpdex" OR pagePath contains "/exchanges"
- date_range: 최근 7일

결합 분석:
1. 특정 Perp DEX 뉴스가 발표된 날 → 해당 거래소 페이지 트래픽 변화 매핑
2. 뉴스가 트래픽으로 전환된 사례 vs 전환되지 않은 사례 비교
3. 뉴스 발생 시 즉시 연계할 수 있는 콘텐츠 대응 SOP 초안
4. 다음 주 예상 뉴스 이벤트 + 사전 준비할 콘텐츠 리스트

outputs/perpdex-news-vs-traffic-{오늘 날짜 YYYY-MM-DD}.md로 저장해줘.
```

---

## 03. 미국 규제 뉴스 + 미국 유저 행동 변화 분석

```
아래 두 작업을 병렬로 실행해줘.

작업 A — Agent-Research:
최근 30일간 미국 크립토 규제 관련 주요 이벤트를 조사해줘.
- SEC, CFTC 발표
- 크립토 관련 법안/판결
- 주요 거래소 규제 조치
- 각 이벤트 날짜와 내용을 타임라인으로 정리

작업 B — GA4 MCP (520538981):
같은 30일간 미국 사용자 데이터를 가져와줘.
- dimensions: date, landingPage
- metrics: totalUsers, sessions, bounceRate, conversions
- dimension_filter: country = "United States"
- date_range: 최근 30일

결합 분석:
1. 규제 이벤트 발생 전후 미국 유저 트래픽 변화 비교
2. 규제 뉴스가 나온 날 이탈률이 증가했는지 확인
3. 규제 민감 시기에 효과적인 콘텐츠 유형 파악
   (교육형이 더 효과적인지? 신뢰 구축형이 더 효과적인지?)
4. 규제 이벤트 대응 콘텐츠 템플릿 3개 작성
   (예: "SEC 발표 이후에도 안전하게 수수료를 절감하는 방법")
5. 수익 보장/투자 권유 표현 체크리스트 업데이트

research/us-regulation-vs-traffic-{오늘 날짜 YYYY-MM-DD}.md로 저장해줘.
```

---

## 04. 동남아 KOL 리서치 + 동남아 유입 채널 분석

```
아래 두 작업을 병렬로 실행해줘.

작업 A — Agent-Research:
동남아 4개국(베트남, 태국, 인도네시아, 필리핀)에서 활동 중인
크립토 KOL/인플루언서를 조사해줘.
- 국가별 5명씩 (총 20명)
- 트위터/텔레그램 팔로워 수, 주요 콘텐츠 주제, 최근 활동
- 리베이트/어필리에이트 관련 콘텐츠를 발행한 이력이 있는지

작업 B — GA4 MCP (520538981):
최근 30일간 동남아 4개국 유입 데이터를 가져와줘.
- dimensions: country, sessionSource, sessionMedium
- metrics: totalUsers, sessions, engagementRate, conversions
- dimension_filter: country in ["Vietnam", "Thailand", "Indonesia", "Philippines"]
- date_range: 최근 30일

결합 분석:
1. 국가별 현재 유입 채널 구조 (어디서 오고 있는지?)
2. 텔레그램 유입 비중 확인 (brand-brief의 가설: 텔레그램 의존도 높음)
3. KOL 리스트와 현재 유입 채널을 매칭 → 가장 임팩트 있을 KOL 협업 우선순위
4. 국가별 KOL 아웃리치 전략 (채널, 메시지, 인센티브 구조)
5. 국가별 KOL 아웃리치 초기 메시지 초안 (영어)

outputs/sea-kol-vs-traffic-{오늘 날짜 YYYY-MM-DD}.md로 저장해줘.
```

---

## 05. 파트너 거래소 뉴스 + 거래소별 가이드 페이지 성과

```
아래 두 작업을 병렬로 실행해줘.

작업 A — Agent-Research:
ReboundX 파트너 거래소(OKX, Binance, Backpack, Bybit, GRVT, Lighter, edgeX,
Variational)의 최근 7일 뉴스를 수집해줘.
- 신규 기능, 상장, 수수료 변경, 이벤트, 파트너십 등

작업 B — GA4 MCP (520538981):
같은 7일간 거래소 가이드 페이지별 트래픽을 가져와줘.
- dimensions: pagePath, date
- metrics: screenPageViews, totalUsers, bounceRate, conversions
- dimension_filter: pagePath contains "/guide/" OR pagePath contains "/exchanges/"
- date_range: 최근 7일

결합 분석:
1. 거래소별 뉴스 이벤트 vs 해당 가이드 페이지 트래픽 상관관계
2. 뉴스가 있었지만 트래픽이 반응하지 않은 거래소 → 콘텐츠 연계 누락
3. 트래픽은 높지만 전환(UID 연결)이 낮은 거래소 가이드 → UX/카피 문제
4. 각 거래소별 이번 주 콘텐츠 액션 제안:
   | 거래소 | 뉴스 | 페이지 성과 | 액션 |
5. 즉시 활용할 트윗 초안 3개 (뉴스 연계형)

outputs/partner-news-vs-pages-{오늘 날짜 YYYY-MM-DD}.md로 저장해줘.
```

---

## 06. 에어드랍 트렌드 + 에어드랍 계산기 사용 패턴

```
아래 두 작업을 병렬로 실행해줘.

작업 A — Agent-Research:
현재 진행 중이거나 예정된 Perp DEX 에어드랍을 조사해줘.
- ReboundX 파트너 DEX 우선
- 에어드랍 예상 시기, 참여 조건, 예상 가치
- 트위터에서 "perp dex airdrop" 트렌드

작업 B — GA4 MCP (520538981):
최근 30일간 에어드랍 포인트 계산기 페이지(/en/perpdex/point-calculator) 사용 데이터를 가져와줘.
- dimensions: date, country, deviceCategory
- metrics: screenPageViews, totalUsers, averageSessionDuration, engagementRate
- dimension_filter: pagePath contains "/perpdex"
- date_range: 최근 30일

결합 분석:
1. 에어드랍 발표 시점과 계산기 페이지 트래픽 급증 시점 매핑
2. 계산기 페이지 사용자의 지역 분포 (어떤 국가에서 관심이 높은지?)
3. 모바일 vs 데스크톱 사용 패턴
4. 에어드랍 이벤트별 콘텐츠 대응 타이밍 최적화
5. "에어드랍 + 리베이트 이중 혜택" 메시지로 연결하는 콘텐츠 5개
   - 트윗 3개 + 텔레그램 메시지 2개 (수익 보장 표현 금지)

outputs/airdrop-vs-calculator-{오늘 날짜 YYYY-MM-DD}.md로 저장해줘.
```

---

## 07. 크립토 트레이딩 커뮤니티 트렌드 + 소셜 유입 분석

```
아래 두 작업을 병렬로 실행해줘.

작업 A — Agent-Research:
레딧(r/CryptoCurrency, r/ethfinance, r/defi)과 트위터에서
최근 7일간 "trading fees" "fee rebate" "perp dex" 관련 화제 게시물을 수집해줘.
- 각 게시물의 반응(업보트/리트윗/댓글 수)
- 커뮤니티에서 가장 공감을 얻은 메시지 톤과 프레이밍
- ReboundX가 언급되었는지 여부

작업 B — GA4 MCP (520538981):
같은 7일간 소셜 미디어 유입 데이터를 가져와줘.
- dimensions: sessionSource, date
- metrics: totalUsers, sessions, engagementRate, conversions
- dimension_filter: sessionDefaultChannelGroup = "Organic Social"
- date_range: 최근 7일

결합 분석:
1. 커뮤니티에서 화제인 주제와 ReboundX 소셜 유입 트렌드 비교
2. ReboundX가 아직 참여하지 않고 있는 화제 주제 특정
3. 커뮤니티에서 공감받는 메시지 톤 → ReboundX 콘텐츠에 적용할 인사이트
4. 레딧 참여 전략 제안 (댓글형? 독립 포스트형?)
5. 이번 주 소셜 콘텐츠에 반영할 커뮤니티 트렌드 TOP 3
6. 즉시 사용 가능한 레딧 댓글 초안 2개 + 트윗 2개

output/community-vs-social-traffic-{오늘 날짜 YYYY-MM-DD}.md로 저장해줘.
```

---

## 08. SEO 키워드 리서치 + 오가닉 검색 성과 크로스 분석

```
아래 두 작업을 병렬로 실행해줘.

작업 A — Agent-Research:
아래 키워드 그룹의 검색 트렌드와 경쟁 현황을 조사해줘.
- "crypto fee rebate" / "trading fee cashback" / "exchange rebate"
- "[거래소명] rebate" (OKX, Bybit, binance, Backpack 각각)
- "perp dex comparison" / "best perpetual exchange"
- "crypto airdrop calculator"
각 키워드: 추정 월간 검색량, SERP 상위 3개 사이트, 콘텐츠 형태

작업 B — GA4 MCP (520538981):
최근 30일간 오가닉 검색 유입 데이터를 가져와줘.
- dimensions: landingPage, sessionSource
- metrics: totalUsers, sessions, bounceRate, averageSessionDuration, conversions
- dimension_filter: sessionMedium = "organic"
- date_range: 최근 30일
- order_by: sessions 내림차순
- limit: 30

결합 분석:
1. 현재 오가닉 유입이 있는 키워드/페이지와 리서치 키워드 매핑
2. 검색 수요는 높지만 ReboundX가 아직 공략하지 못한 키워드 갭
3. 유입은 있지만 전환이 안 되는 페이지 → 콘텐츠 최적화 대상
4. 우선 공략 키워드 10개 선정 + 각 키워드별 콘텐츠 제목/구조 초안
5. 기존 페이지 SEO 최적화 제안 (메타 타이틀, H1, 내부 링크)

outputs/seo-vs-organic-{오늘 날짜 YYYY-MM-DD}.md로 저장해줘.
```

---

## 09. 트레이딩 컴피티션 벤치마킹 + 캠페인 트래픽 효과 분석

```
아래 두 작업을 병렬로 실행해줘.

작업 A — Agent-Research:
최근 3개월간 크립토 업계 트레이딩 컴피티션 사례를 조사해줘.
- ReboundX 파트너 거래소(Backpack, BingX, Bybit 등) 중심
- 상금 규모, 참가자 수, 진행 기간, 프로모션 채널
- 성공/실패 사례 패턴

작업 B — GA4 MCP (520538981):
ReboundX의 트레이딩 컴피티션 페이지 관련 데이터를 가져와줘.
- dimensions: pagePath, date, sessionDefaultChannelGroup
- metrics: screenPageViews, totalUsers, newUsers, conversions
- dimension_filter: pagePath contains "competition" OR pagePath contains "contest"
- date_range: 최근 90일

결합 분석:
1. ReboundX 기존 컴피티션의 트래픽 패턴 (론칭 → 진행 → 종료 기간별)
2. 어떤 채널에서 컴피티션 참여자가 유입되었는지
3. 업계 벤치마크 대비 ReboundX 컴피티션 성과 평가
4. 다음 컴피티션 기획 시 개선 포인트:
   - 최적 진행 기간
   - 효과적인 프로모션 채널 조합
   - 상금 구조 제안
   - 사전/중간/마감 홍보 메시지 초안 (트윗 + 텔레그램)
5. 컴피티션 → UID 연결 전환 극대화 전략

research/competition-benchmark-vs-data-{오늘 날짜 YYYY-MM-DD}.md로 저장해줘.
```

---

## 10. 전체 마케팅 효율 진단: 시장 상황 + 자사 퍼포먼스 종합

```
brand-brief.md를 먼저 읽어줘.
그리고 아래 두 작업을 병렬로 실행해줘.

작업 A — Agent-Research (시장 컨텍스트 수집):
1. 최근 30일간 크립토 시장 전반 동향 (BTC 가격 추이, 전체 거래량 트렌드)
2. 리베이트/캐시백 플랫폼 업계 동향
3. 주요 경쟁사 활동 요약
4. Perp DEX 섹터 성장률 및 트렌드
5. 미국/동남아 크립토 시장 특이사항

작업 B — GA4 MCP (520538981, 최근 30일 전체 데이터):
요청 1:
- dimensions: date
- metrics: totalUsers, newUsers, sessions, conversions, engagementRate
- date_range: 최근 30일

요청 2:
- dimensions: country
- metrics: totalUsers, conversions
- limit: 15

요청 3:
- dimensions: sessionDefaultChannelGroup
- metrics: totalUsers, sessions, conversions
- date_range: 최근 30일

요청 4:
- dimensions: pagePath
- metrics: screenPageViews, bounceRate, conversions
- order_by: screenPageViews DESC
- limit: 20

종합 진단 리포트:
1. 시장 환경 요약 (기회 vs 위협)
2. 자사 트래픽/전환 트렌드 요약
3. 시장 성장 대비 자사 성장 비교 (outperform? underperform?)
4. 채널별 ROI 추정 (유입 대비 전환 효율)
5. 지역별 기회 격차 (어디에 더 투자해야 하는지)
6. 페이지별 최적화 우선순위
7. 다음 30일 액션 플랜 (우선순위 순, 구체적 실행 항목)

outputs/marketing-diagnosis-{오늘 날짜 YYYY-MM-DD}.md에 전체 리포트 저장.
outputs/action-plan-{오늘 날짜 YYYY-MM-DD}.md에 액션 플랜만 별도 저장.
```

---

## 사용 팁

- **병렬 실행**: Agent-Research와 GA4 MCP 작업은 서로 의존성이 없으므로 병렬 실행으로 시간 절약
- **주간 루틴 추천**: 01, 02, 05번 → 매주 월요일 / 07번 → 매주 수요일
- **월간 루틴 추천**: 10번 → 매월 초 / 03번 → 규제 이벤트 발생 시 즉시
- **결과 연쇄 활용**: 이 리서치 결과를 ai-marketing-skills 프롬프트의 인풋으로 사용하면 데이터 기반 콘텐츠 생성 가능
- **날짜 자동화**: "오늘 날짜를 파일명에 자동으로 넣어줘"로 실행 시점 기준 저장
