# Курсовой маршрут: Deep Research в сервисах и Gemini Notebook

Для режима «Промпты для сервисов» и для перепроверки. Шаги проверены в уроке 28.09.2026; доступные режимы зависят от аккаунта и тарифа.

Полная схема — 3 темы × 5 сервисов, до 15 отчётов. Начать можно с одной темы и сравнить несколько сервисов. Контекст и вопросы везде одинаковые: задания из `research/prompts.md`.

## Как передать ДНК и запустить исследование

| Сервис | ДНК | Запуск |
|---|---|---|
| ChatGPT | Project → Sources → добавить `dna.md` → новый чат в проекте | Deep research; выбрать самую мощную модель и максимальный уровень рассуждения, если настройка есть |
| Claude | Projects → New Project → project knowledge → «+» → `dna.md` | включить Research и веб-поиск, вставить задание |
| Gemini | Add Files → Files → `dna.md` | Add Files → Deep Research → вопрос → проверить план (Edit plan) → Start research; готовый отчёт — Export to Docs |
| Perplexity | Projects → New project → Files → `dna.md`; правила — в инструкции проекта | режим исследования (Research) |
| Parallel AI | Task Playground: задание и краткий контекст из ДНК в одном запросе | проверить параметры и стоимость перед запуском |

До старта проверьте: нужный документ прикреплён, цель и ограничения учтены.

После отчёта:
1. Сохраните отчёт как `research/reports/<тема>-<сервис>-<ГГГГ-ММ-ДД>.md`.
2. В том же чате вставьте промпт извлечения ссылок (конец `research/prompts.md`). Сервис не выдал ссылок — так и отметьте, не восстанавливайте их по памяти.

Отчёты вернулись в Claude Code — продолжай с шага 4.

## Сборка в Gemini Notebook

Gemini Notebook (бывший NotebookLM) — точка сборки урока: отвечает только по загруженным материалам и показывает цитаты.

1. notebook.google.com → новый блокнот, название по проекту → Add sources.
2. Отчёты: Upload files (PDF, TXT, Markdown) или Copied text. Название источника — «сервис — тема — дата». Проверьте, что нужный текст загрузился.
3. Исходные материалы: Add sources → Website, каждый URL с новой строки. Импортируется текст страницы; вложенные страницы не добавляются, платный доступ не поддерживается. Откройте каждую страницу в Sources: текст на месте? Недоступные отметьте.
4. Chat → настройки → Custom → вставить промпт верификатора из `references/04-synthesis.md` → Save.
5. Задать промпты GAP-анализа, синтеза гипотез и выбора гипотезы (тот же файл), затем пары маркетингового блока (`references/05-marketing.md`).
6. Цитаты проверять: навести на номер — фрагмент, нажать — контекст в источнике. Нет ответа в базе — пробел. Источники расходятся — показываем различия, не усредняем.

Полезный ответ сохраняйте в заметку блокнота и используйте в следующем синтезе. Первоисточники оставляйте для проверки.

Дополнительно: блокнот можно открыть из Gemini (личный блокнот в навигации ассистента) или из Claude Code через сторонний skill `notebooklm-research` (github.com/claude-world/notebooklm-skill; нужен вход в Google).

## Справки

- ChatGPT Deep research: https://learn.chatgpt.com/docs/web-search
- ChatGPT Projects: https://learn.chatgpt.com/docs/projects
- Claude Research: https://support.claude.com/en/articles/11088861-use-research-on-claude
- Claude Projects: https://support.claude.com/en/articles/9519177-how-can-i-create-and-manage-projects
- Gemini Deep Research: https://support.google.com/gemini/answer/15719111?hl=en
- Perplexity Research: https://www.perplexity.ai/help-center/en/articles/10738684-what-is-research-mode
- Perplexity Projects: https://www.perplexity.ai/help-center/en/articles/10352961-what-are-spaces
- Parallel Task Playground: https://platform.parallel.ai/play/task
- Gemini Notebook, источники: https://support.google.com/gemininotebook/answer/16215270?hl=en
- Gemini Notebook, цитаты и настройка чата: https://support.google.com/gemininotebook/answer/16179559
