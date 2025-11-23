# Настройка автоматического развертывания MkDocs на GitHub Pages

## Что было настроено

1. **GitHub Actions Workflow** (`.github/workflows/lr3-docs.yml`)
   - Автоматически запускается при пуше в ветку `gubanov-egorr-lr3`
   - Собирает документацию с помощью MkDocs
   - Деплоит в подпапку `Lr3/ResidentalConnect` на GitHub Pages

2. **Обновлен `mkdocs.yml`**
   - Настроен правильный `site_url` для GitHub Pages
   - Добавлены метаданные репозитория
   - Включена поддержка GitHub Pages

3. **Обновлен `requirements.txt`**
   - Добавлены все необходимые зависимости для MkDocs и плагинов

## Как это работает

1. При каждом пуше в ветку `gubanov-egorr-lr3` (если изменены файлы документации) автоматически запускается workflow
2. GitHub Actions:
   - Устанавливает Python и зависимости
   - Собирает документацию командой `mkdocs build`
   - Деплоит собранный сайт в ветку `gh-pages` в подпапку `Lr3/ResidentalConnect`

## Настройка GitHub Pages (один раз)

После первого пуша нужно настроить GitHub Pages в настройках репозитория:

1. Перейдите в **Settings** → **Pages** вашего репозитория
2. В разделе **Source** выберите:
   - **Source**: `Deploy from a branch`
   - **Branch**: `gh-pages`
   - **Folder**: `/ (root)`
3. Нажмите **Save**

## URL документации

После настройки документация будет доступна по адресу:

```
https://egorr-gubanov.github.io/TonikX-ITMO_ICT_WebDevelopment_2025-2026/Lr3/ResidentalConnect/
```

## Ручной запуск

Если нужно запустить деплой вручную:

1. Перейдите в **Actions** в вашем репозитории
2. Выберите workflow **Deploy Lr3 MkDocs Documentation**
3. Нажмите **Run workflow**
4. Выберите ветку `gubanov-egorr-lr3`
5. Нажмите **Run workflow**

## Проверка статуса

- Проверьте статус деплоя в разделе **Actions** репозитория
- После успешного деплоя документация появится по указанному URL через 1-2 минуты

