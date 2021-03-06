# Рубежный контроль 2

### Инструкция
Прототипы функций должны быть вынесены в `.hpp` файл.
Все `.cpp` файлы добавить в `CMakeLists.txt`

### Задание 1
Реализовать функцию `digit_count`, которая вернет количество цифр в строке. Воспользуйтесь функцией `isdigit`
Пример использования функции:
```cpp
std::string s = "0a 13";
int cnt = digit_count(s);
// cnt == 3
```

**Прототип:**
```cc
size_t digit_count(const std::string& str);
```


### Задание 2
Дан динамический массив слов. Требуется реализовать функцию сортировки `custom_sort` по возрастанию этого массива. В качестве условия сравнения использовать количество цифр в строке.
Например, строка `ccc1` меньше чем строка `aa22`, потому что в ней меньше цифр.

**Прототип:**
```cc
void custom_sort(std::vector<std::string>& str);
```

### Задание 3
Реализовать функцию `zip`, которая преобразует два массива в `map`, где значения из первого массива являются ключами, а значения второго массива значениями в `map`. Если входные аргументы разного размера, то вернуть пустой словарь.

Пример использования функции:
```cpp
std::vector<std::string> k = {"a", "b", "c"};
std::vector<int> v = {0, 1, 2};
std::map<std::string, int> dict = zip(k, v);
// dict == {{"a", 0}, {"b", 1}, {"c", 2}}
```

**Прототип:**
```cc
std::map<std::string, int> zip(const std::vector<std::string>& keys,
                               const std::vector<int>& values);
```

### Задание 4
Реализовать функцию, которая удаляет из списка все числа, количесто которых больше чем 1.

Пример использования функции:
```cpp
std::list<int> words = {1, 1, 2, 3, 4, 5};
clear(words);
// words == {2, 3, 4, 5};
// удалили все 1, потому что в списке их 2
// 2, 3, 4, 5 оставили, потому что в списке их по 1
```

**Прототип:**
```cc
void clear(std::list<int>& numers);
```

### Задание 5
Реализовать функцию, которая разворачивает `std::map<std::string, int>` в `std::vector<std::string>`. См. пример

Пример использования функции:
```cpp
std::map<std::string, int> dict = {{"a", 0}, {"b", 1}, {"c", 3}, {"d", 2}};
std::vector<std::string> v = unzip(dict);
// v == {"b", "c", "c", "c", "d", "d"};
// массив состоит из нуля строк "a", из одного слова "b", из трех слов "c" и из двух слов "d"
```

**Прототип:**
```cc
std::vector<std::string> unzip(const std::map<std::string, int>& numers);
```
