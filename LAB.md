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

[FIXME: одним абзацем — что положили в Initial commit, почему `Initial commit` оставлен без префикса Conventional Commits.]

## Шаг 2. chore: .gitignore

[FIXME: одним абзацем — какой стек, откуда взяли `.gitignore` (toptal-генератор / написали сами / иное), что включили.]

## Шаг 3. feat(tasks): complete_task

[FIXME: одним абзацем — что добавили в `tasks.py`, почему тип `feat` и почему scope `tasks`.]

## Шаг 4. fix(tasks): валидация через add -p

[FIXME: одним абзацем — что было: два не связанных изменения в одном файле. Что разделили через `git add -p`. Какие hunk-и видел Git, на какой ответили `y`, на какой `n`.]

Скриншот интерактивной сессии `git add -p`:

![git add -p](screenshots/03-add-p.png)

## Шаг 5. feat(tasks): delete_task

[FIXME: одним абзацем — оставшийся hunk закоммитили обычным `git add`. Перед коммитом проверили `git diff --staged`.]

Скриншот `git diff --staged` перед коммитом:

![git diff --staged](screenshots/02-diff-staged.png)

## Шаг 6. docs: расширенный README и LAB

[FIXME: одним абзацем — что добавили в `README.md` (оглавление, секция TODO, code block, `<details>`, ссылка), какие разделы создали в `LAB.md`. Этот коммит сделали без `-m`, через редактор, с телом ≥ 2 строк.]

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

[FIXME: 1-2 абзаца. Почему выбрали `v0.1.0`, а не `v1.0.0`. На что ориентировались:
- стабильность API (мы только начали — менять что угодно);
- по SemVer мажорная `0.x` — особое соглашение «всё может ломаться»;
- что нужно, чтобы перейти на `v1.0.0`.

Также объясните, почему annotated, а не lightweight: GitHub показывает в Releases только annotated, в annotated есть автор/дата/сообщение релиза.]

## Финальная история

```bash
git log --oneline --graph --decorate
```

Видно 7 коммитов: 6 содержательных + 1 финальная актуализация `LAB.md`. Тег `v0.1.0` стоит на 6-м коммите, `HEAD -> main` — на 7-м (актуализации). Это иллюстрирует, что тег закреплён за коммитом и не двигается за веткой.

![git log финал](screenshots/01-git-log.png)
