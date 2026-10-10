---
name: video
description: "Make a video, motion graphics or animated clip: promo or launch video, explainer, product demo, captions, animated title, social clip. Use whenever the user asks to create, edit or render a video or motion graphics. Loads the HyperFrames or Remotion skills on demand."
---

# video

Скиллы HyperFrames и Remotion большие, поэтому постоянно не подключены.
Этот скилл подгружает их только под задачу с видео.

## 1. Выбери инструмент

- **HyperFrames** (по умолчанию): видео из HTML, CSS и GSAP. Промо-ролики,
  моушен-графика, титры, субтитры, видео из сайта или PR. Не требует React.
- **Remotion**: в проекте уже есть Remotion (`remotion` в `package.json`),
  либо пользователь просит именно Remotion или видео на React.

## 2. Проверь, не подключены ли скиллы уже

Если в списке доступных скиллов уже есть `hyperframes` или
`remotion-best-practices`, просто используй их и пропусти шаг 3.

## 3. Скачай скиллы

```bash
# HyperFrames
d="${TMPDIR:-/tmp}/agent-skills/hyperframes"
[ -d "$d" ] || git clone -q --depth 1 --filter=blob:none --sparse https://github.com/heygen-com/hyperframes.git "$d"
git -C "$d" sparse-checkout set skills && git -C "$d" pull -q --ff-only
ls "$d/skills"

# Remotion
d="${TMPDIR:-/tmp}/agent-skills/remotion"
[ -d "$d" ] || git clone -q --depth 1 https://github.com/remotion-dev/skills.git "$d"
git -C "$d" pull -q --ff-only
ls "$d/skills"
```

## 4. Работай по скачанным скиллам

1. Прочитай входной скилл целиком:
   - HyperFrames: `skills/hyperframes/SKILL.md`;
   - Remotion: `skills/remotion-best-practices/SKILL.md`.
2. Входной скилл скажет, какие ещё скиллы нужны под задачу (анимация, звук,
   субтитры, рендер, промо-ролик). Открывай их `SKILL.md` по мере надобности,
   а не все сразу.
3. Пути в скиллах (`references/...`, `scripts/...`) считай от папки этого
   скилла.
4. Следуй инструкциям скачанных скиллов так же, как если бы они были
   установлены.

## Постоянно включить для проекта

Если проект целиком про видео, добавь в `.claude/settings.json` проекта:

```json
"enabledPlugins": {
  "hyperframes@lukinslava-skills": true,
  "remotion@lukinslava-skills": true
}
```
