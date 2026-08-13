# GRE 한 달 속성 마스터 코스 (2026-08-14 ~ 2026-09-14)

미국 대학원 박사과정 지원용 · 2인 듀얼 트랙 · 무료 자료 우선 · 풀타임(하루 6시간+)

## 시작하기 (내일 아침에 할 일)

1. **ETS 계정 생성** → https://www.ets.org/gre — 시험 접수(9/14~18 권장, $220)와 PowerPrep 이용에 필요
2. **PowerPrep Online Practice Test 1 응시** (진단, 약 2시간) → 결과를 `05-resources/error-log.md`에 기록
3. Claude Code에서 `/gre-daily` 실행 → 그날의 스케줄에 맞춰 코칭 시작

## 듀얼 트랙 목표

| | 트랙 A (가상세포/전산생물학) | 트랙 B (정치학·통계) |
|---|---|---|
| Quant | **168+** (필수 무기) | 163+ |
| Verbal | 155+ | **160+** |
| AWA | 3.5+ | **4.5+** |
| 시간 배분 | Quant 50% / Verbal 35% / AWA 15% | Quant 35% / Verbal 45% / AWA 20% |

상세 근거: `00-overview/target-scores.md`

## ⚠️ 먼저 확인할 것: GRE가 정말 필요한가

2020년 이후 미국 박사과정의 GRE 요구는 급감했습니다(생명과학 계열은 특히 많이 폐지, 통계·경제 등 정량 분야는 여전히 요구/권장 다수). **지원할 프로그램 목록의 admissions 페이지에서 GRE required / optional / not accepted 여부를 이번 주 안에 직접 확인**하세요. optional이어도 고득점은 국제학생에게 플러스가 되는 경우가 많습니다. (출처: `05-resources/references.md` #GRE-optional)

## 폴더 구조

```
00-overview/   최신 시험 정보 · 목표 점수
01-quant/      Quant 공부법 + 토픽 체크리스트
02-verbal/     Verbal 공부법 + 어휘 시스템
03-awa/        Issue 에세이 전략 + 템플릿
04-schedule/   주차별 일일 스케줄 (week1~4)
05-resources/  레퍼런스 목록 · 오답노트
.claude/skills 학습 도구 (아래 참고)
```

## Claude Code 학습 도구 (하네스)

| 명령 | 기능 |
|---|---|
| `/gre-daily` | 오늘 날짜 기준 스케줄 확인 + 학습 세션 운영 |
| `/vocab-quiz` | 어휘 퀴즈 (현재 진도 기반) |
| `/awa-grade` | 작성한 Issue 에세이를 ETS 기준으로 채점 + 첨삭 |
| `/error-log` | 틀린 문제 기록 + 주간 약점 분석 |

## 4주 로드맵 요약

- **Week 1 (8/14금~8/20목)**: 진단 + 시스템 구축. PP1 응시, 어휘 시작(하루 30개), Quant 개념 복구, Verbal 문제 유형 학습
- **Week 2 (8/21~8/27)**: 코어 스킬 빌드. 유형별 전략 완성, 문제 볼륨 증가, AWA 첫 에세이
- **Week 3 (8/28~9/3)**: 실전 볼륨 + 약점 타격. 섹션 단위 타이머 훈련, 오답노트 기반 집중 보강
- **Week 4 (9/4~9/10)**: 모의고사 사이클. PP2 + 무료 모의 2회, 리뷰 중심
- **버퍼 (9/11~9/13)**: 가벼운 복습 + 컨디션 조절 → **시험 9/14(월)~9/18(금) 권장**

## 운영 원칙 (토큰 절약 + 효과 극대화)

1. **무료·공식 자료 우선**: ETS PowerPrep, ETS 무료 PDF, Khan Academy, GregMat 무료 콘텐츠, Magoosh 무료 어휘 — 유료는 필요 판단 후에만 (GregMat $5/월이 최고 가성비)
2. **외부 자료를 쓸 때마다 `05-resources/references.md`에 출처 기록** (Claude가 자동 수행)
3. Claude 세션에서는 웹 리서치 반복 금지 — 이 저장소의 md가 단일 진실 소스, 갱신이 필요할 때만 검색
4. 매일 밤 오답노트 갱신 → 주말에 약점 분석 → 다음 주 계획 미세조정
