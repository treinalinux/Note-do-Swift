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

