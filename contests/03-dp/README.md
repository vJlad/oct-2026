# 03. ДП

Одномерное, двумерное, по профилю, по дереву, по подмножествам.
Условия на английском, разборы на русском.

Формат: 3 часа, индивидуально, 8 задач, ICPC-скоринг.

| # | Задача | Источник | Ссылка | Тема | Сложность | Сдало |
|---|---|---|---|---|---|---|
| A | An oscillating subsequence | Central Russia Regional 2025 | [106189D](https://codeforces.com/gym/106189/problem/D) | ЛИС, жадность | 1300 | 256 |
| B | Tree Painting | Southern & Volga Qualifier 2021-22 | [104015I](https://codeforces.com/gym/104015/problem/I) | ДП по дереву, размеры | 1400 | 477 |
| C | Chain Reaction | Codeforces 607A (crossover) | [607A](https://codeforces.com/problemset/problem/607/A) | 1D ДП, бинпоиск | 1600 | — |
| D | Bicolorings | Codeforces 1051D (crossover) | [1051D](https://codeforces.com/problemset/problem/1051/D) | **ДП по профилю** | 1700 | — |
| E | Distance in Tree | Codeforces 161D (crossover) | [161D](https://codeforces.com/problemset/problem/161/D) | ДП по дереву | 1800 | — |
| F | RBS | Southern & Volga Qualifier 2021-22 | [104015L](https://codeforces.com/gym/104015/problem/L) | ДП по подмножествам | 1900 | 114 |
| G | Tree problem | Central Russia Regional 2024 | [106035G](https://codeforces.com/gym/106035/problem/G) | DSU на дереве | 2000 | 243 |
| H | Roman and Numbers | Codeforces 401D (crossover) | [401D](https://codeforces.com/problemset/problem/401/D) | ДП по маске + остаток | 2000 | — |

Источники: 106189 — Central Russia Regional 2025, 104015 — Southern & Volga
Qualifier 2021-22, 106035 — Central Russia Regional 2024.

## Про источники и «профиль»

В четвертьфиналах NERC чистых задач «посчитайте ДП по профилю» почти нет:
профильное ДП там живёт внутри задач на замощения и раскраски, которых
в открытых гимнах немного. Поэтому D (1051D) — crossover из раунда CF:
это эталонная задача на профиль (2×n, маска столбца, число компонент),
и на ней удобно объяснять технику.

Остальное — ICPC: A, B, F, G. B и G — про деревья (размеры поддеревьев и
small-to-large), F — про подмножества, A — про ЛИС.

## Баланс

- A–B — 15–30 минут: обе решаются после одной идеи.
- C–E — ядро, 1.5 часа.
- F–H — на дорешивание: F требует аккуратной верхней оценки на `2^n · n`,
  G — техники «сливаем меньшие карты в большие», H — маски + остаток.

## Что обсудить после

1. D — почему нельзя считать «раскраски независимо по столбцам»: компоненты
   склеиваются через границу, и именно это ловит маска.
2. F — почему нельзя просто переставлять строки жадно, и почему состояние
   «набор использованных строк» достаточно (баланс восстанавливается).
3. G — почему наивное слияние `map` даёт `O(n^2)` и как размер поддерева
   спасает ситуацию.
