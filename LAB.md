# LAB — день 3

Отчёт о выполнении домашнего задания дня 3 в рамках курса ["Интенсив по погружению в GIT"](https://slurm.io/git-intensive): построение реальной истории на ветке `main` с использованием Conventional Commits, разделение изменений через `git add -p` и публикация релиза через annotated тег `v0.1.0`.

## Содержание

- [LAB — день 3](#lab--день-3)
  - [Содержание](#содержание)
  - [Шаг 1. Initial commit](#шаг-1-initial-commit)
  - [Шаг 2. chore: .gitignore](#шаг-2-chore-gitignore)
  - [Шаг 3. feat(tasks): complete\_task](#шаг-3-feattasks-complete_task)
  - [Шаг 4. fix(tasks): валидация через add -p](#шаг-4-fixtasks-валидация-через-add--p)
  - [Шаг 5. feat(tasks): delete\_task](#шаг-5-feattasks-delete_task)
  - [Шаг 6. docs: расширенный README и LAB](#шаг-6-docs-расширенный-readme-и-lab)
  - [Релиз: тег v0.1.0](#релиз-тег-v010)
  - [Почему именно v0.1.0](#почему-именно-v010)
  - [Финальная история](#финальная-история)

## Шаг 1. Initial commit

положили комит

## Шаг 2. chore: .gitignore

питон, взяли с сайта

## Шаг 3. feat(tasks): complete_task

потому что

## Шаг 4. fix(tasks): валидация через add -p

положили, видели

Скриншот интерактивной сессии `git add -p`:

![git add -p](screenshots/03-add-p.png)

## Шаг 5. feat(tasks): delete_task


Скриншот `git diff --staged` перед коммитом:

![git diff --staged](screenshots/02-diff-staged.png)

## Шаг 6. docs: расширенный README и LAB

добавили то то и то то

## Релиз: тег v0.1.0

После шага 6 запушили `main`, поставили annotated тег и запушили его:

```bash
git push origin main
git tag -a v0.1.0      # многострочное сообщение через редактор
git push origin v0.1.0
```

Скриншот вывода `git show v0.1.0` (видно `tag` объект, автора, сообщение):

![git show v0.1.0](screenshots/04-show-tag.png)

Скриншот публикации тега (`git push origin v0.1.0` или страница Releases/Tags на GitHub):

![Тег запушен](screenshots/05-tag-pushed.png)

## Почему именно v0.1.0

- стабильность API (мы только начали — менять что угодно);
- по SemVer мажорная `0.x` — особое соглашение «всё может ломаться»;
- что нужно, чтобы перейти на `v1.0.0`.


## Финальная история

```bash
git log --oneline --graph --decorate
```

Видно 7 коммитов: 6 содержательных + 1 финальная актуализация `LAB.md`. Тег `v0.1.0` стоит на 6-м коммите, `HEAD -> main` — на 7-м (актуализации). Это иллюстрирует, что тег закреплён за коммитом и не двигается за веткой.

![git log финал](screenshots/01-git-log.png)
