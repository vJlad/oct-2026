# 01. Математика

Комбинаторика, теория чисел, CRT, модульная арифметика.
Условия на английском (ICPC-гимны), разборы ниже — на русском.

Формат: 3 часа, индивидуально, 8 задач, ICPC-скоринг.

| # | Задача | Источник | Ссылка | Тема | Сложность | Сдало |
|---|---|---|---|---|---|---|
| A | Adventure in Flatland | Moscow Subregional 2020-21 | [104842A](https://codeforces.com/gym/104842/problem/A) | логика, квадранты | 900 | 490 |
| B | Divisibility Trick | Northern Subregional 2023-24 | [104772D](https://codeforces.com/gym/104772/problem/D) | конструктив, делимость | 1200 | 740 |
| C | Integer Square | Southern & Volga Qualifier 2021-22 | [104013I](https://codeforces.com/gym/104013/problem/I) | сумма двух квадратов | 1400 | 780 |
| D | Halfway There | Northern Subregional 2021-22 | [104011H](https://codeforces.com/gym/104011/problem/H) | симметрия, взаимная простота | 1600 | 469 |
| E | Deep Primes | Moscow Subregional 2020-21 | [104842D](https://codeforces.com/gym/104842/problem/D) | простые, перебор | 1700 | 321 |
| F | Remainders Game | Codeforces 687B (crossover) | [687B](https://codeforces.com/problemset/problem/687/B) | CRT, НОК | 1800 | — |
| G | Game With Stones | Moscow Subregional 2020-21 | [104842G](https://codeforces.com/gym/104842/problem/G) | медианы, транспорт | 2000 | 171 |
| H | Pisano period | Central Russia Regional 2021 | [104454C](https://codeforces.com/gym/104454/problem/C) | модульная арифметика | 2200 | — |

Источники: 104842 — Moscow Subregional 2020-21, 104772 — Northern Subregional
2023-24, 104013 — Southern & Volga Qualifier 2021-22, 104011 — Northern
Subregional 2021-22, 104454 — Central Russia Regional 2021.

## Баланс

- A–C — 15–40 минут: чистая логика и один перебор.
- D–F — ядро контеста, 2–2.5 часа суммарно.
- G–H — на дорешивание. G требует увидеть «транспорт = префиксные суммы»,
  H — знание структуры периода Пизано и умение делить на простые.

## Про CRT

Классического «склей две системы сравнений» в ICPC-четвертьфиналах почти
не встречается, а F (687B) — это CRT в самой полезной формулировке:
«когда остатки по модулям определяют ответ по модулю k». Ответ: тогда и
только тогда, когда `k` делит НОК модулей. Если хочется ещё одну задачу
на явный CRT — можно добавить [1748D ConstructOR](https://codeforces.com/problemset/problem/1748/D)
(2100) как бонус на дорешивание.

## Что обсудить после

1. A и D — обе решаются «посмотри на симметрию», и обе убивают тех, кто
   начинает перебирать.
2. E — почему перебор до `10^18` не нужен: множество ответов конечно,
   и это надо доказать, а не предположить.
3. G — почему медиана покоординатно оптимальна (выпуклость суммы модулей)
   и почему ответ автоматически даёт неотрицательные `b_i`.
