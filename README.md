# site-factory — Среда для производства сайтов в Claude Code

Одна папка = вся система: память (CLAUDE.md), директивы (.claude/commands/),
скиллы (skills/), MCP (figma.config.json), артефакты каждого этапа (artifacts/).

## Быстрый старт
1. Открой папку в Claude Code (VS Code).
2. Подключи Figma MCP, впиши fileKeys в figma.config.json.
3. Положи свои скиллы в skills/ (или подключи глобально): style-decompose,
   vite-react-prototype, nano-banana.
4. Запусти конвейер: `/site <короткое описание проекта>`
   — он пройдёт brief → research → spec → design → assets → build → review → handoff,
   останавливаясь на согласование после каждого этапа.

## Зачем так
- Скорость: повторяемый конвейер вместо промпта с нуля каждый раз.
- Грамотность: каждый экран подкреплён гипотезой из ресёрча, дизайн — токенами, не на глаз.
- Согласования: на каждом этапе есть артефакт-обоснование.

## Поток данных
00_brief → 01_research → 02_SPEC → 03_design-system(tokens) → 04_assets → src/ → 06_review → HANDOFF
