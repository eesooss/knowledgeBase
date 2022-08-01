# Optionals



Тип **optional** в Swift — это enum, который может иметь одно из двух значений: None или Some(T), где T — это любой тип данных. С его помощью можно обезопасить себя от попытки доступа к nil значению.

Существует несколько способов развернуть optional:

* Проверка на nil:

```swift
let a: String? = “string”
```

* Guard let:

```swift
guard let a = a else { return }
```

* If let:

```swift
if let a = a {
    print(a)
} else {
    print("Error")
```

* Force unwrapping — это небезопасный способ, если значение равно nil, программа завершится:

```swift
print(a!)
```

* Nil coalescing:

```swift
print(a ?? "Error")
```

* Optional chaining:

```swift
print(a?.uppercased())
```

Также **optional** используется в приведении типов:

```swift
let b = (a as? Int) // b будет равно nil, если a нельзя преобразовать в Int
```

```swift
let b = (a as! Int) //если а нельзя преобразовать в Int, программа завершится
```
