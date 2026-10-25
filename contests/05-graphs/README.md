# 05. Графы и пути

BFS/DFS, кратчайшие пути, деревья, LCA, DSU, графовые конструктивы.

Формат: 3 часа, индивидуально, 8 задач, ICPC-скоринг.
Условия на английском, разборы на русском.

| # | Задача | Источник | Ссылка | Тема | Сложность | Сдало |
|---|---|---|---|---|---|---|
| A | Build the Non-Cactus | Moscow Subregional 2021-22 | [104848F](https://codeforces.com/gym/104848/problem/F) | конструктив графа | 1300 | 438 |
| B | The Two Routes | Codeforces 601A | [601A](https://codeforces.com/problemset/problem/601/A) | BFS в дополнении | 1500 | — |
| C | Edgy Trees | Codeforces 1139C | [1139C](https://codeforces.com/problemset/problem/1139/C) | DSU + степени | 1600 | — |
| D | Fare | Central Russia Regional 2022 | [104805C](https://codeforces.com/gym/104805/problem/C) | LCA + произведения | 1700 | 139 |
| E | Just the Last Digit | Northern Subregional 2019-20 | [104874J](https://codeforces.com/gym/104874/problem/J) | восстановление DAG | 1800 | 278 |
| F | Equidistant | Northern Subregional 2019-20 | [104874E](https://codeforces.com/gym/104874/problem/E) | диаметр, середины | 1800 | 301 |
| G | Dijkstra? | Codeforces 20C | [20C](https://codeforces.com/problemset/problem/20/C) | Дейкстра + путь | 1900 | — |
| H | The Shortest Statement | Codeforces 1051F | [1051F](https://codeforces.com/problemset/problem/1051/F) | остов + LCA + Дейкстра | 2400 | — |

Источники: 104848 — Moscow Subregional 2021-22, 104805 — Central Russia
Regional 2022, 104874 — Northern Subregional 2019-20.

## Баланс

- A–C — 20–40 минут: конструктив, BFS по дополнению, DSU.
- D–F — ядро: LCA, восстановление графа по числам путей, работа
  с диаметром дерева.
- G–H — на дорешивание. G — техника восстановления пути в Дейкстре
  (её многие пишут с ошибками), H — «а что если рёбер почти как в дереве».

## Что обсудить после

1. B — почему ровно у одного из двух транспортов есть прямое ребро `1 → n`,
   и почему из-за этого конфликт «приехали одновременно» не возникает.
2. E — почему номер строки обрабатывается с конца и почему `a[i][j]`
   сравнивается с уже посчитанным числом путей, а не с нулём.
3. H — почему `m − n ≤ 20` — это подсказка «дерево + 20 лишних рёбер»,
   а не «нужно что-то сложное».
