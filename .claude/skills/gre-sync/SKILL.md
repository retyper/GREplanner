---
name: gre-sync
description: 오늘 공부 기록을 GitHub(retyper/GREplanner)에 업로드 — pull, commit, push 한 번에
---

# /gre-sync

두 사람이 같은 레포를 쓰므로 **항상 pull부터** 한다.

1. `git pull --rebase origin main` — 상대방이 올린 기록을 먼저 받는다. 충돌이 나면 (주로 error-log.md, vocab-system.md의 표) 양쪽 기록을 모두 살리는 방향으로 병합해준다.
2. `git status`로 변경 파일을 확인하고 한 줄로 요약해 보여준다.
3. 전부 스테이징 후 커밋. 메시지 형식: `study: MM/DD 요약` (예: `study: 08/15 A quant arithmetic 15문항, 오답 3건 기록`). 학습자 이름(A/B)과 주요 활동을 담는다.
4. `git push origin main`으로 업로드하고 완료를 알린다.
5. push가 인증 오류로 실패하면 `! gh auth login` 실행을 안내한다.

인자 없이 실행하면 위 과정 전체를 수행. "pull만" 같은 인자가 오면 해당 단계만.
