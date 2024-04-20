## Functions

``` go
    func enterTheClub (age int) (string, bool) {
	if age >= 18 {
		return "Входи", true
	} else {
		return "Не входи", false
	}
}
```
(age int) - Принимаемый параметр
(string, bool) - Возвращаемые значения (В Go может быть больше одного возвращаемого значения) 
