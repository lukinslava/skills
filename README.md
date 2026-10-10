# skills

Мой набор скиллов, собранный в один [маркетплейс плагинов Claude Code](https://code.claude.com/docs/en/plugin-marketplaces).
Скиллы сюда не копируются: каждый плагин ссылается на репозиторий автора,
поэтому обновления приходят из исходников.

| Плагин | Скиллы | Источник |
| --- | --- | --- |
| `lukinslava` | design-references (мои сайты с референсами), video (подгружает HyperFrames или Remotion по запросу на видео) | этот репозиторий, [`plugins/lukinslava`](plugins/lukinslava) |
| `brag` | brag, brag-slim | [latent-spaces/brag](https://github.com/latent-spaces/brag) |
| `nodumbmode` | nodumb, ask-nodumb, edge-hunt, system-feedback, changelog-discipline, nodumb-loop | [hanumatori/nodumbmode](https://github.com/hanumatori/nodumbmode) |
| `deslop` | sasha, serega-gentle, serega-emotional | [mishanaer/deslop](https://github.com/mishanaer/deslop) |
| `vercel-react` | vercel-react-best-practices, vercel-composition-patterns, vercel-react-view-transitions, web-design-guidelines | [vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills) (набор из [IlyaGrshin/wallet_animations](https://github.com/IlyaGrshin/wallet_animations)) |
| `taste-skill` | design-taste-frontend, high-end-visual-design, redesign-existing-projects, minimalist-ui, industrial-brutalist-ui, image-to-code и др. (13 шт.) | [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) ([tasteskill.dev](https://www.tasteskill.dev/)) |
| `hyperframes` | hyperframes, hyperframes-animation, motion-graphics, product-launch-video и др. (21 шт.) | [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes), не включён по умолчанию* |
| `remotion` | remotion-best-practices, remotion-create, remotion-render и др. (12 шт.) | [remotion-dev/skills](https://github.com/remotion-dev/skills), не включён по умолчанию* |

\* `hyperframes` и `remotion` большие: одни только описания HyperFrames занимают около 4 тыс. токенов в каждой сессии. Поэтому постоянно они не включены. Когда вы просите видео, скилл `video` скачивает нужные скиллы с GitHub и работает по ним. Для проекта, который целиком про видео, их можно включить в `.claude/settings.json` проекта.

## Подключить к проекту

Скопируйте [`examples/project-settings.json`](examples/project-settings.json)
в проект как `.claude/settings.json` (или добавьте эти два ключа в существующий файл)
и закоммитьте. При открытии проекта Claude Code предложит добавить маркетплейс
и включить плагины. Лишние плагины можно убрать из `enabledPlugins`.

## Подключить сразу ко всем проектам

```bash
claude plugin marketplace add lukinslava/skills
claude plugin install lukinslava@lukinslava-skills
claude plugin install brag@lukinslava-skills
claude plugin install nodumbmode@lukinslava-skills
claude plugin install deslop@lukinslava-skills
claude plugin install vercel-react@lukinslava-skills
claude plugin install taste-skill@lukinslava-skills
```

Плагины ставятся в пользовательскую область (`~/.claude`) и работают в любом проекте.

## Обновить

```bash
claude plugin marketplace update lukinslava-skills
```

## Добавить сайт с референсами

Допишите строку в таблицу в
[`plugins/lukinslava/skills/design-references/SKILL.md`](plugins/lukinslava/skills/design-references/SKILL.md).

## Добавить новый репозиторий со скиллами

Добавьте запись в [`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json):

```json
{
  "name": "имя-плагина",
  "source": { "source": "github", "repo": "owner/repo" },
  "skills": ["./путь/к/папке/со/скиллами"]
}
```

- Если в репозитории уже есть `.claude-plugin/plugin.json` или папка `skills/`, ключ `skills` не нужен.
- `skills` принимает папку с одним `SKILL.md` или папку с подпапками `<имя>/SKILL.md`; `"./"` означает корень репозитория.
- Скиллы лежат в подпапке большого репозитория: используйте `{ "source": "git-subdir", "url": "owner/repo", "path": "sub/dir" }`.
- Чтобы зафиксировать версию, добавьте в `source` поле `"ref"` (ветка или тег) или `"sha"`.

Перед коммитом проверьте:

```bash
claude plugin validate .
```
