# Проектные навыки Claude Code

Откройте корень клона в Claude Code. Навыки обнаруживаются в `.claude/skills/` и доступны через слеш-команды, например `/android-roleplay-design`. [Правила проекта](../CLAUDE.md) связывают навыки с обычными задачами.

| Имя | Назначение | Путь | Источник | Версия или SHA | Когда применять |
| --- | --- | --- | --- | --- | --- |
| `android-cli` | Android CLI, SDK, устройства и документация | [SKILL.md](../.claude/skills/android-cli/SKILL.md) | [android/skills](https://github.com/android/skills/tree/7f7b21730a605d112ca9f79b6e40105ce7b670ee/devtools/android-cli) | `7f7b21730a605d112ca9f79b6e40105ce7b670ee` | Для работы с Android SDK, AVD, APK или поиска в официальной документации |
| `adaptive` | Адаптивная компоновка Compose | [SKILL.md](../.claude/skills/adaptive/SKILL.md) | [android/skills](https://github.com/android/skills/tree/7f7b21730a605d112ca9f79b6e40105ce7b670ee/jetpack-compose/adaptive) | `7f7b21730a605d112ca9f79b6e40105ce7b670ee` | Для изменения ширины окна, многооконной компоновки или сохранения состояния при повороте, с учётом предусловий навыка |
| `edge-to-edge` | Системные панели и отступы IME | [SKILL.md](../.claude/skills/edge-to-edge/SKILL.md) | [android/skills](https://github.com/android/skills/tree/7f7b21730a605d112ca9f79b6e40105ce7b670ee/system/edge-to-edge) | `7f7b21730a605d112ca9f79b6e40105ce7b670ee` | Когда клавиатура или системные панели перекрывают компоненты |
| `testing-setup` | Инфраструктура Android-тестов и скриншотов | [SKILL.md](../.claude/skills/testing-setup/SKILL.md) | [android/skills](https://github.com/android/skills/tree/7f7b21730a605d112ca9f79b6e40105ce7b670ee/testing/testing-setup) | `7f7b21730a605d112ca9f79b6e40105ce7b670ee` | При настройке unit-, UI-, screenshot- и end-to-end-тестов |
| `android-emulator-qa` | Запуск APK, UI-дерево, скриншоты и логи через adb | [SKILL.md](../.claude/skills/android-emulator-qa/SKILL.md) | [openai/plugins](https://github.com/openai/plugins/tree/981b02c0c44058b595f3b4180002c3ae3c806d40/plugins/test-android-apps/skills/android-emulator-qa) | `981b02c0c44058b595f3b4180002c3ae3c806d40` | Для приёмки сценариев и воспроизведения UI-дефектов на эмуляторе |
| `android-roleplay-design` | Дизайн-система и визуальная приёмка Compose | [SKILL.md](../.claude/skills/android-roleplay-design/SKILL.md) | [GramMarket](../.claude/skills/android-roleplay-design/SKILL.md) | `1.0.0` | При изменении экранов, темы или компонентов |
| `roleplay-engine` | События сцены, синхронизация и генерация Ollama | [SKILL.md](../.claude/skills/roleplay-engine/SKILL.md) | [GramMarket](../.claude/skills/roleplay-engine/SKILL.md) | `1.0.0` | При изменении формата чата, карточек, контекста, повтора или перегенерации |
| `android-apk-and-vps` | Сборка и подпись APK, HTTPS, VPS и бэкап SQLite | [SKILL.md](../.claude/skills/android-apk-and-vps/SKILL.md) | [GramMarket](../.claude/skills/android-apk-and-vps/SKILL.md) | `1.0.0` | При работе с Gradle, GitHub Actions, выпуском и эксплуатацией |

## Лицензии и инструменты

- Четыре навыка Android распространяются по Apache 2.0. В каждом каталоге лежит исходный `LICENSE.txt` и полный набор файлов навыка. Бинарник `android` устанавливается отдельно по [официальной инструкции](https://developer.android.com/tools/agents/android-cli).
- В каталоге `android-emulator-qa` сохранён полный набор файлов, включая лицензию Apache 2.0, Python-скрипты и метаданные OpenAI. Для самого сценария достаточно Android SDK Platform-Tools (`adb`), Android-эмулятора или устройства, APK и Python 3.10+ для вспомогательных скриптов. Устанавливать плагин OpenAI для Claude Code не требуется.
- Визуальный прогон ожидает исходники приложения, APK и эмуляторы. Порядок проверки и список снимков описаны в [сценарии приёмки](../.claude/skills/android-roleplay-design/references/ui-review.md).

## Справочные материалы по дизайну

- [Anthropic Frontend Design](https://github.com/anthropics/claude-plugins-official/tree/main/plugins/frontend-design) используется как источник идей. Для отдельной установки в Claude Code добавьте официальный marketplace командой `/plugin marketplace add anthropics/claude-plugins-official` и выполните `/plugin install frontend-design@claude-plugins-official`.
- [Android Mobile UI](https://developer.android.com/design/ui/mobile)
- [Jetpack Compose Accessibility](https://developer.android.com/codelabs/jetpack-compose-accessibility)
