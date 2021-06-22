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


