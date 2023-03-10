*Задание:*

Реализуйте функцию exceptionSafeInvoke, которая аналогична std::invoke, но при этом не выпускает из себя исключения,
т.е.:

- Если Callabale возвращает void, то exceptionSafeInvoke() должна возвращать bool (false, если произошло любое
  исключение).
- Если Callabale возвращает T != void, то exceptionSafeInvoke() должна возвращать std::optional<T> (nullopt, если
  произошло любое исключение).

*Реализация:*

- Функция получает на вход Callable объект и аргументы.

- Далее происходит вызов функции.

- Обрабатываются исключения, как описано в задании.

- Возвращаемые типы: bool, std::optional<'T'>.

*Демонстрационная программа:*

Выполняется вызов функций.

*Сборка:*

```bash
cmake -B build
cmake --build build
```

*Запуск:*

```bash
./build/invoke
```

*Запуск тестов:*

```bash
./build/test/test_run
```

*Интеграционные тесты:*

```bash
bash test/integr/test.sh
```
