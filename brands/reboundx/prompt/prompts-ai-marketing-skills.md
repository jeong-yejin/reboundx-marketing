# AI-Marketing-Skills 활용 프롬프트 10선
> ReboundX 전용 | content-ops, growth-engine, expert-panel 스킬 기반
> 사용법: `cd ~/Desktop/MKT/brands/reboundx` → `claude` 실행 후 프롬프트 입력

---

## 01. Expert Panel로 랜딩 페이지 카피 품질 검증

```
brand-brief.md를 읽고 content-ops 스킬로 아래 랜딩 페이지 카피를 작성해줘.

대상 페이지: ReboundX 메인 랜딩 페이지
타겟: 미국 중급 트레이더 (월 거래량 $50K+, 수수료 부담을 인식하고 있음)

작성할 섹션:
1. 히어로 섹션 (헤드라인 + 서브카피 + CTA)
2. 작동 방식 3단계 설명 (아이콘 + 한 줄 설명)
3. 파트너 거래소 섹션 (CEX 4개 + Perp DEX 6개 = 10개 거래소 강조)
4. 정산 투명성 섹션 (온체인 검증 + 24시간 정산 SLA 강조)
5. FAQ 섹션 (5문 5답)

각 섹션 카피를 영어로 2개 버전(A/B) 작성한 후,
expert-panel 스킬로 두 버전을 비교 평가해줘.
평가 기준: 전환율 최적화, 신뢰 구축, 규제 컴플라이언스, AI 문체 탐지

최종 승자 버전을 outputs/landing-page-copy.md로 저장해줘.
```

---

## 02. Growth Engine으로 트위터 헤드라인 A/B 실험 설계

```
brand-brief.md를 읽고 growth-engine 스킬을 사용해서
트위터 헤드라인 A/B 실험을 설계해줘.

실험 목적: 미국 타겟 트위터 게시물의 클릭률(CTR) 최적화
테스트 변수: 헤드라인 프레이밍 방식

변수 옵션 (5개 variants):
A. 수치 중심: "Traders using ReboundX save an average of $X/month in fees"
B. 질문형: "Still paying full trading fees? Here's what smart traders do differently"
C. 사회적 증거: "10,000+ traders already getting their fees back across 10 exchanges"
D. 두려움 자극: "Every trade costs you more than you think — unless you're getting rebates"
E. 교육형: "How fee rebates work: a 60-second explainer for crypto traders"

각 variant에 대해:
1. 완성된 트윗 전문 (280자 이내, 영어, 해시태그 3개 포함)
2. 타겟 반응 예측 (어떤 세그먼트에 효과적일지)

growth-engine으로 실험 생성:
- agent: twitter
- hypothesis: "수치 중심 프레이밍이 중급 트레이더에게 가장 높은 CTR을 보일 것"
- variable: headline_framing
- metric: click_through_rate
- batch-mode 사용

outputs/twitter-ab-experiment.md로 저장해줘.
```

---

## 03. 텔레그램 온보딩 시퀀스 제작 + Expert Panel 검증

```
brand-brief.md를 읽고 content-ops 스킬로
텔레그램 신규 멤버 온보딩 메시지 시퀀스를 작성해줘.

타겟: 동남아 크립토 트레이더 (텔레그램 커뮤니티에 처음 입장한 사용자)
언어: 영어 (현지화 가능한 간결한 문장)
톤: 친근하지만 전문적. 이모지 적절히 사용.

시퀀스 (총 7개 메시지, 3일간 자동 발송):

Day 0 (입장 직후):
1. 환영 메시지 + ReboundX 한 줄 소개 + 핵심 혜택
2. 3단계 시작 가이드 (가입 → UID 연결 → 자동 리베이트)

Day 1:
3. 파트너 거래소 선택 가이드 (CEX vs Perp DEX 비교)
4. 정산 구조 설명 (24시간 자동 정산, 온체인 투명성)

Day 2:
5. 자주 묻는 질문 TOP 3
6. 에어드랍 계산기 소개 (/en/perpdex 링크 포함)

Day 3:
7. 레퍼럴 프로그램 소개 + 공유 CTA

각 메시지 작성 후 expert-panel 스킬로 전체 시퀀스를 평가해줘.
평가 기준: 이탈 방지, 정보 과부하 여부, 행동 유도 효과, 신뢰 구축

outputs/telegram-onboarding-sequence.md로 저장해줘.
```

---

## 04. Perp DEX 비교 콘텐츠 시리즈 제작

```
brand-brief.md를 읽고 content-ops 스킬로
ReboundX 파트너 Perp DEX 비교 콘텐츠 시리즈를 작성해줘.

대상 거래소: GRVT, Lighter, edgeX, Variational, Avantis, Dango

작성할 콘텐츠:

1. 종합 비교표 (표 형식)
   - 지원 체인 / 수수료 구조 / 최대 레버리지 / 지원 자산 수 / 리베이트율
   - ReboundX를 통한 추가 리베이트 혜택 별도 행으로 표시

2. 거래소별 1분 요약 카드 (각 거래소당 150단어 이내)
   - 핵심 특징 3줄
   - 추천 트레이더 유형
   - ReboundX 리베이트 혜택

3. "어떤 Perp DEX를 선택해야 할까?" 의사결정 플로우차트 텍스트 버전
   - 트레이딩 스타일별 추천 경로

4. 트위터 스레드 (6개 트윗) — 6개 Perp DEX를 한 스레드로 소개
   - 각 트윗 280자 이내
   - 마지막 트윗: ReboundX 링크 + 리베이트 CTA

전체 콘텐츠를 expert-panel로 검증 (컨버전 최적화 + 교육 효과 기준)

outputs/perpdex-comparison-series.md로 저장해줘.
```

---

## 05. 주간 콘텐츠 캘린더 자동 생성

```
brand-brief.md를 읽고 content-ops 스킬로
다음 주(월~일) 콘텐츠 캘린더를 생성해줘.

채널별 발행 빈도:
- 트위터(X): 주 5회 (월~금)
- 텔레그램: 주 3회 (월/수/금)
- 블로그/가이드: 주 1회 (수)

각 게시물에 포함할 정보:
| 날짜 | 채널 | 콘텐츠 유형 | 타겟 지역 | 완성 카피 | 해시태그 | CTA |

콘텐츠 유형 믹스 (주간 기준):
- 교육형 40% (리베이트 구조, Perp DEX 비교, 수수료 절감 팁)
- 인증형 25% (정산 내역 캡처 형식, 사용자 후기 형식)
- 커뮤니티형 20% (투표, Q&A, 밈)
- 프로모션형 15% (이벤트, 컴피티션, 신규 거래소 추가)

조건:
- 미국 타겟 콘텐츠와 동남아 타겟 콘텐츠 비율 = 6:4
- 모든 카피는 영어로 작성
- 수익 보장, 투자 권유 표현 절대 금지
- 파트너 거래소 10개를 골고루 노출 (편중 금지)

outputs/content-calendar-week-2026-04-13.md로 저장해줘.
```

---

## 06. 레퍼럴 프로그램 랜딩 페이지 카피 + 이메일 시퀀스

```
brand-brief.md를 읽고 content-ops 스킬로
레퍼럴 프로그램 전용 랜딩 페이지와 이메일 시퀀스를 작성해줘.

A. 랜딩 페이지 카피 (영어)
타겟: 기존 ReboundX 사용자 중 레퍼럴 공유 의향이 있는 트레이더

섹션:
1. 히어로: "Share ReboundX. Earn More Rebates." 컨셉
2. 레퍼럴 구조 시각화 (텍스트): 내가 공유 → 친구 가입 → 둘 다 리베이트 증가
3. 3단계 참여 방법
4. 예상 리베이트 시뮬레이션 (월 거래량 $10K 기준)
5. 자주 묻는 질문 3개
6. CTA: "Get Your Referral Link"

B. 이메일 시퀀스 (기존 유저 대상, 3통)
- Email 1: 레퍼럴 프로그램 런칭 안내
- Email 2: 성공 사례 + 리베이트 수치 시각화
- Email 3: 마감 임박 리마인더 (한시적 보너스가 있는 경우)

각 이메일: 제목 2개 옵션 + 본문 + CTA

expert-panel로 전체 카피 검증 후 최종본 저장.
outputs/referral-landing-email.md로 저장해줘.
```

---

## 07. 정산 투명성 콘텐츠 패키지

```
brand-brief.md를 읽고 content-ops 스킬로
ReboundX의 정산 투명성을 강조하는 콘텐츠 패키지를 제작해줘.

배경: 사용자 상태 3번 — "정산과 출금 구조를 신뢰하지 못하는 사용자"를 위한 콘텐츠

작성할 콘텐츠:

1. 트위터 스레드 (5트윗): "ReboundX 정산은 이렇게 작동합니다"
   - 트윗 1: 후킹 (거래 수수료가 실제로 돌아오는 과정)
   - 트윗 2: 정산 프로세스 도식화 (텍스트)
   - 트윗 3: 온체인 검증 방법
   - 트윗 4: 24시간 SLA 약속
   - 트윗 5: CTA (대시보드 확인 유도)

2. 텔레그램 FAQ 핀 메시지 (5문 5답)
   - 정산 시점, 출금 방법, 리베이트 계산 방식, 거래소 연결 해제 시, 최소 출금 금액

3. 대시보드 UX 마이크로카피 (10개)
   - 정산 예정 금액 / 정산 완료 / 출금 가능 / 출금 진행 중 / 출금 완료
   - 각 상태별 툴팁 텍스트

4. 블로그 포스트 구조 (H1~H3 + 각 섹션 요약)
   - 제목: "How ReboundX Settlement Works: Full Transparency"

expert-panel로 전체 패키지 신뢰 구축 효과 평가.
outputs/transparency-content-package.md로 저장해줘.
```

---

## 08. Growth Engine 실험: 텔레그램 CTA 최적화

```
brand-brief.md를 읽고 growth-engine 스킬로
텔레그램 CTA 버튼 텍스트 최적화 실험을 설계해줘.

실험 목적: 텔레그램 공지 메시지의 CTA 클릭률 최적화
테스트 변수: CTA 버튼 텍스트

컨텍스트: 파트너 거래소 신규 추가 공지 메시지에 붙는 CTA

변수 옵션 (6개 variants):
A. "Start Getting Rebates →"
B. "Connect [거래소명] Now"
C. "See Your Rebate Rate"
D. "How Much Can You Save?"
E. "Claim Your Fee Rebate"
F. "Join 10,000+ Traders"

각 variant에 대해:
1. 전체 텔레그램 메시지 본문과 함께 완성된 형태로 작성
2. 타겟 사용자 상태별 예상 반응 (4가지 사용자 상태 기준)

growth-engine으로 실험 생성:
- agent: telegram
- hypothesis: "행동 구체화형 CTA(B)가 범용적인 CTA(A)보다 클릭률이 15% 이상 높을 것"
- variable: cta_text
- metric: click_through_rate
- batch-mode 사용

outputs/telegram-cta-experiment.md로 저장해줘.
```

---

## 09. 월간 콘텐츠 성과 리뷰 + 다음 달 전략 제안

```
outputs/ 폴더의 모든 파일과 brand-brief.md를 읽어줘.

content-ops 스킬로 이번 달 콘텐츠 활동을 리뷰하고
다음 달 전략을 제안해줘.

리뷰 항목:
1. 이번 달 발행한 콘텐츠 수 (채널별)
2. 콘텐츠 유형별 분포 (교육형/인증형/커뮤니티형/프로모션형)
3. 지역별 분포 (미국 vs 동남아)
4. 파트너 거래소별 노출 빈도
5. 누락된 주제나 세그먼트

다음 달 전략 제안:
1. 콘텐츠 유형 믹스 조정 (근거 포함)
2. 채널별 발행 빈도 조정
3. 신규 시도할 콘텐츠 포맷 3개 (예: 트위터 스페이스, AMA, 유저 인터뷰 등)
4. 파트너 거래소별 콘텐츠 밸런스 계획
5. 다음 달 주차별 테마 제안

expert-panel로 전략 품질 평가 후 최종본 저장.
outputs/monthly-content-review-2026-04.md로 저장해줘.
```

---

## 10. 사용자 상태별 리타겟팅 메시지 세트

```
brand-brief.md를 읽고 content-ops 스킬로
사용자 상태 4가지에 맞춘 리타겟팅 메시지 세트를 작성해줘.

사용자 상태:
1. 페이백이 뭔지 모르는 사용자
2. 연결했지만 혜택을 체감하지 못하는 사용자
3. 정산과 출금 구조를 신뢰하지 못하는 사용자
4. ReboundX 링크 없이 거래소에 이미 가입한 사용자

각 상태별 작성할 메시지:

A. 트위터 광고 카피 (280자 이내) × 2개 옵션
B. 텔레그램 DM 메시지 × 1개
C. 웹사이트 팝업/배너 카피 × 1개
D. 이메일 제목 + 본문 요약 × 1개

조건:
- 각 상태의 핵심 장벽을 정확히 타겟팅
- 상태 1은 교육 중심, 상태 2는 수치 시각화 중심
- 상태 3은 신뢰 구축 중심, 상태 4는 재가입 유도 중심
- 수익 보장 표현 절대 금지
- 영어로 작성

expert-panel로 전체 메시지 세트를 평가 (상태별 적합성 + 전환 예측)

outputs/retargeting-messages.md로 저장해줘.
```

---

## 사용 팁

- **스킬 경로**: content-ops = `.claude/skills/content-ops.md`, growth-engine = `.claude/skills/growth-engine.md`
- **Expert Panel 활용**: 모든 콘텐츠 작성 후 "expert panel this"라고 추가하면 자동 품질 검증
- **Growth Engine 데이터 로깅**: 콘텐츠 발행 후 실제 성과를 `experiment-engine.py log`로 기록하면 통계적으로 승자 판별
- **조합**: Agent-Research 리서치 결과를 이 프롬프트들의 인풋으로 활용하면 데이터 기반 콘텐츠 제작 가능
