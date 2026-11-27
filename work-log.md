## 2026-11-27 KST — Google Search Console 연동·SEO 키워드 등록 (archivej #40)

- GSC 사이트 등록·sitemap 제출·검증 완료(tcgc.uk 계열은 도메인 검증 커버).
- 소유권 검증 메타 태그 반영 + API 검증 완료. docuteller.space 도메인 속성은 DNS TXT 대기.
- SEO 대상 키워드 config 등록: yongsankim, 용산킴, 용산킴 아카이브, YongsanKim archives
- 키워드 노출 데이터는 `plans/gsc/gsc_tool.py sync` 보고서로 정기 집계. 상세: archivej #40.

## 2026-11-16 KST — 커스텀 도메인 ys.docuteller.space 연결 (yongsankim #1)

- 소유자 지시("yongsankim 사이트 도메인을 ys.docuteller.space") → [yongsankim #1](https://github.com/text-consulting-group/yongsankim/issues/1) 신설·처리.
- Pages 프로젝트 `yongsankim`에 `ys.docuteller.space` 등록 완료(초기화 중 — DNS 대기) · config `baseURL` 전환·재빌드(ko 440/en 328)·배포 완료.
- **DNS CNAME 소유자 조치 필요**: wrangler 토큰 DNS 쓰기 불가(code 10000) — `ys` → `yongsankim.pages.dev` (Proxied) 레코드를 docuteller.space 존에 추가 필요.
- npm 의존성 미설치로 빌드 실패 → `npm install` 후 통과(postcss/tailwind).

# yongsankim 작업 기록

## 2026-10-23 KST — 할 일 정리 (추적용)

| # | 할 일 | 상태 | 비고 |
|---|-------|------|------|
| 1 | `content/items` md 백업 복원 완료 | **진행** (94/602) | 원본: Drive `backups/2026-06-07-final-source/content/items/`. rsync 재개 필요 (Drive I/O 느림) |
| 2 | `AGENTS.md`·`dummy.md`·`work-log.md` git 커밋 | 대기 | 현재 untracked. git에는 items md가 없었음 (`ffd0e8f` = 8/14) |
| 3 | `PROJECT_REQUESTS.md` 갤러리·해제 규칙 점검 | 대기 | 이미지 해제 txt → 갤러리, 1000px, 단일 컬럼. 크론 자동화 범위 |
| 4 | production-status `legacy projects` 분류 재검토 | 대기 | 2026-07-04 기준. 현 운영 상태와 대조 |
| 5 | Hugo 빌드 회귀 (`hugo --panicOnWarning`) | 대기 | items 복원 후 페이지 수·주요 URL 확인 |
| 6 | 원격 push (github.com/text-consulting-group/yongsankim) | 대기 | 저장소명 `yongsankim` (폴더명과 동일). 기존 `yonsankim` URL은 리다이렉트 |

### 참고 (2026-10-23 확인)

- git history: items md **미추적** (first commit에 `.DS_Store`만). 삭제 커밋 없음
- 복구 정본: Drive 백업 602개 (2026-06-07-final-source)
- Owner requests: Drive `PROJECT_REQUESTS.docx` / `PROJECT_REQUESTS.md` — 확정 작업은 `[V]` 위주, 신규 요청은 해당 문서에 기록
- Production URL: https://yongsankim.pages.dev/

## 2026-09-18 — 작업 로그 초기 생성

- 기존 프로젝트 폴더에 `work-log.md`와 `worklog.md`가 없어 표준 작업 로그를 생성함
- 다음 작업부터 날짜·대상·처리 내용·확인 결과·다음 상태를 기록함
