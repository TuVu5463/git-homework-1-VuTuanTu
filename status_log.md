Part A Section 1
touch week2.md
git add week2.md
git commit -m 'Tạo week2.md'
git branch week2
git switch week2
Part A Section 2
touch text1.txt
touch text2.txt
git add text1.txt
git commit -m 'working 1'
git add text2.txt
git commit -m 'working 2'
Part A Section 3
echo 'Hello World' >> week2.md
git commit -a -m 'THêm 1 dòng bất kì vào week2.md trong branch week2'
Khi chuyển về master và thực hiện cat week2.md thì week2.md hoàn toàn không có dòng Hello World đã viết bên trên
Part A Section 4
git checkout -b week2b
git merge week2
git branch -d week2
Part B Section 1
git checkout -b wip
touch wip.txt
git add wip.txt
git commit -m 'Thêm wip.txt'
git switch master
git merge week2b
Part B Section 2
git branch --merged
git branch --no-merged
git branch --merged >> week2.md
git branch --no-merged >> week2.md
Part B Section 3
git branch -d week2b
Part B Section 4
git remote add origin https://github.com/TuVu5463/git-homework-2-VuTuanTu.git
git branch -m wip work-in-progress
Sau đó là công đoạn push 2 nhánh lên github
Nếu trước đó đã từng push nhánh wip lên github thì sau khi đổi tên sử dụng câu lệnh git push -u origin work-in-progress để đẩy tên mới lên git và sử dụng git push origin --delete wip để xóa nhánh đã up lên trước đó
Part C Section 1
Đoạn đầu commit lại week2.md do em bị nhầm giữa status_log.md và week2.md
git switch work-in-progress
echo 'Hello World' >> wip.txt
git commit -a -m 'Thêm text vào wip.txt trong nhánh work-in-progress'
Part C Section 2
git branch -vv
Part C Section 3
git push origin work-in-progress
Sau đó lên github và tạo pull request nhánh work-in-progress vào nhánh master
Part D Section 1
git checkout -b experiment
touch file1.txt
touch file2.txt
git add file1.txt
git commit -m "Commit đầu tiên"
git add file2.txt
git commit -m "Commit thứ hai"
Part D Section 2
git switch master
touch new_file.txt
git add new_file.txt
git commit -m "Thêm 1 file trong master"
Part D Section 3
git switch experiment
git rebase master
Part D Section 4
Quá trình rebase đã tạm thời tách các commit của nhánh experiment ra và ghép chúng lên đỉnh của master thành một đường thẳng tuyến tính, giúp nhánh master sau đó có thể gộp nhanh mà không cần tạo merge commit.
Part D Section 5
git switch master
git merge experiment
Part D Section 6
git push origin master --rebase
git push origin master
Part D Section 7
git add status_log.md
git commit -m "Thêm file status_log.md"
git push origin main
