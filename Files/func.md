## Higher-order functions

### allSatisfy()
Способ проверить: все ли элементы коллекции удовлетворяют заданному условию 

_Implemented since Swift 4.2_
```swift
let allScores = [8.4, 4.4, 9.5, 8.7]
let moviesToWatch = allScores.allSatisfy { $0 >= 7.5 } // false
```