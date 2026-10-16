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
| Стейкхолдеры                                               | [motivation/stakeholders.md](motivation/stakeholders.md) |
| Бизнес-драйверы                                            | [motivation/drivers.md](motivation/drivers.md)           |
| Бизнес-цели                                                | [motivation/goals.md](motivation/goals.md)               |
| [Capability](../../glossary/terms/capability.md) | [capability/README.md](capability/README.md) (каталог по контекстам) |

## Вне области продукта

- рефакторинг кода и управление зависимостями между репозиториями (кроме операций
git и SCM API);
- хостинг SCM и замена GitLab, GitHub и других платформ;
- долговременное хранение секретов (учётные данные — через переменные окружения
или средства ОС).
