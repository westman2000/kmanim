# Журнал паритета API (API Parity Log)

Этот документ сопоставляет API оригинального Manim (ManimCE) с API нативного Android-движка KManim на Kotlin.

**Легенда статусов:**
- ✅ Готово (полный паритет)
- 🟡 Частично реализовано (с ограничениями)
- ⬜ Не реализовано (в планах)
- ❌ Не портируем (вне области видимости)

## MObjects (Геометрия и фигуры)

| Manim (ManimCE) | KManim (Kotlin) | Статус | Заметка / Спринт |
|-----------------|-----------------|--------|-------------------|
| `Circle` | `circle(...)` | ⬜ | Запланировано (Спринт 1) |
| `Square` | `square(...)` | ⬜ | Запланировано (Спринт 2) |
| `Line` | `line(...)` | ⬜ | Запланировано (Спринт 2) |
| `Polygon` | `polygon(...)` | ⬜ | Запланировано (Спринт 2) |

## Анимации

| Manim (ManimCE) | KManim (Kotlin) | Статус | Заметка / Спринт |
|-----------------|-----------------|--------|-------------------|
| `Create` | `Create(...)` | ⬜ | Запланировано (Спринт 1) |
| `FadeIn` | `FadeIn(...)` | ⬜ | Запланировано (Спринт 2) |
| `FadeOut` | `FadeOut(...)` | ⬜ | Запланировано (Спринт 2) |
| `Shift` | `Shift(...)` / `.animate.shift()`| ⬜ | Запланировано (Спринт 2) |
| `Transform` | `Transform(...)` | ⬜ | Запланировано (Спринт 3) |
| `Mobject.match_points` | `VMobject.matchPoints(...)` | ⬜ | Метод объекта, не билдер `Transform` (Спринт 3, D-24) |
| `TransformMatchingShapes` | `TransformMatchingShapes(...)` | ⬜ | Сопоставление частей сложных морфингов (roadmap, Спринт 8+) |
| `TransformMatchingTex` | `TransformMatchingTex(...)` | ⬜ | Сопоставление частей формул (roadmap, Спринт 8+) |

## Текст и Формулы

| Manim (ManimCE) | KManim (Kotlin) | Статус | Заметка / Спринт |
|-----------------|-----------------|--------|-------------------|
| `Text` | `TextLabel(...)` | ⬜ | Растровый (Спринт 4) |
| (нет прямого аналога) | `VectorText(...)` | ⬜ | Контурный (Спринт 4) |
| `Tex` (text-mode) | `tex(...)` | ⬜ | LaTeX text-режим, отдельно от `MathTex` (Спринт 5, D-42) |
| `MathTex` | `mathTex(...)` | ⬜ | Math-режим; + индексация подвыражений (`substringsToIsolate`) (Спринт 5) |

## Галерея примеров (examples.html — исполняемая спецификация паритета)

Перечислимая опись реальной галереи ManimCE (4 секции, 19 сцен; *сверено по v0.20.1, перепроверить* — D-14/D-42). Каждая сцена воспроизводится на нашем DSL и прогоняется golden-эшелоном «manim-parity».

| Секция | Сцена ManimCE | Статус | Заметка |
|--------|---------------|--------|---------|
| Basic Concepts | `ManimCELogo` | ⬜ | |
| Basic Concepts | `BraceAnnotation` | ⬜ | |
| Basic Concepts | `VectorArrow` | ⬜ | |
| Basic Concepts | `GradientImageFromArray` | ❌/🟡 | Работа с растром/массивом — уточнить портируемость |
| Basic Concepts | `BooleanOperations` | ⬜ | Булевы операции над путями |
| Animations | `PointMovingOnShapes` | ⬜ | |
| Animations | `MovingAround` | ⬜ | |
| Animations | `MovingAngle` | ⬜ | |
| Animations | `MovingDots` | ⬜ | |
| Animations | `MovingGroupToDestination` | ⬜ | |
| Animations | `MovingFrameBox` | ⬜ | |
| Animations | `RotationUpdater` | ⬜ | Требует механизм `Updater` (Спринт 8+) |
| Animations | `PointWithTrace` | ⬜ | |
| Plotting with Manim | `SinAndCosFunctionPlot` | ⬜ | Спринт 6 |
| Plotting with Manim | `ArgMinExample` | ⬜ | Спринт 6 |
| Plotting with Manim | `GraphAreaPlot` | ⬜ | Спринт 6 |
| Plotting with Manim | `PolygonOnAxes` | ⬜ | Спринт 6 |
| Plotting with Manim | `HeatDiagramPlot` | ⬜ | Спринт 6 |
| Special Camera Settings | `FollowingGraphCamera` | ⬜ | Управление камерой (Спринт 8+) |

*Этот документ будет расширяться по мере прохождения спринтов.*
