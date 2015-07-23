# git_homework
*********** Задание 1

git log develop-feature1 --after "3 hours ago" --not master develop --pretty=format:"%cn: %s"

git log master develop --grep=1234 --pretty=format:"%cn: %s | %cd"

*********** Задание 2
git log develop-feature1 //смотрим id коммита, который мы должны слить в develop
git checkout develop //переходим в бранч девелоп
git cherry-pick <id> //где <id> - id коммита, который мы сливаем в develop. 
git push origin develop // Теперь в ветке develop есть этот коммит.

*********** Задание 3
git rebase -i HEAD~2 // список последних двух комитов в текстовом редакторе

Далее надо исправить 'pick' на 'reword' в текстовом редакторе, сохранить файл. Потом будут открываться файлы
с сообщениями коммитов, которые нужно изменить и сохранить.

после этого написать команду

git push origin develop-feature3 --force
