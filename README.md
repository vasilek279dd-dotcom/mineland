# Mineland — сайт сервера

Статический сайт Minecraft-сервера Mineland. IP: `26.84.4.227:25565`, версия 1.21.8.

## Файлы

| Файл | Назначение |
|------|------------|
| `index.html` | вся страница + скрипт онлайна |
| `styles.css` | стили |
| `CNAME` | домен `minelendorig.work.gd` для GitHub Pages |
| `.github/workflows/pages.yml` | автодеплой на GitHub Pages при push в `main` |

## Как залить на GitHub Pages

1. Создать репозиторий на github.com (например `mineland`), Public.
2. Загрузить в него содержимое `mineland-dist/` (кнопка `Add file` → `Upload files`, перетащить все файлы, включая папку `.github`).
3. `Settings` → `Pages` → `Source`: **GitHub Actions** → `Save`.
4. Через ~1 минуту сайт будет на `https://<user>.github.io/mineland/`.
5. Для домена `minelendorig.work.gd` у себя на DNS добавьте запись **CNAME**:
   - имя: `minelendorig.work.gd`
   - значение: `<user>.github.io`
   - TTL: 3600
6. После того как домен заработает, в `Settings` → `Pages` → `Custom domain` вписать
   `minelendorig.work.gd` и поставить галку `Enforce HTTPS`.

## Онлайн сервера

Виджет онлайна опрашивает `api.mcsrvstat.us`, при отказе — `api.mcstatus.io`.
Обновление раз в 30 секунд + при возврате на вкладку. Если сервер не отвечает —
показывается «Сервер оффлайн».

## Локальный просмотр

Открыть `index.html` двойным кликом. Всё работает без сборки и зависимостей.
