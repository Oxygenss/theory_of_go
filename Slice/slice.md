## Slice

`Слайс` - это тип данных, последовательность динамической длины (динамический массив). По сути своей слайс - это структура, которая состоит из трех элементов:
указатель на базовый массив, lenght (количество элементов, которые используются в слайсе), capacity (количество элементов, которые влезают в базовый массив)

``` go
// Упрощенная структура Slice
type slice struct {
    lenght    int
    capacity  int
    baseArray *int
}
```

``` go
// Объявление слайса 
var slice []int

// Объявление с инициализацией 
slice := []int{1, 2, 3, 4}
```

Функции для работы со слайсом:

``` go
// Возвращает lenght
len(slice)

// Возвращает capacity
cap(slice)

// Добавление элемента
slice = append(slice, 5)

// Копирование значение из одного слайса в другой
copy(new_slice, old_slice)

// Аллокация памяти для слайса (тип слайса, lenght, capacity)
slice := make([]int, 5, 10)
```


``` go
// Использование for-range для слайса
slice := []int{45, 65, 32, 65}

for i, value := range slice {
    // i - Номер элемента
    // value - Значение элемента
	fmt.Println(i, value)
}

// Вывод
// 0 45
// 1 65
// 2 32
// 3 65
```

Полезные практики:

- Проверять слайс на пустоту с помощью len(list) == 0
- По возможности, аллоцировать память для слайса 
- Создавать новую копию переданного в функцию слайса, если не хотим изменять его, но работать с его значениями
- Результат append присваивать той же переменной