# 08. Конструктивы

Интерактив, двойной запуск, игры, стратегии, «постройте объект с нужным
свойством».

Формат: 3 часа, индивидуально, 9 задач, ICPC-скоринг.
Условия на английском, разборы на русском.

| # | Задача | Источник | Ссылка | Тема | Сложность | Сдало |
|---|---|---|---|---|---|---|
| A | Pills | Central Russia 2024 | [106035L](https://codeforces.com/gym/106035/problem/L) | интерактив, одно взвешивание | 1400 | 352 |
| B | Encode and Decode (Easy) | Codeforces 2168A1 | [2168A1](https://codeforces.com/problemset/problem/2168/A1) | **двойной запуск**, вход в формат | 1500 | — |
| C | Composite Coloring | Codeforces 1332B | [1332B](https://codeforces.com/problemset/problem/1332/B) | конструктив по простым | 1600 | — |
| D | Problem on array | Central Russia 2022 | [104805I](https://codeforces.com/gym/104805/problem/I) | интерактив, сортировка за `2N` | 1700 | 157 |
| E | Guess the K-th Zero | Codeforces 1520F1 | [1520F1](https://codeforces.com/problemset/problem/1520/F1) | интерактив, бинпоиск | 1700 | — |
| F | String Equality | Codeforces 1451C | [1451C](https://codeforces.com/problemset/problem/1451/C) | жадность по алфавиту | 1800 | — |
| G | Eight-Connected Figures | Northern Subregional 2025-26 | [106193E](https://codeforces.com/gym/106193/problem/E) | интерактив по случайной сетке | 1900 | 199 |
| H | Engineer Artem | Codeforces 1438C | [1438C](https://codeforces.com/problemset/problem/1438/C) | конструктив по чётности | 2000 | — |
| I | Oriented Journey | Codeforces 2215C | [2215C](https://codeforces.com/problemset/problem/2215/C) | **двойной запуск**, канал связи | 2200 | — |

Источники: 106035 — Central Russia Regional 2024, 104805 — Central Russia
Regional 2022, 106193 — Northern Subregional 2025-26.

## Про двойной запуск

Это формат, а не тема: решение исполняется **дважды**. В первом запуске
программа получает данные и выдаёт «сообщение» жюри; во втором запуске
она получает это сообщение (и больше ничего) и должна восстановить ответ.
Память между запусками не сохраняется — весь канал связи ограничен тем,
что вы напечатали.

На Codeforces у этого есть тег **`communication`**. Всего таких задач 11,
и они перечислены ниже — можно набирать второй контест только из них:

| Задача | Сложность | О чём |
|---|---|---|
| [2168A1](https://codeforces.com/problemset/problem/2168/A1) | ~1500 | закодировать массив в строку (лёгкая версия) |
| [2168A2](https://codeforces.com/problemset/problem/2168/A2) | ~1900 | то же, но `a_i` большие |
| [2168B](https://codeforces.com/problemset/problem/2168/B) | ~2000 | один бит + 30 запросов: найти позицию `n` |
| [2179F](https://codeforces.com/problemset/problem/2179/F) | 2000 | раскраска в 3 цвета, чтобы путник шёл к корню |
| [2255C](https://codeforces.com/problemset/problem/2255/C) | 2100 | картинка под сдвигами/поворотами/инверсией |
| [2215C](https://codeforces.com/problemset/problem/2215/C) | 2200 | ориентировать рёбра дерева, чтобы передать число |
| [2168C](https://codeforces.com/problemset/problem/2168/C) | ~2200 | перехват бабочек |
| [2214G](https://codeforces.com/problemset/problem/2214/G) | ~2400 | — |
| [2163E](https://codeforces.com/problemset/problem/2163/E) | 2700 | Plegma |
| [2237G](https://codeforces.com/problemset/problem/2237/G) | 2900 | Send GCDs |
| [2261H](https://codeforces.com/problemset/problem/2261/H) | 3500 | дерево |

В контест вошли две: **B** — вход в формат (закодировать массив в строку),
**I** — содержательная (передать `n−1` бит через ориентацию рёбер дерева,
которого не видишь).

## Баланс

- A–C — 20–40 минут: интерактив и первый двойной запуск.
- D–F — ядро: бюджеты запросов и жадность.
- G–I — на дорешивание: оценка ожидания, локальный инвариант и канал связи.

## Что обсудить после

1. B — почему в лёгкой версии хватает одного символа на элемент, и что
   ломается, когда `a_i` большие.
2. I — что именно является «каналом» между запусками (порядок рёбер и их
   ориентация) и почему без соглашения «меньшая метка первой» декодер
   не сможет прочитать бит.
3. G — почему при `p = 1/2` и 8-связности BFS по компоненте укладывается
   в лимит запросов.
