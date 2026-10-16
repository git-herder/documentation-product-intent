# Git Herder — замысел продукта

**Git Herder** — открытая CLI-утилита для массовых операций над git-репозиториями на
[SCM-платформах](../../glossary/terms/scm-platform.md) и над локальными рабочими копиями этих
репозиториев. Продукт снимает рутину при работе с большими наборами репозиториев
в микросервисных и модульных системах.

Команда: `git-herder`, синонимы: `githerder`, `gherd`.

Слой мотивации — [бизнес-цели](../../glossary/terms/business-goal.md), [бизнес-драйверы](../../glossary/terms/business-driver.md)
и [стейкхолдеры](../../glossary/terms/stakeholder.md):
<!-- markdownlint-disable MD060 -->
| Раздел                                                     | Файл                                                       |
| ---------------------------------------------------------- | ---------------------------------------------------------- |
| Стейкхолдеры                                               | `[motivation/stakeholders.md](motivation/stakeholders.md)` |
| Бизнес-драйверы                                            | `[motivation/drivers.md](motivation/drivers.md)`           |
| Бизнес-цели                                                | `[motivation/goals.md](motivation/goals.md)`               |
| [Capability](../../glossary/terms/capability.md) (каталог) | `[capability/](capability/)`                               |
| Профили Git Herder                                         | `[capability/profiles.md](capability/profiles.md)`         |
| Трассировка выполнения                                     | `[capability/operation-trace.md](capability/operation-trace.md)` |
| Обратная связь в терминале                                 | `[capability/terminal-feedback.md](capability/terminal-feedback.md)` |
| Единый отбор для массовых операций                         | `[capability/repository-selection.md](capability/repository-selection.md)` |
| Защита от случайных нежелательных изменений                 | `[capability/operation-preview.md](capability/operation-preview.md)` |
| Массовое клонирование из SCM                               | `[capability/mass-clone.md](capability/mass-clone.md)` |
| Отказоустойчивое выполнение массовых сетевых операций      | `[capability/resilient-network-execution.md](capability/resilient-network-execution.md)` |
| Отчёт о репозиториях в SCM                                 | `[capability/scm-repository-reports.md](capability/scm-repository-reports.md)` |
| Редактирование метаданных репозиториев на SCM              | `[capability/scm-repository-metadata.md](capability/scm-repository-metadata.md)` |

## Вне области продукта

- рефакторинг кода и управление зависимостями между репозиториями (кроме операций
git и SCM API);
- хостинг SCM и замена GitLab, GitHub и других платформ;
- долговременное хранение секретов (учётные данные — через переменные окружения
или средства ОС).
