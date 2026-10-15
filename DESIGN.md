---
name: Зал
description: Ночной зал — тёмный премиум-мир семьи Apple Fitness со своей идентичностью
colors:
  night: "#0A0C0E"
  surface: "#16191D"
  surface-raised: "#1E2328"
  hairline: "rgba(255,255,255,0.08)"
  text: "#F2F4F6"
  muted: "#9AA4AD"
  ember: "#FF6A3D"
  ember-pressed: "#E8552B"
  on-ember: "#1C0E06"
  zone-green: "#34C77B"
  over-amber: "#F5C04E"
  steel: "#66809A"
  danger: "#FF5D57"
  glass: "rgba(12,14,16,0.72)"
typography:
  display:
    fontFamily: "ui-rounded, 'SF Pro Rounded', -apple-system, system-ui, sans-serif"
    fontSize: "40px"
    fontWeight: 800
    lineHeight: 1.05
    letterSpacing: "-0.02em"
  largetitle:
    fontFamily: "-apple-system, BlinkMacSystemFont, 'SF Pro Display', system-ui, sans-serif"
    fontSize: "28px"
    fontWeight: 800
    lineHeight: 1.15
    letterSpacing: "-0.02em"
  body:
    fontFamily: "-apple-system, BlinkMacSystemFont, 'SF Pro Text', system-ui, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.45
  label:
    fontFamily: "-apple-system, BlinkMacSystemFont, 'SF Pro Text', system-ui, sans-serif"
    fontSize: "13px"
    fontWeight: 600
    lineHeight: 1.3
  caption:
    fontFamily: "-apple-system, BlinkMacSystemFont, 'SF Pro Text', system-ui, sans-serif"
    fontSize: "11px"
    fontWeight: 700
    letterSpacing: "0.06em"
rounded:
  card: "16px"
  control: "13px"
  input: "12px"
  chip: "999px"
  segment: "5px"
spacing:
  xs: "4px"
  sm: "8px"
  md: "12px"
  lg: "16px"
  xl: "24px"
components:
  button-primary:
    backgroundColor: "{colors.ember}"
    textColor: "{colors.on-ember}"
    rounded: "{rounded.control}"
    padding: "13px 18px"
  button-primary-active:
    backgroundColor: "{colors.ember-pressed}"
    textColor: "{colors.on-ember}"
  button-secondary:
    backgroundColor: "{colors.surface-raised}"
    textColor: "{colors.text}"
    rounded: "{rounded.control}"
    padding: "13px 18px"
  chip:
    backgroundColor: "{colors.surface-raised}"
    textColor: "{colors.text}"
    rounded: "{rounded.chip}"
    padding: "10px 15px"
  chip-selected:
    backgroundColor: "{colors.ember}"
    textColor: "{colors.on-ember}"
    rounded: "{rounded.chip}"
  card:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.text}"
    rounded: "{rounded.card}"
    padding: "16px"
---

# Design System: Зал

## Overview

**Creative North Star: "Ночной зал"**

Тёмный железный мир: зал ночью, выключенный свет, горячий металл. Семья Apple Fitness/Activity — всегда тёмная сцена, крупные округлые цифры, энергия движения — но идентичность своя: фирменный акцент — эмбер (раскалённая сталь), а не зелёный Fitness и не кольца Activity. Сигнатурный элемент системы — «коридор объёма»: сегментные шкалы недельного объёма — то, чем для Apple являются кольца.

Это Operate-поверхность: пользователь в задаче (записать подход между отдыхами, одной рукой, беглым взглядом). Выразительность живёт в точных деталях — материале, цифрах, одном авторском моменте движения — и никогда не мешает задаче.

**Key Characteristics:**
- Всегда тёмный (OLED-чёрный фон, тональные слои поверх).
- Округлые дисплейные цифры (ui-rounded, 800), все цифры табличные.
- Эмбер только на действии и выборе; семантика данных — зелёный/янтарь/сталь.
- Глубина — тональные слои + волосяные линии; стекло только на функциональных плавающих панелях.
- Одно авторское движение: записанный подход.

## Colors

Ночная сцена с одним горячим акцентом и честной семантикой данных.

### Primary
- **Эмбер** (#FF6A3D): единственный «горячий» цвет — главное действие (записать подход), активный выбор (таб, чип, сегмент-контрол), «сегодня». Нажатое состояние — **Эмбер тёмный** (#E8552B). Текст на эмбере — **Уголь** (#1C0E06), не белый.

### Neutral
- **Ночь** (#0A0C0E): фон всего приложения. Не #000 — чуть тёплый графит.
- **Поверхность** (#16191D): карточки.
- **Поверхность поднятая** (#1E2328): вложенные элементы, чипы, сегмент-контролы.
- **Волос** (rgba(255,255,255,0.08)): единственный цвет границ.
- **Текст** (#F2F4F6) и **Приглушённый** (#9AA4AD): два уровня текста, третьего нет.
- **Стекло** (rgba(12,14,16,0.72) + blur): материал шапки и таб-бара.

### Tertiary (семантика данных — коридор объёма)
- **Зелень зоны** (#34C77B): объём в коридоре, тренированный день.
- **Янтарь перебора** (#F5C04E): выше коридора, предупреждения.
- **Сталь** (#66809A): объём копится, ещё не в зоне; недоборные сегменты.
- **Красный** (#FF5D57): только разрушающие действия и алкоголь-метка.

### Named Rules
**Правило эмбера.** Эмбер занимает ≤10% экрана: действие, выбор, «сегодня». Семантика данных (зона/перебор/накопление) никогда не красится эмбером — жар означает «нажми», а не «хорошо».
**Правило двух температур.** Янтарь перебора — жёлтый, эмбер — красно-оранжевый; если их можно спутать, значение уехало от токена.

## Typography

**Display Font:** ui-rounded / SF Pro Rounded (fallback -apple-system)
**Body Font:** -apple-system / SF Pro Text
**Label/Mono Font:** цифры — те же семейства с `font-variant-numeric: tabular-nums`; моно только для JSON-экспорта.

**Character:** округлые жирные цифры несут энергию (ДНК Apple-фитнеса), текст — нейтральный системный SF. Никаких внешних шрифтов: приложение офлайн.

### Hierarchy
- **Display** (800, 40px/1.05, -0.02em, rounded): большие числа — вес, среднее за 7 дней.
- **Large Title** (800, 28px/1.15, -0.02em): заголовок экрана («Сегодня», дата).
- **Title** (700, 17px): названия карточек и упражнений.
- **Body** (400, 16px/1.45): основной текст, поля ввода (16px — обязим, iOS не зумит).
- **Label** (600, 13px): вторичные подписи, значения подходов.
- **Caption** (700, 11px, +0.06em, uppercase): заголовки групп-списков — родная грамматика iOS, только над группированными списками, не над каждым блоком.

### Named Rules
**Правило железных цифр.** Каждая цифра в интерфейсе — tabular-nums. Дисплейные цифры — только ui-rounded 800.

## Layout

Одна колонка, max-width 560px, отступ 16px по краям. Ритм — кратный 4. Крупные заголовки экрана как в iOS (large title, вплотную к контенту), заголовок группы ближе к своей группе, чем к предыдущей. Плотность повышается в данных (журнал, таблицы диапазонов), дышит на «Сегодня». Safe-area insets соблюдаются сверху и снизу.

## Elevation & Depth

Тональная система: глубина — светлотой слоя (ночь → поверхность → поднятая), границы — волосяные линии 1px rgba(255,255,255,0.08). Тени только у плавающих слоёв: открытая форма записи и тост. Шапка и таб-бар — стекло (backdrop-filter blur 20px saturate 1.4 поверх rgba-ночи), с волосяной линией по кромке.

### Named Rules
**Правило функционального стекла.** Blur существует только там, где контент реально проезжает под панелью: шапка, таб-бар, шторка настроек. Стекло как украшение запрещено.

## Shapes

Мягкая непрерывная геометрия Apple: карточки 16px, контролы 13px, поля 12px, чипы — капсулы. Сегменты коридора — скруглённые прямоугольники 5px. Ни одного острого угла, ни одного цветного border-left. Границы — только волосяные.

## Components

### Buttons
- **Shape:** 13px.
- **Primary:** эмбер, текст-уголь, 800; активное нажатие — ember-pressed + scale(0.97) 160ms.
- **Secondary:** surface-raised + волосяная граница, текст обычный.
- **Danger:** прозрачный, текст #FF5D57; подтверждение — двойной тап (унаследовано).
- **Focus:** outline 2px эмбер со смещением 2px (focus-visible).

### Chips (выбор упражнения)
- **Style:** капсула surface-raised, текст 15px/600; приоритетные — волосяная граница эмбера.
- **State:** выбранный — эмбер с угольным текстом; записанный сегодня — зелёная галочка, прозрачность 0.55.

### Cards / Containers
- **Corner Style:** 16px.
- **Background:** surface; вложенное — surface-raised. Вложенных карточек нет.
- **Border:** волосяная линия. **Shadow:** нет (кроме плавающей формы записи).
- **Internal Padding:** 16px.

### Inputs / Fields
- **Style:** surface-raised, волосяная граница, 12px радиус, 16px шрифт.
- **Focus:** граница эмбер + мягкое свечение эмбера 15% (border-color + box-shadow 0 0 0 3px rgba(255,106,61,0.15)).

### Navigation (таб-бар)
- Стекло, прижат к низу, 4 таба; иконки stroke 1.8, активный — эмбер (иконка и подпись), неактивный — muted. Никакого фона у активного таба — только цвет.

### Коридор объёма (сигнатурный компонент)
Недельный объём группы — ряд сегментов 16×16, r5: сталь — копится, зелень — в зоне (лёгкое свечение box-shadow зелени 25%), янтарь — сверх коридора, пустые до min — контур волосяной. Для групп в повторениях — капсульная шкала с меткой минимума. Заполнение нового сегмента — spring-переход 220ms. Это главный узнаваемый образ приложения.

## Do's and Don'ts

### Do:
- **Do** всё движение 150–250ms, ease-out `cubic-bezier(0.32, 0.72, 0, 1)`; авторский момент один — записанный подход (пульс чипа-счётчика + заполнение сегмента).
- **Do** уважать `prefers-reduced-motion` полностью.
- **Do** контраст текста ≥4.5:1 на своём слое (muted #9AA4AD на surface проходит).
- **Do** `-webkit-tap-highlight-color: transparent` + собственные active-состояния каждому нажимаемому элементу.

### Don't:
- **Don't** светлой темы. Мир всегда ночной; `theme-color` — #0A0C0E.
- **Don't** градиентного текста, декоративного стекла, цветных боковых полос, section-номеров.
- **Don't** оркестровки загрузки экрана: приложение открывается в задачу мгновенно.
- **Don't** внешних ресурсов (шрифты, иконки, CDN) — офлайн священен.
- **Don't** третьего уровня серого текста и второго акцентного цвета.
