# Git Herder — замысел продукта

**Git Herder** — открытая CLI-утилита для массовых операций над git-репозиториями на
[SCM-платформах][SCM-PLATFORM-TERM] и над локальными рабочими копиями этих
репозиториев. Продукт снимает рутину при работе с большими наборами репозиториев
в микросервисных и модульных системах.

Слой мотивации — [бизнес-цели][BUSINESS-GOAL-TERM], [бизнес-драйверы][BUSINESS-DRIVER-TERM]
и [стейкхолдеры][STAKEHOLDER-TERM]:

| Раздел | Файл |
| ------ | ---- |
| Стейкхолдеры | [`motivation/stakeholders.md`](motivation/stakeholders.md) |
| Бизнес-драйверы | [`motivation/drivers.md`](motivation/drivers.md) |
| Бизнес-цели | [`motivation/goals.md`](motivation/goals.md) |
| [Capability][CAPABILITY-TERM] (каталог) | [`capability/`](capability/) |
| Профили Git Herder | [`capability/profiles.md`](capability/profiles.md) |

## Вне области продукта

- рефакторинг кода и управление зависимостями между репозиториями (кроме операций
  git и SCM API);
- хостинг SCM и замена GitLab, GitHub и других платформ;
- долговременное хранение секретов (учётные данные — через переменные окружения
  или средства ОС).

<!-- LINKS -->

[SCM-PLATFORM-TERM]: ../../glossary/terms/scm-platform.md
[BUSINESS-GOAL-TERM]: ../../glossary/terms/business-goal.md
[BUSINESS-DRIVER-TERM]: ../../glossary/terms/business-driver.md
[STAKEHOLDER-TERM]: ../../glossary/terms/stakeholder.md
[CAPABILITY-TERM]: ../../glossary/terms/capability.md
