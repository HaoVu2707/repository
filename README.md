# repository
Not pushed + old commit:
git rebase -i HEAD~X
# X is the number of commits to go back
# Move to the line of your commit, change pick into edit,
# then change your commit message:
git commit --amend
# Finish the rebase with:
git rebase --continue
Rebase opened your history and let you pick what to change. With edit you tell you want to change the message. Git moves you to a new branch to let you --amend the message. git rebase --continue puts you back in your previous branch with the message changed.

Already pushed + old commit:
Edit your message with the same 3 steps process as above (rebase -i, commit --amend, rebase --continue). Then force push the commit:

git push origin master --force
⚠️ But! Remember re-pushing your commit after changing it will very likely prevent others to sync with the repo, if they already pulled a copy. You should first check with them.
vũ thị hảo
phạm hoàng anh thư
anh thư phạm