# goit-algo-hw-09
# Жадібні алгоритми та динамічне програмування



# Висновки щодо ефективності алгоритмів видачі решти

## Вступ
Домашнє завдання полягало в розробці двох алгоритмів для видачі решти покупцеві: жадібного алгоритму та алгоритму динамічного програмування. У цьому файлі ми проаналізуємо ефективність кожного з них та зробимо висновки щодо їх придатності для різних сценаріїв використання.

## Оцінка часу виконання
Порівняння ефективності алгоритмів ґрунтувалося на вимірюванні часу виконання функцій для видачі решти на прикладі суми в 113 одиниць. Було використано жадібний алгоритм (`find_coins_greedy`) та алгоритм динамічного програмування (`find_min_coins`). Основні результати:

1. **Жадібний алгоритм**
   - Виконується дуже швидко, оскільки просто перебирає доступні номінали монет від найбільшого до найменшого, що забезпечує малу кількість ітерацій.
   - Час виконання є лінійним відносно кількості доступних номіналів: **O(N)**, де **N** - кількість номіналів.
   - Проте, жадібний алгоритм не завжди гарантує мінімальну кількість монет для всіх можливих сум, оскільки використовує локально оптимальні рішення.

2. **Алгоритм динамічного програмування**
   - Гарантує мінімальну кількість монет для будь-якої заданої суми, оскільки розглядає всі можливі комбінації.
   - Час виконання є квадратичним: **O(N * M)**, де **N** - кількість номіналів монет, а **M** - сума, яку потрібно видати. Таким чином, для великих сум час виконання може бути значним.
   - Алгоритм динамічного програмування є більш ресурсоємним через необхідність зберігати та обчислювати проміжні значення для кожної можливої суми.

## Висновки
- **Жадібний алгоритм** добре підходить для випадків, коли потрібно швидко знайти розв'язок і коли набір номіналів монет дозволяє завжди знаходити мінімальну кількість монет (як у випадку євро або гривні).
- **Алгоритм динамічного програмування** є кращим вибором для випадків, коли необхідно знайти абсолютно оптимальне рішення, особливо якщо номінали монет не є стандартизованими або мають складні співвідношення.
- Для великих сум алгоритм динамічного програмування стає менш ефективним через його квадратичну складність, тоді як жадібний алгоритм, хоча і не завжди оптимальний, виконується швидко навіть для великих сум.

У підсумку, вибір алгоритму залежить від вимог до точності та продуктивності. Якщо точність не є критичною, жадібний алгоритм є кращим вибором завдяки своїй швидкості. Якщо ж критично знайти мінімальну кількість монет, тоді варто застосовувати динамічне програмування, незважаючи на збільшений час виконання.

