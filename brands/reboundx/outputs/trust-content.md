# 정산 신뢰도 강화 콘텐츠 — 카드뉴스 + FAQ + 대시보드 UX 카피

> 생성: 2026-07-07 (6/29 월간 정기 실행 복구분, 5/25 버전 대체)
> 대상 사용자 상태: "정산과 출금 구조를 신뢰하지 못하는 사용자" — 투명한 정산 흐름 노출이 우선.
> 원칙: 구조를 보여준다. 수익 강조 금지. 확인 안 된 정책은 [운영 확인 필요]로 표시하고 추측으로 채우지 않음.

## 1. 정산 구조 카드뉴스 (5장, 트위터/텔레그램 공용)

영어 카피 기준 (미국/동남아 공용). 카드당 텍스트 1–2줄, 시각 요소는 제작 노트 참고.

**Card 1 — 도입 (질문으로 시작)**
> "Where is my rebate right now?"
> Fair question. Here's the exact path your rebate takes — every step of it.

제작 노트: 어두운 배경, 카드 5장 경로 미리보기 (거래 → 집계 → 정산 → 지급 → 검증).

**Card 2 — 발생**
> You trade as usual. The exchange charges its normal fee.
> A share of that fee is owed back to you — at the rate listed for your exchange (e.g. OKX 55%+10%, Bybit 35%+10%).

제작 노트: 거래소 로고 + 리베이트율 표 축약형. "owed back" 강조.

**Card 3 — 정산**
> Settlement runs automatically. Payout lands within 24 hours.
> No claim button. No ticket. The clock is the promise.

제작 노트: 24h 타이머 비주얼. SLA 수치를 카드에서 가장 크게.

**Card 4 — 검증**
> Every settlement is published on-chain and off-chain.
> You don't have to trust the dashboard — you can audit it.

제작 노트: 실제 정산 기록 스크린샷(금액 마스킹) 또는 온체인 익스플로러 캡처.

**Card 5 — 행동 안내**
> One thing to check today: is your UID connected?
> No UID link = no rebate path. Takes minutes. Guide in bio.

제작 노트: CTA는 "확인"이지 "가입 유도" 아님. 체크리스트 UI 형태.

## 2. FAQ 콘텐츠 5개

사이트/텔레그램 고정 공지용. 영어 본문 + 한국어 요지.

**Q1. When do I get paid? (정산은 언제 되나요?)**
> Rebates settle automatically within 24 hours of fee collection. You don't need to request anything — settlement is triggered by the trade itself, and each payout appears in your dashboard with a timestamp.

요지: 24시간 이내 자동. 신청 절차 없음. 타임스탬프로 확인 가능.

**Q2. How do I withdraw? (출금은 어떻게 하나요?)**
> Withdrawals are made from your dashboard to your connected web3 wallet. Amounts shown as "Withdrawable" are ready to move.
> [운영 확인 필요: 최소 출금 금액, 지원 네트워크, 출금 수수료 유무 — 확정 후 문구에 수치로 삽입]

요지: 대시보드 → 연결 지갑. 세부 조건은 운영 확정값 필요.

**Q3. Does my exchange actually charge me less? (연결한 거래소에서 실제로 수수료가 차감되나요?)**
> No — and that's the point of the structure. Your exchange charges its normal fee, exactly as before. ReboundX doesn't touch your trades or your exchange account. The rebate is paid separately from the referral share the exchange pays out. Same fees on the exchange side, a separate payback on ours.

요지: 거래소 수수료는 그대로. 리베이트는 거래소가 지급하는 레퍼럴 셰어에서 별도로 돌아옴. (구조 오해 1순위 — 카드뉴스 2번과 연결)

**Q4. How is my rebate amount calculated? (리베이트 금액은 어떻게 계산되나요?)**
> Rebate = your paid fees × your exchange's published rate. The rates are listed openly: Binance 40%+10% (futures), OKX 55%+10%, Bybit 35%+10%, GRVT 25%, edgeX 30%, and more. No tiers to guess, no hidden multipliers — the rate you see is the rate applied.

요지: 낸 수수료 × 공개된 거래소별 요율. 요율표 페이지로 링크.

**Q5. What happens if I disconnect my exchange? (중간에 거래소 연결을 끊으면 어떻게 되나요?)**
> Rebates stop accruing for trades made after disconnection — the structure needs your UID link to attribute fees to you. Settled amounts already in your account remain yours.
> [운영 확인 필요: 미정산(집계 중) 금액의 처리 방침, 재연결 시 소급 여부 — 확정 전 게시 금지]

요지: 이후 거래분 중단은 구조상 확실. 기정산분 귀속·미정산분 처리·소급 여부는 운영 확정 필요.

## 3. 대시보드 정산 현황 UX 카피

상태별 레이블 + 보조 텍스트. 원칙: 사용자가 계산하지 않아도 되도록 수치 먼저, 다음 액션 1개.

| 상태 | 레이블 (EN) | 보조 텍스트 (EN) | 한국어 요지 |
|------|-------------|------------------|-------------|
| 정산 예정 | **Pending settlement** | Settles within 24h of your trade. Next settlement: {timestamp} | 다음 정산 시점을 시간으로 명시. "곧" 금지 |
| 정산 완료 | **Settled** | Paid on {date, time} · View record → | 지급 시각 + 정산 기록 링크 (검증 동선) |
| 출금 가능 | **Withdrawable** | Ready to move to your wallet · Withdraw → | 즉시 행동 가능함을 버튼으로 |

빈 상태(잔액 0) 카피:
> **No rebates yet.** Your UID is connected — rebates appear here within 24h of your next trade.
> (UID 미연결 시) **UID not connected.** Rebates can't be tracked without it. Connect now → 

작성 규칙:
- 모든 상태에 시점 정보 포함 (언제 정산되는지 / 언제 정산됐는지). 신뢰 이탈의 핵심 원인이 "시점 불명확"이므로 시간 정보가 레이블보다 중요.
- "Processing" 같은 무기한 상태어 금지 — 반드시 기한 병기.
- 금액은 USDT 단위 그대로 노출, 환산·연환산 표기 금지 (수익 프레이밍 방지).
