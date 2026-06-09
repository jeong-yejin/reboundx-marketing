# Agent-Research 활용 프롬프트 10선
> ReboundX 전용 | Agent-Research (WebSearch, WebFetch) 기반
> 사용법: `cd ~/Desktop/MKT/brands/reboundx` → `claude` 실행 후 프롬프트 입력

---

## 01. Perp DEX 시장 동향 스캔

```
brand-brief.md를 읽고 Agent-Research를 활용해서 다음 작업을 수행해줘.

조사 대상:
- Hyperliquid, dYdX, GMX, Vertex Protocol, Drift 등 주요 Perp DEX의 최근 2주간 뉴스
- 신규 체인 론칭, 토큰 에어드랍 발표, 거래량 급변동 이벤트
- 트위터(X)에서 "perp dex" "perpetual exchange" 키워드 트렌드

정리 형식:
1. 거래소별 주요 이벤트 요약 (표 형식)
2. ReboundX 파트너 거래소(GRVT, Lighter, edgeX, Variational, Avantis, Dango)에 해당하는 이벤트는 별도 하이라이트
3. 각 이벤트에 대해 ReboundX가 활용할 수 있는 콘텐츠 앵글 제안 1개씩

결과물을 research/perpdex-trends.md로 저장해줘.
```

---

## 02. 경쟁 리베이트 플랫폼 벤치마킹

```
Agent-Research로 아래 경쟁 리베이트 플랫폼을 조사해줘.

조사 대상 플랫폼:
- BingX 공식 리베이트 프로그램
- OKX 공식 어필리에이트
- 8V, CoinCatch 등 리베이트 중개 플랫폼
- 트위터에서 "crypto fee rebate" "trading cashback" 관련 활동 중인 계정

조사 항목 (플랫폼별):
1. 리베이트율 (maker/taker 구분)
2. 정산 주기
3. 지원 거래소 수 (CEX, DEX 각각)
4. 최근 캠페인/프로모션 내용
5. 소셜 미디어 팔로워 수 및 활동 빈도

분석:
- ReboundX와 비교해서 우위 포인트 3가지, 열위 포인트 3가지
- 경쟁사가 하고 있지만 ReboundX가 안 하고 있는 것
- 즉시 트위터/텔레그램에 활용할 수 있는 차별화 메시지 3개

research/competitor-benchmark.md로 저장해줘.
```

---

## 03. 미국 크립토 규제 업데이트 모니터링

```
Agent-Research로 미국 크립토 규제 관련 최신 동향을 조사해줘.

조사 범위:
- SEC, CFTC의 최근 2주간 크립토 관련 발표/조치
- 리베이트/캐시백/어필리에이트 프로그램에 영향을 줄 수 있는 규제 변화
- "crypto affiliate regulation" "rebate compliance" 관련 뉴스
- 주요 크립토 미디어(CoinDesk, The Block, Decrypt) 규제 섹션

정리 형식:
1. 규제 이벤트 타임라인 (날짜 | 기관 | 내용 | 영향도)
2. ReboundX 운영에 직접 영향 가능한 항목은 🔴 표시
3. 콘텐츠 작성 시 주의해야 할 표현 업데이트 사항
4. 규제 변화를 역으로 활용할 수 있는 콘텐츠 앵글 (예: "규제 환경에서도 안전한 수수료 절감 방법")

research/us-regulation-2026.md로 저장해줘.
```

---

## 04. 동남아 크립토 커뮤니티 트렌드 리서치

```
Agent-Research로 동남아 크립토 시장 트렌드를 조사해줘.

조사 지역: 베트남, 태국, 인도네시아, 필리핀
조사 항목:
1. 각 국가별 최근 크립토 채택률 데이터 (Chainalysis, Triple-A 등 소스)
2. 텔레그램에서 인기 있는 크립토 커뮤니티/채널 (국가별 상위 5개)
3. 각 지역에서 활동 중인 크립토 KOL (팔로워 10K+ 기준, 국가별 5명)
4. "fee rebate" "거래 수수료 환급" 관련 현지어 키워드 트렌드
5. 각 국가별 선호 거래소 및 Perp DEX 사용 현황

분석:
- 국가별 ReboundX 침투 가능성 순위 (근거 포함)
- 국가별 최적 진입 전략 요약 (채널, 메시지 톤, KOL 활용 방식)
- 텔레그램 커뮤니티 진입을 위한 초기 메시지 초안 (국가별 영어+현지어)
outputs/sea-community.md로 저장해줘.
```

---

## 05. 파트너 거래소 뉴스 종합 브리핑

```
Agent-Research로 ReboundX 파트너 거래소들의 최근 뉴스를 수집해줘.

파트너 거래소 목록:
- CEX: OKX, BingX, Backpack, Bybit
- Perp DEX: GRVT, Lighter, edgeX, Variational, Avantis, Dango

각 거래소별 조사 항목:
1. 최근 2주간 주요 발표 (신규 기능, 상장, 파트너십 등)
2. 수수료 정책 변경 사항
3. 진행 중이거나 예정된 이벤트/캠페인
4. 소셜 미디어 화제성 (트위터 멘션 트렌드)

정리 후 추가 작업:
- 각 뉴스에 대해 ReboundX가 연계할 수 있는 콘텐츠 아이디어 태그
  (예: [트윗 소재] [텔레그램 공지] [블로그 포스트] [리베이트율 업데이트])
- 이번 주 우선 활용해야 할 뉴스 TOP 3 선정 + 즉시 사용 가능한 트윗 초안

research/partner-news.md로 저장해줘.
```

---

## 06. 크립토 트레이더 페르소나 심화 리서치

```
Agent-Research로 ReboundX 타겟 사용자 페르소나를 심화 조사해줘.

brand-brief.md를 먼저 읽고, 아래 세그먼트별로 조사해줘:

세그먼트 1: 미국 헤비 트레이더 (월 거래량 $100K+)
세그먼트 2: 동남아 리테일 트레이더 (월 거래량 $1K~$10K)
세그먼트 3: Perp DEX 네이티브 트레이더 (CEX 미사용 또는 최소 사용)
세그먼트 4: 크립토 입문자 (거래소 가입 전 단계)

각 세그먼트별 조사:
1. 주로 사용하는 정보 소스 (미디어, 커뮤니티, 인플루언서)
2. 거래소 선택 시 중요하게 보는 기준 상위 5개
3. 수수료에 대한 인식과 행동 패턴
4. 리베이트/캐시백에 대한 인식 수준
5. 레딧, 트위터에서 해당 세그먼트가 자주 사용하는 표현/은어

분석:
- 세그먼트별 ReboundX 온보딩 메시지 최적 프레이밍
- 세그먼트별 전환 트리거 (어떤 메시지가 행동을 유발하는지)
- 세그먼트별 신뢰 장벽과 해소 방법

research/persona-deep-dive.md로 저장해줘.
```

---

## 07. 에어드랍 시즌 콘텐츠 소재 발굴

```
Agent-Research로 현재 진행 중이거나 예정된 크립토 에어드랍 이벤트를 조사해줘.

조사 범위:
- ReboundX 파트너 Perp DEX(GRVT, Lighter, edgeX, Variational, Avantis, Dango)의 에어드랍 현황
- 주요 Perp DEX 에어드랍 예정 프로젝트 (DeFiLlama, Airdrop 트래커 참조)
- 트위터에서 "perp dex airdrop" "dex farming" 키워드 트렌드

정리:
1. 에어드랍 프로젝트 리스트 (프로젝트명 | 예상 시기 | 참여 조건 | ReboundX 연계 가능 여부)
2. ReboundX 에어드랍 계산기(/en/perpdex)와 연계할 수 있는 프로젝트 특정
3. 에어드랍 + 리베이트 이중 혜택을 강조하는 콘텐츠 앵글 5개
4. 즉시 사용 가능한 트윗 3개 + 텔레그램 메시지 2개
   (주의: "수익 보장" 표현 금지. "수수료를 돌려받으면서 에어드랍 참여 기회까지" 식으로)

research/airdrop-opportunities-2026-04-08.md로 저장해줘.
```

---

## 08. 크립토 미디어 & 인플루언서 아웃리치 리스트 구축

```
Agent-Research로 ReboundX 홍보에 활용할 미디어 및 인플루언서 리스트를 구축해줘.

조사 대상:

A. 크립토 미디어 (영문)
- 기사 기고 또는 스폰서 콘텐츠가 가능한 미디어 10개
- 각 미디어의 월간 트래픽 추정치, 주요 독자층, 콘텐츠 형태

B. 트위터(X) 인플루언서 (미국 타겟)
- 거래/트레이딩 관련 팔로워 50K+ 계정 10개
- 각 계정의 콘텐츠 스타일, 최근 스폰서 콘텐츠 여부, 예상 협업 비용 범위

C. 텔레그램 KOL (동남아 타겟)
- 국가별(베트남, 태국, 인도네시아, 필리핀) 크립토 커뮤니티 운영자 각 3명
- 팔로워 규모, 커뮤니티 활동 수준, 레퍼럴 프로그램 수용도

각 대상에 대해:
- 아웃리치 우선순위 (상/중/하)
- 아웃리치 초기 메시지 초안 (ReboundX의 Perp DEX 제휴 수 업계 최다 포인트 포함)

research/outreach-list.md로 저장해줘.
```

---

## 09. SEO 키워드 & 콘텐츠 갭 분석

```
Agent-Research로 ReboundX 관련 SEO 키워드를 조사해줘.

조사 항목:

1. 핵심 키워드 그룹 (영문 기준):
   - "crypto fee rebate" 관련 키워드 20개 (검색량 추정 포함)
   - "perp dex comparison" 관련 키워드 15개
   - "trading fee cashback" 관련 키워드 15개
   - 파트너 거래소별 "[거래소명] rebate" "[거래소명] fee discount" 키워드

2. 경쟁 분석:
   - 각 키워드 그룹에서 상위 노출 중인 사이트/페이지 조사
   - 상위 페이지의 콘텐츠 형태, 길이, 구조 분석

3. 콘텐츠 갭:
   - 검색 수요는 있으나 양질의 콘텐츠가 부재한 키워드 특정
   - ReboundX가 즉시 공략할 수 있는 롱테일 키워드 10개

4. 콘텐츠 제안:
   - 우선순위 높은 키워드별 콘텐츠 제목 + 구조 (H1, H2) 초안
   - 예상 트래픽 임팩트 순으로 정렬

research/seo-keywords.md로 저장해줘.
```

---

## 10. 트레이딩 컴피티션 벤치마킹 & 기획 소재 수집

```
Agent-Research로 크립토 업계 트레이딩 컴피티션 사례를 조사해줘.

조사 범위:
- 최근 3개월간 진행된 주요 트레이딩 컴피티션 (CEX + DEX)
- Bybit, BingX, Backpack 등 ReboundX 파트너 거래소의 컴피티션 히스토리
- 트위터에서 "trading competition crypto" "trading tournament" 인기 게시물

각 사례별 수집 항목:
1. 운영 거래소 및 공동 주최사
2. 상금 규모 및 구조
3. 참가 조건 및 참가자 수
4. 진행 기간 및 순위 산정 방식
5. 프로모션 채널 및 방식

분석:
- 성공 사례 vs 실패 사례 패턴 분석
- ReboundX의 perp-dex day, Backpack Trading Competition과 비교해서 개선할 수 있는 포인트
- 다음 컴피티션 기획 시 참고할 포맷/구조 제안 3가지
- 컴피티션 사전 홍보용 트윗 카피 3개 + 텔레그램 공지 1개

research/competition-benchmark.md로 저장해줘.
```

---

## 사용 팁

- **날짜 자동화**: "오늘 날짜를 파일명에 자동으로 넣어줘"라고 추가하면 실행 시점 날짜로 저장
- **조합 활용**: 이 리서치 결과를 ai-marketing-skills나 GA4 MCP 프롬프트의 입력으로 사용하면 데이터 기반 콘텐츠 생성 가능
- **주간 루틴**: 01, 05, 07번은 매주 실행 추천 → `/loop 7d` 활용 가능
