# Note-do-Swift

## Variáveis

```swift

import UIKit
var nome = "Dev ios"
print(nome)

```

## Constantes e comentários

```swift

import UIKit
var nome = "Dev ios"
nome = "Developer ios"

// Meu comentário de 1 linha
// Constante com o let não pode mudar o estado
let constante = "Dev ios"
/*
 Meu comentário de várias linhas
 Um bom exemplo de constante é o pi
 Dê preferência para o uso do let,
 mas quando precisar mudar o estado use o var.
 */
let pi = 3.14

print(nome)
print(constante)
print(pi)

```

## Tipos de dados

```swift

import UIKit

let int = 2022 // Int -> inteiros
let double = 8.1 // Double -> números decimais
let string = "Alan" // String -> textos
let isDeveloper = true // Bool -> true ou false

// Tipando as variáveis
let number: Int = 2021
let pi: Double = 3.14
let name: String = "Alan Alves"
let no: Bool = false

```

## Conversão de tipos de dados

```swift
import UIKit
let x = 10
let name = String(x)
print(name)

let y = "20"
let vinte = Int(y)
print(vinte)

```

## Operadores

```swift

import UIKit

// == , != , <, <= , > , >=
let result = 4 != 3

let x = 10
let y = 10

let res = x == y

let firstName = "Alan"
let lastName = "Alves"

print(result)
print(res)
print(firstName == lastName)

// ! && ||

let isDriver = false
let isStudent = true

print(!isDriver)

let ou = isDriver || isStudent
print("|| -> Pelo menos um tem que ser verdadeiro:", ou)

let e = isDriver && isStudent
print("&& -> Os dois tem que ser verdadeiros:", e)


```

## Condicionais e ternários

```swift

import UIKit

let isHungry = true
let isThirsty = true

if !isHungry {
    print("estou com fome")
} else if !isThirsty{
    print("estou com sede")
} else {
    print("estou satisfeito")
}

// Escopo

var product: String
let company = "Apple"
if company == "Google" {
    product = "Android"
} else {
    product = "iPhone"
}
print(product)

// operador ternário
// expressao ? valor-true : valor-false
var newProduct :String
newProduct = company == "Google" ? "Android" : "iPhone"
print(newProduct)

```

## Tuplas

```swift
import UIKit

let latitude: Double = 23.21
// let coords: (Double, Double) = (23.4, 54.22)
// print(coords.0)
// print(coords.1)

let coords = (lat: 23.4, lng: 54.22)

print(coords.0)
print(coords.1)

print("lat:", coords.lat)
print("lng:", coords.lng)

let camera = (x: 10, y: 20, z: 1)

// Caso queria ignorar algum eixo use o _
// let (x, y, _) = camera
let (x, y, z) = camera

print(x)
print(y)
print(z)

let user = (name: "Alan", age: 30)
print(user.name)
print(user.age)

```

## Arrays

```swift
import UIKit

var userNames: [String] = []

userNames.append("Alan")
print(userNames)

userNames.append("Carla")
print(userNames)

userNames += ["Pablo", "Rodrigo"]

print(userNames)

```

## Modificadores de Arrays

```swift
import UIKit

var userNames: [String] = []

userNames.append("Alan")
print(userNames)

userNames.append("Carla")
print(userNames)

userNames += ["Pablo", "Rodrigo", "Sara", "Rebeca", "Jessica"]

print(userNames)
print("Total de elementos no array:", userNames.count)
print("Carla está na lista?", userNames.contains("Carla"))

// acesso por indice
print(userNames[4])
print("Do zero ao 3:", userNames[0...3])

//
userNames.insert("Jorge", at: 4)
print("Jorge foi adicionado com sucesso no indice 4:", userNames)
print(userNames)

// Na ordem
userNames.sort()
print(userNames)

// Remover elemontos do array
userNames.removeLast()
print("Ultimo elemento foi removido do array:",userNames)

userNames.remove(at: 1)
print("Elemento 1 foi removido do array:",userNames)

userNames.removeAll()
print("Sem elementos no array:",userNames)
print("Sem elementos no array:",userNames.isEmpty)

// condicionais
if let first = userNames.first {
    print(first)
} else {
    print("A lista não contém elementos")
}

```

## While e repet

```swift
import UIKit

// while - primeiro checa e depois executa
var i = 1

while i <= 10 {
    print("i -", i)
    i += 1
}

// repet - primeiro executa e depois checa, é um do while em outras linguagens
var j = 1
repeat {
    print("j -", j)
    j += 1
} while (j <= 10)


```

## For

```swift
import UIKit

let range = 0...5 // inlcuseve
let newRange = 0..<5 // exlcuseve
range
newRange
var limit = 5
let rg = 0..<limit

// for
var sum = 0
let count = 10

for i in 1...count {
    sum += i
}
print(sum)

for _ in 1...count {
    print("oi")
}

for _ in 1...count where count > 50 {
    print("...")
}

// números pares
for i in 1 ... count where i % 2 == 0 {
    print("interpolação: \(i)")
}


```

## Interpolation of String and caracter unicode

```swift

import UIKit
// Interpolation of String and caracter unicode
let name: String = "Fulano Ciclano"
var age = 23
var isDrunk = false
var hasDocumeent = true

if age >= 18 && hasDocumeent && !isDrunk {
    print("\(name) pode digir \u{2665}")
} else {
    print("\(name) não pode dir  \u{264}")
}
// orther unicodes \u{1F469}

var new_index_before = name[name.index(before: name.endIndex)]
var new_index_after = name[name.index(after: name.startIndex)]
var new_offsetby = name[name.index(name.startIndex, offsetBy: 2)]

print(new_index_before)
print(new_index_after)
print(new_offsetby)
print(name.last)

// each line
for index in name.indices {
    print("\(name[index])")
}

// in line
for index in name.indices {
    print("\(name[index]) ", terminator: ""
    )
}

print("\n")
// var my_index = name.firstIndex(of: " ")!
var full_name = "Ciclano Beltrano de Fulano"

var last_index = full_name.lastIndex(of: " ")
print("\(full_name[..<last_index!])")

var words = full_name.split(separator: " ")
print("\(words[0])")


```
