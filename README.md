# Smalltalk

## Hello World:

- Transcript show: 'Hello World'.

---
## Comandos para manipulação do Transcript:

- Transcript clear.
- Transcript cr.
- Transcript space.
- Transcript tab.
---

## Declaração de Variável:

- |variavel|
- variavel:= valor desejado .
- variavel:= #('x' 2 z) .
---

## Condicional:

ifTrue e ifFalse:

- comparação ifTrue: [ Ação se a comparação for verdadeira ] .
- comparação ifFalse: [ Ação se a comparação for falsa ] .

---

## Laços de repetição:

whileTrue, whileFalse, timesRepeat, to do, to by do e array do:

- whileTrue --> [ comparação ] whileTrue: [ Iteração se a comparação for verdadeira ] .
  * EX: |x|. x:= 3. [x>0] whileTrue: [Transcript cr show: x. x:= x-1.].
- whileFalse --> [ comparação ] whileFalse: [ Iteração se a comparação for falsa ] .
  * EX: |x|. x:= 3. [x<0] whileFalse: [Transcript cr show: x. x:= x-1.].
- timesRepeat --> numero de vezes a repetir timesRepeat: [ Ação ] .
  * EX: 10 timesRepeat: [ Transcript show: 'Exemplo'; cr. ] .
- to do --> numero para começar a repetição to: ultimo numero da repetição do: [:numero da vez| Iteração] .
  * EX: 0 to: 10 do: [:i| Transcript show: i; cr.] .
- to by do --> numero para começar a repetição to: ultimo numero da repetição do: quantidade de passo da repetição [:numero da vez| Iteração] .
  * EX: 0 to: 10 by: 2 do: [:i| Transcript show: i; cr].
- array do --> array do: [:variavel do array da vez| ação].
  * EX: #(0 1 2 3) do: [:a| Transcript show: a; cr.].
  
---

 ## Janelas de diálogo
 
 Janelas de confirmação e requesição:
 
 - Janelas de confirmação: self inform: 'Mensagem'.
 - Janelas de requesição: variavel:= FillInTheBlank request: 'Mensagem'.
 
 ---
 ## Blocos
 - Os blocos são objetos e podem ser atribuídos a uma variável.
 - Eles são usados extensivamente nas estruturas condicionais e de repetição, em operações sobre coleções controle de exceções, na      criação e controle de processos e também no mecanismo de tratamento de erros.
 - Blocos são parecidos com funções.
 - Blocos são instancias da classe BlockClosur e que é subclass de Object.
 - Para executar o conteúdo de um bloco precisamos explicitamente
enviar uma mensagem.
    * Estrutura
      |bloco|
      "o resultado deste exemplo sera o valor da ultima expressão: 22"
       bloco := [ :x :y |
           x + y.
           ].
       bloco value: 2 value: 2.
