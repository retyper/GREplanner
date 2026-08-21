---
name: gre-sync
description: 오늘 공부 기록을 GitHub(retyper/GREplanner)에 업로드 — pull, commit, push 한 번에
---

# /gre-sync

두 사람이 같은 레포를 쓴다. 개인 기록 파일이 분리되어 있어(`05-resources/log-A.md` / `log-B.md`, `03-awa/essays/{A|B}-*.md`) 정상적으로는 충돌이 나지 않는다. 아래 순서만 지키면 된다.

1. **학습자 확인**: `.learner` 파일을 읽는다 (`A` 또는 `B`). 없으면 한 번 묻고 `echo A > .learner`로 만든다. (이 파일은 gitignore됨)
2. **변경 파일 점검**: `git status --short`. 상대 학습자의 개인 파일(`log-{상대}.md`, `03-awa/essays/{상대}-*`)이 수정되어 있으면 **실수이므로 커밋하지 말고 알린다** (`git checkout -- <파일>` 제안).
3. **개인정보 점검**: diff에 여권번호·예약번호·이메일이 없는지 확인 (공개 레포).
4. **커밋**: `git add -A && git commit -m "study(A): MM/DD 요약"` — 학습자 표기 필수. 예: `study(A): 08/21 진단 기록, 스케줄 재조정, AWA 3.0`
5. **pull --rebase 후 push**:
   ```
   git pull --rebase origin main && git push origin main
   ```
   - rebase 충돌이 나면: 개인 파일이면 내 쪽(`--ours`가 아니라 **양쪽 기록을 모두 살리는** 방향)으로 병합. 공용 파일(스케줄·CLAUDE.md)이면 **상대 변경을 지우지 말고** 양쪽 내용을 합친 뒤 `git add <파일> && git rebase --continue`.
   - push가 rejected면 다시 `git pull --rebase origin main` 후 재시도 (1회까지).
6. push 인증 오류면 `! gh auth login` 실행을 안내한다.
7. 완료 후 한 줄로 보고. **장문 세션 요약은 만들지 않는다** (`05-resources/token-economy.md`).

인자 없이 실행하면 전체 수행. "pull만" 같은 인자가 오면 해당 단계만.
