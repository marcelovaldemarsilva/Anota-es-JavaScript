# Anota-es-JavaScript
Principais Anotações de JS


minhas anotações ate agora: 
Comandos em JS:

<script>	window.alert       // este comando emite uma mensagem!
window.confirm                  // este comando faz uma pergunta de confirmação
window.prompt                  // este comando faz um pergunta de resposta!')
</script>
________________________________________________________________________

Variáveis:

Como Criar variáveis, Ex: var nome ou let nome

para uma variável receber um valor usamos:
 var nome = Gustavo       // desta forma criamos uma variável e ao mesmo tempo demos uma valor a ela

nome = Gustavo             //desta forma apenas demos um valor para a variável  que ja foi criada

Regras das variáveis:
Podem começar com: Letra, $ ou _
Não podem começar com números 
É possível usar letras ou números
É possível usar  acentos e símbolos 
Não pode conter espaços 
Não pode usar palavras que são comandos

Dicas para nomes das variáveis: 
Maiúsculas e Minúsculas fazem a diferença!
Tente escolher nomes coerentes a função da variável. Ex: Variável que vai armazenar a idade, coloca o nome dela de “idade”
Evite se tornar um “Programador Alfabeto” ou um “Programador Numérico”. Ex: Não usar os nomes das variáveis como “a”, “b”, “c”, etc; ou “a1”, “a2”, “a3”, etc.

Tipos de Dados das Variáveis: (Tipos Primitivos, lembrando que existem muitas outras!)

Numbers;
Strings;
Boolean;

// Numbers: 1; -2; 4.5; 6.555 -> Basicamente números
// Strings: Maria, Google, Joao, pedreiro, (seu CPF) -> Basicamente cadeia de caracteres
// Boolean: True; False

________________________________________________________________________

Transformando uma string em um number

var n1 = Number.parseInt (window.prompt ('digite aqui um numero!'))
var numero1 = Number.parseFloat (window.prompt ('digite aqui um numero!'))
var numero1 = Number (window.prompt ('digite aqui um numero!’))

Mas qual é a diferença entra “Number.parseInt”, “Number.parseFloat” e Number?

// Number.parseInt: Numero Inteiro
// Number.parseFloat: Numero com virgula
// Number: Js vai decidir qual é

________________________________________________________________________

Transformando um number em uma string

window.alert ('a soma dos numeros é: ' + soma.toString())  // Jeito mais antigo
ou
window.alert ('a soma dos numeros é: ' + String(soma))      // Jeito mais simples
________________________________________________________________________

Formatando Strings:

var teste = 'java script’

‘eu estou aprendendo’ + teste
`eu estou aprendendo ${teste}` -> não esqueça de usar crase!
teste.length                   // conta quantos caracteres tem na variável  
teste.toUpperCase        // coloca tudo em caixa alta
teste.toLowerCase        // coloca tudo em minúsculo 

________________________________________________________________________

Formatando números:

Var n1 = 1543.5

n1.toFixed(2)                                                                              // Coloca em duas casas decimais (para colocar em mais ou menos casas troque o numero entre parênteses)
n1.toLocaleString( ‘pt-BR’,{style: ‘currecy’, currency: ‘BRL’} )    // Coloca o R$ na frente do numero (pode trocar entre outras                                                                                                                 moedas)
n1.replace (‘.’, ‘,’)                                                                       // Troca o ponto pela virgula

________________________________________________________________________


Operadores:

Tipos de operadores que vamos estudar:

Aritméticos
Atribuição
relacionais
lógicos
ternarios

________________________________________________________________________


Operadores Aritméticos:
 +     // Somar   
  -    // Subtrair
  *    // Multiplicação 
  /    // divisão
 %   // Resto de uma divisão 
 **   // Potencia do primeiro numero elevado ao segundo

5 + 3   = 8
5 - 3    = 2
5 * 3    = 15
5 / 3    = 1,6
5 % 3  =  2
5 ** 3   = 125

Precedencia dos operadores↓

 ( ) 
 **
 /   *   %
 +  -

Auto Atribuições:                                                                               Forma Simplificada:

var  n = 3                                                                                                var n = 3

n = n + 4    // ele vai somar ele mesmo a 4                                  |     n   +=  4 
n = n - 5    //ele vai pegar ele mesmo e subtrair 5                        |     n   -=  2
n = n  * 4   //ele vai pegar ele mesmo e multiplicar por 4              |    n   *=  5
n = n  / 2   //ele vai pegar ele mesmo e dividir por 2                     |    n   /=  2
n = n ** 2  //ele vai pegar ele mesmo e elevar a 2 potência           |    n  **= 2
n = n %  5 //ele vai pegar ele mesmo, dividir por 5 e dar o resto  |    n  %= 5

outra simplificação:

n++     // é a mesma coisa que n = n + 1 ou n += 1
n—     //é a mesma coisa que n = n - 1 ou n -= 1
++n    // ele vai somar antes
—n    // ele vai diminuir antes

Meu script desta aula:
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Programação</title>
    <style>

body{ background-color: black;
color:rgb(98, 192, 255);
font: normal 20pt arial ;
}

h1{color: rgb(97, 29, 255);
font:25pt arial }

    </style>

</head>
<body>

    <h1><strong>Programação do Gustavo:</strong></h1>

<script>

var nome = window.prompt ('Qual é o seu nome?')
var n1 = Number (window.prompt ('qual é o seu número favorito?'))
var n2 = Number (window.prompt (`agora fale um outro número!`))
var n3 = n1 / n2
var n4 = n2 / n1

document.write (`Olá, ${nome}! Seu nome tem ${nome.length} letras <br/>`)
document.write (`Seu nome em letras maiusculas é "${nome.toUpperCase()}" <br/>`)
document.write (`Seu nome em letras minusculas é "${nome.toLowerCase()}" <br/>`)

document.write (`<br/>`)

document.write (`Operações com o número ${n1}! <br/>`)
document.write (`<br/>`)

document.write (`Seu número favorito somado a ele mesmo é ${n1 + n1}! <br/>`)
document.write (`Seu número favorito vezes ele mesmo é ${n1 * n1}! <br/>`)
document.write (`Seu número favorito elevado a ele mesmo é ${n1 ** n1}! <br/>`)

document.write (`<br/>`)

document.write (`Operações com o número ${n2}! <br/>`)
document.write (`<br/>`)

document.write (`Seu outro número somado a ele mesmo é ${n2 + n2}! <br/>`)
document.write (`Seu outro número vezes ele mesmo é ${n2 * n2}! <br/>`)
document.write (`Seu outro número elevado a ele mesmo é ${n2 ** n2}! <br/>`)

document.write (`<br/>`)

document.write (`Operações com os números ${n1} e ${n2}! <br/>`)
document.write (`<br/>`)

document.write (`Seu número favorito  mais o outro número que você digitou antes é ${n1 + n2} <br/>`)
document.write (`Seu número favortio menos o outro número é ${n1 - n2} <br/>`)
document.write (`Seu outro número menos o seu número favorito é ${n2 - n1} <br/>`)
document.write (`Seu número favorito vezes o outro número é ${n1 * n2} <br/>`)
document.write (`Seu outro número vezes o seu número favorito é ${n2 * n1} <br/>`)
document.write (`Seu número favorito dividido pelo seu outro número é ${n3.toFixed(2)} <br/>`)
document.write (`Seu número outro número dividido pelo seu número favorito é ${n4.toFixed(2)} <br/>`)
document.write (`Seu número favorito elevado ao seu outro número é ${n1 ** n2} <br/>`)
document.write (`Seu outro número elevado ao seu número favorito é ${n2 ** n1} <br/>`)

</script>

</body>
</html>
