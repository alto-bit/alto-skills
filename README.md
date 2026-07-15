# alto-skills

Alto 개인 Claude Code skill 마켓플레이스.

## 설치

```
/plugin marketplace add alto-bit/alto-skills
/plugin install <skill-name>@alto-skills
```

## 기획 스킬 (alto-plan · alto-prd · alto-spec)

**같은 규격으로 기획**하고 작업 중 AI slop을 없애기 위한 자체 제작 스킬 꾸러미. 셋을 함께 설치해 쓴다 (alto-plan이 공유 인터뷰 게이트·anti-slop·라우팅의 허브).

| 스킬 | 역할 |
|------|------|
| `alto-plan` | 진입점. 모호한 기획 요청을 인터뷰로 정제(모호성 제거) → PRD/Spec 라우팅. anti-slop 원칙의 허브 |
| `alto-prd` | 공통 PRD. Background·Goal·Scope + **Epic → User Story(US-x.y) → 인수 조건(AC)** 상세 + 전체 PRD 렌더 HTML 뷰. `check_prd.py` 강제 검증 게이트 |
| `alto-spec` | 스펙 주도 개발. `.specs/`에 spec.md(설계)+PROGRESS.md(진행)+INDEX.md. 가이드 필수 6개 섹션. `check_spec.py` 강제 검증 게이트 |

- **강제 검증**: PRD·Spec 모두 작성 후 `check_*.py`가 canonical 필수 구조를 프로그램으로 검사한다. `exit 0`(PASS) 전에는 완료 불가.
- **canonical**: 각 스킬 `references/canonical/`에 방법론 원본을 보관 — 규격 판단의 최종 기준.
- 설치: `/plugin install alto-plan@alto-skills` (alto-prd·alto-spec도 동일). 벤더 심링크 불필요 — 절대경로 의존 없음.
