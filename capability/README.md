# Каталог capability Git Herder

Документы в этом каталоге описывают [Capability](../../../glossary/terms/capability.md)
продукта — устойчивые способности CLI, а не отдельные команды или user stories.
Трассировка к [бизнес-целям](../motivation/goals.md) — в каждом файле и в реестре
целей.

Файлы разложены по **ограниченным контекстам** (подкаталоги). Сквозные capability
в [`platform/`](platform/) обслуживают любую массовую операцию; прикладные — в
[`scm/`](scm/) (операции на [SCM-платформе](../../../glossary/terms/scm-platform.md))
и [`local/`](local/) (операции над локальными рабочими копиями на диске). Две
подмодели отбора — в
[единый отбор](platform/repository-selection.md).

## Сквозная платформа массового выполнения — `platform/`

Как Git Herder задаёт контекст, отбор, безопасность, сеть, вывод в терминал и
журнал для **всех** массовых команд.

| Capability | Файл |
| ---------- | ---- |
| Профили Git Herder | [profiles.md](platform/profiles.md) |
| Единый отбор для массовых операций | [repository-selection.md](platform/repository-selection.md) |
| Защита от случайных нежелательных изменений | [operation-preview.md](platform/operation-preview.md) |
| Отказоустойчивое выполнение массовых сетевых операций | [resilient-network-execution.md](platform/resilient-network-execution.md) |
| Обратная связь в терминале | [terminal-feedback.md](platform/terminal-feedback.md) |
| Трассировка выполнения | [operation-trace.md](platform/operation-trace.md) |

## Операции на SCM-платформе — `scm/`

Чтение или изменение состояния репозиториев **на платформе** (API SCM). Вход —
**SCM-отбор** из [repository-selection.md](platform/repository-selection.md).

| Capability | Файл | Бизнес-цель |
| ---------- | ---- | ----------- |
| Массовое клонирование из SCM | [mass-clone.md](scm/mass-clone.md) | [BG-1](../motivation/goals.md#bg-1) |
| Отчёт о репозиториях в SCM | [scm-repository-reports.md](scm/scm-repository-reports.md) | [BG-2](../motivation/goals.md#bg-2) |
| Редактирование метаданных репозиториев на SCM | [scm-repository-metadata.md](scm/scm-repository-metadata.md) | [BG-4](../motivation/goals.md#bg-4) |

**Планируются** (цели есть, capability ещё не описаны): управление вебхуками
([BG-3](../motivation/goals.md#bg-3)); API-часть массовой публикации при создании
репозиториев на SCM ([BG-5](../motivation/goals.md#bg-5) — граница с локальным
push уточняется при описании capability).

## Операции над локальными рабочими копиями — `local/`

Действия **git** в workspace на диске. Вход — **локальный отбор** из
[repository-selection.md](platform/repository-selection.md). См. [local/README.md](local/README.md).

| Capability | Статус | Бизнес-цель |
| ---------- | ------ | ----------- |
| Массовое выполнение локальных git-операций | proposed | [BG-5](../motivation/goals.md#bg-5), [BG-6](../motivation/goals.md#bg-6), [BG-7](../motivation/goals.md#bg-7), [BG-8](../motivation/goals.md#bg-8) |

См. [mass-local-git-operations.md](local/mass-local-git-operations.md) (pull, fetch, push, merge, switch, изменяющий remote).

Сквозная платформа (`platform/`) применяется к операциям в `scm/` и `local/` одинаково.
