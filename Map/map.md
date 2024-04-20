## Map

`Map` - ассоциативный массив(словарь, хеш-таблица), использует в своей основе хеш-таблицы. 

`unsafe.Pointer` - Указатель на данные любого типа, нужны для того, чтобы реализовать функционал map с любыми типами ключей и значений (способ разработчиков уйти от дженериков)

``` go
// Объявление
var person map[string]string

// Объявление с инициализацией 
var person = map[string]string {
    "name": "qq",
    "surname": "ww",
}

// Поиск значение по ключю, если ключа нет, то вернет значение по умолчанию
Name := person["name"]

// Проверка на существование ключа
// exists - true, если ключ существует, иначе - false
Name, exists := person["name"]
```
<br> `Функции для работы с map:`
``` go
// Возвращает lenght
len(person)

// Удаление ключа
delete(person, "name")

// Аллокация памяти для map (тип map, lenght)
person := make(map[string]string, 10)

```

``` go
// Использование for-range для map
var person = map[string]string {
    "name": "qq",
    "surname": "ww",
}

for i, value := range person {
    // i - Ключ
    // value - Значение
	fmt.Println(i, value)
}

// Вывод
// surname ww
// name qq
```


Выполняет 3 основные функции:
- Search (Время поиска - константное O(1))
- Delet
- Lookup