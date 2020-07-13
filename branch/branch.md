 [на главную](/readme.md)

## branch — команда, которая создает новую ветку в репозитории.

Просто перечисляем существующие ветки, отметив активную:

        git branch

Создаём новую ветку new-branch:

        git branch new-branch

Удаляем ветку, если та была залита (merged) с разрешением возможных конфликтов в текущую:

        git branch -d new-branch

Удаляем ветку в любом случае:

        git branch -D new-branch

Переименовываем ветку:

        git branch -m new-name-branch

Показывываем те ветки, среди предков которых есть определенный коммит:

        git branch --contains v1.2

Показываем коммит ответвления ветки new-name-branch от ветки master:

        git merge-base master new-name-branch