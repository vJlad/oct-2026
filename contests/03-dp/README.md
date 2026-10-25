# 03. ДП

Одномерное, двумерное, по профилю, цифровое, по дереву, по подмножествам.
Условия на английском, разборы на русском.

Формат: 3 часа, индивидуально, 9 задач, ICPC-скоринг.

| # | Задача | Источник | Ссылка | Тема | Сложность | Сдало |
|---|---|---|---|---|---|---|
| A | An oscillating subsequence | Central Russia 2025 | [106189D](https://codeforces.com/gym/106189/problem/D) | ЛИС, экстремумы | 1300 | 256 |
| B | Tree Painting | Southern & Volga Qualifier 2021-22 | [104015I](https://codeforces.com/gym/104015/problem/I) | размеры поддеревьев | 1400 | 477 |
| C | Chain Reaction | Codeforces 607A | [607A](https://codeforces.com/problemset/problem/607/A) | 1D ДП, бинпоиск | 1600 | — |
| D | Bicolorings | Codeforces 1051D | [1051D](https://codeforces.com/problemset/problem/1051/D) | **ДП по профилю** | 1700 | — |
| E | Magic Numbers | Codeforces 628D | [628D](https://codeforces.com/problemset/problem/628/D) | **цифровая ДП** | 1800 | — |
| F | Distance in Tree | Codeforces 161D | [161D](https://codeforces.com/problemset/problem/161/D) | ДП по дереву | 1800 | — |
| G | RBS | Southern & Volga Qualifier 2021-22 | [104015L](https://codeforces.com/gym/104015/problem/L) | ДП по подмножествам | 1900 | 114 |
| H | Tree problem | Central Russia 2024 | [106035G](https://codeforces.com/gym/106035/problem/G) | DSU на дереве | 2000 | 243 |
| I | Roman and Numbers | Codeforces 401D | [401D](https://codeforces.com/problemset/problem/401/D) | маска + остаток | 2000 | — |

Источники: 106189 — Central Russia Regional 2025, 104015 — Southern & Volga
Qualifier 2021-22, 106035 — Central Russia Regional 2024.

## Про профиль и цифры

В четвертьфиналах NERC чистых задач «ДП по профилю» и «цифровая ДП» нет:
первое живёт внутри задач на замощения, второе — почти всегда в раундах CF.
Поэтому D (1051D) и E (628D) — crossover'ы, и оба выбраны как эталонные:
на них техника объясняется за 10 минут, а дальше студент узнаёт её сам.

- D — состояние «маска столбца + число компонент», переход по 16 вариантам.
- E — состояние «позиция + остаток + флаг tight», переход по цифре.

Остальное — ICPC: A, B, G, H.

## Баланс

- A–C — 15–30 минут.
- D–F — ядро, 1.5 часа: профиль, цифры, дерево.
- G–I — на дорешивание.

## Что обсудить после

1. D — почему нельзя считать столбцы независимо: компоненты склеиваются
   через границу.
2. E — почему `f(b) − f(a−1)` считается одной функцией, и почему длина
   фиксирована (все числа отрезка одной длины).
3. G — почему состояние «набор использованных строк» достаточно: баланс
   восстанавливается по маске.
4. H — почему наивное слияние `map` даёт `O(n^2)` и как размер поддерева
   спасает ситуацию.
