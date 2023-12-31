## Задание №3. 
### Попарное тестирование
___
На сайте  https://www.saucedemo.com/ при авторизации есть два поля:  "Username" и "Password".

Значение  "Username" может быть: 
   - пустое
   - не верное
   - standard_user
   - locked_out_user
   - problem_user
   - performance_glitch_user

Значение "Password" может быть:
   - пустое
   - не верное
   - secret_sauce

Теперь составим комбинации из этих значений. В этом может помочь сервис на сайте https://pairwise.teremokgames.com/

__Таблица вариантов ввода  "Username" и "Password"___

|№|Username|Password|
|:-|:-|:-|
|1|Пустое	|Пустое|
|2|Пустое	|secret_sauce|
|3|Пустое	|не верное|
|4|standard_user	|secret_sauce|
|5|standard_user	|не верное|
|6|standard_user	|Пустое|
|7|locked_out_user	|не верное|
|8|locked_out_user	|Пустое|
|9|locked_out_user	|secret_sauce|
|10|problem_user	|Пустое|
|11|problem_user	|secret_sauce|
|12|problem_user	|не верное|
|13|performance_glitch_user	| secret_sauce|
|14|performance_glitch_user	| не верное|
|15|performance_glitch_user	| Пустое|
|16|Не верное	|не верное|
|17|Не верное	|Пустое|
|18|Не верное	|secret_sauce|

Составляем тест-кейсы для этих вариантов.

## Тест-кейс №1 — Прохождения авторизации.
1. Предшествующие условия:
    - открыт сайт https://www.saucedemo.com/
    - пользователь не авторизован
2. Шаги:
   - поле "Username" пустое
   - поле "Password" пустое 
   - навести курсор и нажать на кнопку Login
3. Ожидаемый результат:
   - ошибка авторизации "Epic sadface: Username is required".
___

## Тест-кейс №2 — Прохождения авторизации.
1. Предшествующие условия:
    - открыт сайт https://www.saucedemo.com/
    - пользователь не авторизован
2. Шаги:
   - поле "Username" пустое
   - в поле "Password" ввести латинскими буквами "secret_sauce"
   - навести курсор и нажать на кнопку Login
3. Ожидаемый результат:
   - ошибка авторизации "Epic sadface: Username is required".
___

## Тест-кейс №3 — Прохождения авторизации.
1. Предшествующие условия:
    - открыт сайт https://www.saucedemo.com/
    - пользователь не авторизован
2. Шаги:
   - поле "Username" пустое
   - в поле "Password" ввести любое значение, любой раскладкой клавиатуры
   - навести курсор и нажать на кнопку Login
3. Ожидаемый результат:
   - ошибка авторизации "Epic sadface: Username is required".
___

## Тест-кейс №4 — Прохождения авторизации.
1. Предшествующие условия:
    - открыт сайт https://www.saucedemo.com/
    - пользователь не авторизован
2. Шаги:
   - в поле "Username" ввести латинскими буквами "standard_user"
   - в поле "Password" ввести латинскими буквами "secret_sauce"
   - навести курсор и нажать на кнопку Login
3. Ожидаемый результат:
   - успешная авторизация.
___

## Тест-кейс №5 — Прохождения авторизации.
1. Предшествующие условия:
    - открыт сайт https://www.saucedemo.com/
    - пользователь не авторизован
2. Шаги:
   - в поле "Username" ввести латинскими буквами "standard_user"
   - в поле "Password" ввести ввести любое значение, любой раскладкой клавиатуры
   - навести курсор и нажать на кнопку Login
3. Ожидаемый результат:
   - ошибка авторизации "Epic sadface: Username and password do not match any user in this service".
___

## Тест-кейс №6 — Прохождения авторизации.
1. Предшествующие условия:
    - открыт сайт https://www.saucedemo.com/
    - пользователь не авторизован
2. Шаги:
   - в поле "Username" ввести латинскими буквами "standard_user"
   - в поле "Password" ничего не вводим
   - навести курсор и нажать на кнопку Login
3. Ожидаемый результат:
   - ошибка авторизации "Epic sadface: Password is required".
___

## Тест-кейс №7 — Прохождения авторизации.
1. Предшествующие условия:
    - открыт сайт https://www.saucedemo.com/
    - пользователь не авторизован
2. Шаги:
   - в поле "Username" ввести латинскими буквами "locked_out_user"
   - в поле "Password" ввести ввести любое значение, любой раскладкой клавиатуры
   - навести курсор и нажать на кнопку Login
3. Ожидаемый результат:
   - ошибка авторизации "Epic sadface: Username and password do not match any user in this service".
___

## Тест-кейс №8 — Прохождения авторизации.
1. Предшествующие условия:
    - открыт сайт https://www.saucedemo.com/
    - пользователь не авторизован
2. Шаги:
   - в поле "Username" ввести латинскими буквами "locked_out_user"
   - поле "Password" пустое
   - навести курсор и нажать на кнопку Login
3. Ожидаемый результат:
   - ошибка авторизации "Epic sadface: Password is required".
___

## Тест-кейс №9 — Прохождения авторизации.
1. Предшествующие условия:
    - открыт сайт https://www.saucedemo.com/
    - пользователь не авторизован
2. Шаги:
   - в поле "Username" ввести латинскими буквами "locked_out_user"
   - в поле "Password" ввести латинскими буквами "secret_sauce"
   - навести курсор и нажать на кнопку Login
3. Ожидаемый результат:
   - ошибка авторизации "Epic sadface: Sorry, this user has been locked out.".
___

## Тест-кейс №10 — Прохождения авторизации.
1. Предшествующие условия:
    - открыт сайт https://www.saucedemo.com/
    - пользователь не авторизован
2. Шаги:
   - в поле "Username" ввести латинскими буквами "problem_user"
   - поле "Password" пустое
   - навести курсор и нажать на кнопку Login
3. Ожидаемый результат:
   - ошибка авторизации "Epic sadface: Password is required".
___

## Тест-кейс №11 — Прохождения авторизации.
1. Предшествующие условия:
    - открыт сайт https://www.saucedemo.com/
    - пользователь не авторизован
2. Шаги:
   - в поле "Username" ввести латинскими буквами "problem_user"
   - в поле "Password" ввести латинскими буквами "secret_sauce"
   - навести курсор и нажать на кнопку Login
3. Ожидаемый результат:
   - авторизации прошла успешно.
___

## Тест-кейс №12 — Прохождения авторизации.
1. Предшествующие условия:
    - открыт сайт https://www.saucedemo.com/
    - пользователь не авторизован
2. Шаги:
   - в поле "Username" ввести латинскими буквами "problem_user"
   - в поле "Password" ввести ввести любое значение, любой раскладкой клавиатуры
   - навести курсор и нажать на кнопку Login
3. Ожидаемый результат:
   - ошибка авторизации "Epic sadface: Username and password do not match any user in this service".
___

## Тест-кейс №13 — Прохождения авторизации.
1. Предшествующие условия:
    - открыт сайт https://www.saucedemo.com/
    - пользователь не авторизован
2. Шаги:
   - в поле "Username" ввести латинскими буквами "performance_glitch_user"
   - в поле "Password" ввести "secret_sauce"
   - навести курсор и нажать на кнопку Login
3. Ожидаемый результат:
   - успешная авторизация.
___

## Тест-кейс №14 — Прохождения авторизации.
1. Предшествующие условия:
    - открыт сайт https://www.saucedemo.com/
    - пользователь не авторизован
2. Шаги:
   - в поле "Username" ввести латинскими буквами "performance_glitch_user"
   - в поле "Password" ввести ввести любое значение, любой раскладкой клавиатуры
   - навести курсор и нажать на кнопку Login
3. Ожидаемый результат:
   - ошибка авторизации "Epic sadface: Username and password do not match any user in this service".
___

## Тест-кейс №15 — Прохождения авторизации.
1. Предшествующие условия:
    - открыт сайт https://www.saucedemo.com/
    - пользователь не авторизован
2. Шаги:
   - в поле "Username" ввести латинскими буквами "performance_glitch_user"
   - поле "Password" пустое
   - навести курсор и нажать на кнопку Login
3. Ожидаемый результат:
   - ошибка авторизации "Epic sadface: Password is required".
___

## Тест-кейс №16 — Прохождения авторизации.
1. Предшествующие условия:
    - открыт сайт https://www.saucedemo.com/
    - пользователь не авторизован
2. Шаги:
   - в поле "Username" ввести ввести любое значение, любой раскладкой клавиатуры
   - в поле "Password" ввести ввести любое значение, любой раскладкой клавиатуры
   - навести курсор и нажать на кнопку Login
3. Ожидаемый результат:
   - ошибка авторизации "Epic sadface: Username and password do not match any user in this service".
___

## Тест-кейс №17 — Прохождения авторизации.
1. Предшествующие условия:
    - открыт сайт https://www.saucedemo.com/
    - пользователь не авторизован
2. Шаги:
   - в поле "Username" ввести ввести любое значение, любой раскладкой клавиатуры
   - поле "Password" пустое
   - навести курсор и нажать на кнопку Login
3. Ожидаемый результат:
   - ошибка авторизации "Epic sadface: Password is required".
___

## Тест-кейс №18 — Прохождения авторизации.
1. Предшествующие условия:
    - открыт сайт https://www.saucedemo.com/
    - пользователь не авторизован
2. Шаги:
   - в поле "Username" ввести любое значение, любой раскладкой клавиатуры
   - поле "Password" ввести "secret_sauce"
   - навести курсор и нажать на кнопку Login
3. Ожидаемый результат:
   - ошибка авторизации "Epic sadface: Username and password do not match any user in this service".
___