# Estruturas de repetição
Podemos chamar também de Loop, Laço ou método de iteração.

#### O que veremos aqui:
- for 
- while
- do... while
- for... of

## For

#### Estrutura:

for (expressaoInicial; condição; incremento) {
    código aqui;
  }

#### Exemplo:

for (let i = 0; i <= 10; i++) {}

- 1- Primeiro se diz onde inicia a repetição: essa variável (i) está começando do zero. Se cria uma variável pra saber de onde começa, o for a tem como referência pra saber quantas vezes repetiu. 
- 2- Depois vem a condição que define quantas vezes essa repetição vai acontecer. Essa condição do exemplo: enquanto o i for menor ou igual a 10.
- 3- A informação que o for precisa é o incremento. Ou seja: o ritmo que ele vai levar pra repetição. No exemplo, você quer que ele repita do zero até o dez, de 1 em 1. (Se fosse de dois em dois seria: i = i + 2, que ai seria o passo a cada dois.)


```jsx
for(let i = 0; i < 10; i = i+2){ 
    console.log(`número ${i}`)
}
```
- No console irá mostrar: 0, 2, 4, 6, 8. 
- Você disse que sua variável (nesse caso, a variável é i) começa do 0, que quer que o código se repita enquanto essa variável for menor do que 10, e quer que vá contando de 2 em 2, dando passo de 2 em 2. E, no console, pediu para mostrar i, ou seja, todos os números que contaram depois da repetição do código.
- Então ele começou no 0 e mostrou. Andou 2 (que foi o incremento que botamos, passo de 2 em 2), chegou no 2 e mostrou, andou mais 2, foi no 4 e mostrou, andou mais 2, foi no 6 e mostrou, andou mais 2, foi no 8 e mostrou. E aí o código parou de repetir, porque a condição foi atingida. Se quiséssemos que o 10 entrasse na lista, teríamos que colocar <=10. 

#### Fazendo operações com a variável dentro do for:
```jsx
for (let i = 0; i <= 10; i++) {
     let soma = i + i 
     console.log(`a soma de ${i} com ${i} é ${soma}`)} 
 

```
Nesse exemplo, o que aconteceu:
- Botamos novamente que nossa variável, i, começa do 0. Que queremos que o código se repita enquanto essa variável for menor ou igual a 10, e que queremos passinho de 1 em 1. 
- E aí, no escopo do for, dissemos: queremos que a cada atualização dos números, eles sejam somados com eles mesmos. Ou seja: o for passa no 0, soma o 0 com ele mesmo. Depois passa no 1, e soma o 1 com ele mesmo. Depois passa no 2, e soma o 2 com ele mesmo... e por aí vai. Está passando em cada um, até 10, porque o incremento que colocamos foi esse passinho de um em um, diferente do exemplo anterior que foi i = i + 2 (ou seja, passinho de 2 em 2).

### For em arrays
```jsx
const numeros = [3, 2, 4, 3, 5, 1, 3, 4, 2, 5, 7, 1, 3] 
 for (let i = 0; i < numeros.length; i++) {
     const dobro = numeros[i] * 2
   console.log(`o dobro de ${numeros[i]} é ${dobro}`) }
```
- Nesse caso, como é uma array, não estamos começando do número 0, e sim do elemento 0, que é o 3. 
- Nossa condição é: enquanto i for menor que o número de elementos dessa array. 
Colocamos " i < numeros.length " porque a forma que o for percorre a array, é contando começando pelo elemento 0 (que nesse caso, é o 3), então em tese, ela fica 1 numero menor. O ".length" conta tudo, se colocar <= é como se o for tivesse passando por uma coisa que não existe, por isso tem que ser menor. 
- Dando passinho de 1 em 1. 
- E, no escopo do for, dissemos: a cada vez que o for passar pelos elementos dessa array, quero que os numeros sejam multiplicados por 2. Então ele passa no primeiro elemento e o multiplica pro 2, vai pro segundo elemento, multiplica por 2 e por aí vai...

```jsx

 let outrosNumeros = [5, 3, 5, 6]

for (i = 0; i < outrosNumeros.length; i++){

    const dobro = outrosNumeros[i] * 2
    console.log(dobro)
} 

/*
se nesse exemplo, ao invés de "outrosNumeros[i] *2", botassemos só [i]*2, você pediria o dobro dos index. ou seja: tem 4 elementos nessa array, mas contando por index, ficaria 3. e aí faria o dobro disso (de 0, 1, 2, 3).
por isso tem que botar o nome da array e [i], o nome da array dá todos os elementos que irá pegar pra fazer a conta, e i é o ponto de partida.
*/
```
```jsx
/*Crie um algoritmo usando o for que leia uma lista. 
Mostre no console apenas os números pares.
 Esta lista deve ser assim: [1, 2, 3, 4, 5, 6, 7, 8, 9];
*/
let numeros = [1, 2, 3, 4, 5, 6, 7, 8, 9]

for(let i = 0; i < numeros.length; i++){

    if(numeros[i]%2== 0){
        console.log(numeros[i])
    }
}

```

## While
Estrutura:
 while (condição) {
    código aqui;
    incremento
  }
```jsx
let i = 0; // sempre criamos a variável fora
  while(i <=3) {
    console.log(`número ${i}`)
    i++
  }
```
   O que está dizendo no exemplo:
- Enquanto o i for menor ou igual a 3, vai mostrar todos os números no console, dando passinho de 1 em 1. Então vai mostrar: 0, 1, 2, 3
- A partir disso, não roda mais, porque a condição foi atendida.
- É importante não esquecer do incremento pra não rodar em loop infinito. Se você não passa o incremento, a variável permanece no lugar que você declara (nesse caso, o 0)

```jsx

    //Faça um programa que imprima na tela apenas os números ímpares entre 1 e 50.

    let f = 1

    while(f<=50){

     
        if(f % 2 !==0)
        console.log(f)
        f++

}
```

### Exemplo em uma array


  ```jsx
const numeros = [2, 3, 6, 8, 9]
let n = 0;
  
  while(n<numeros.length){
      const dobro = numeros[n] * 2
      console.log(dobro)
      n++
  }
 ```
  O que está dizendo no exemplo:

  - O n está começando no ELEMENTO ZERO (porque se trata de uma array), que nesse caso, é o 2. Ele não está, como no exemplo anterior, partindo do número zero.
  - Então: enquanto n for menor do que o número de elementos dessa array, o que acontece é:
  - Esses números multiplicam por 2, passando em um por um (n++). 
  - Se não tivesse o n++, rodaria eternamente  4, porque começou no indice 0. O n++ percorre tudo.



## Do...while
O do...while também repete até que a condição seja falsa.
Mas, diferente do while, ele executa o código pelo menos 1 vez, porque primeiro vem o do (faça).
Depois de executar 1 vez, ele confere a condição e vê se continua ou não. 

- Estrutura: 
  do {
    código aqui;
  } while (condição);

```jsx

let contador = 0; // variaveis declaradas fora também

  do{
    
      console.log(`contando...${contador}`)
      contador++  
  
  } while(contador < 10)

```
Aqui está dizendo: 
- Nossa variável (contador) começa do numero 0
- Enquanto for menor do que 10, quero que mostre no console todos os números, dando passinho de 1 em 1.
- Como é no do...while, primeiro ela já faz sem verificar, depois verifica e continua fazendo se a condição ainda for verdadeira, e para quando for falsa.

```jsx

let total = 0
let contador = 0

do {
    total += contador * 100
    console.log(`contador: ${contador}`)
    console.log('total: ' + total)
    contador++
} while(contador < 10)
```
Explicando:

- Esse += (atribuindo alguma coisa MAIS o valor que ele já tem.). No caso, seria: valor do total mais o valor de contador*100 a cada volta, até a condição ser falsa.
- Total e contador começam no 0. 
- Quando acrescenta 1, fica contador 1 e total 100, pois 100x1 = 100.
- Quando vai pro 2, fica 2*100 que é 200, mas ja tem os 100 de antes no total, então o total passa a ser 300.
- Quando vai pro 3, fica 300 do resultado(100*3) mais 300 do valor do total, então o total é 600. No 4, fica 400 (4 * 100) +600... e por aí vai!


## For...of
Ele vai muito bem em arrays. Ele já sabe que é pra começar no primeiro elemento dela (0),
e que é pra percorrer ela inteira, por isso não precisa do incremento (diferente do for, while etc)

- Estrutura:

for (variavel of iteravel) {
    declaração
  }
```jsx
let times = ['Vasco', 'Barcelona', 'PSG', 'Palmeiras']

for (let time of times){
    console.log(time)
} 
```
Explicando:
- Criamos uma variável na estrutura, que é como se disséssemos: para cada TIME, da array TIMES, me mostre no console time (ou seja, cada time daquela array).

```jsx
//em uma string
let palavra = 'morango'
for (let letras of palavra){
    console.log(letras)
}
```
Explicando:
- Criamos uma variável "letras", como se disséssemos: para cada letra da palavra (me mostre cada letra da palavra). 

```jsx
let numeros = [3, 5, 6, 7]

for (let numero of numeros){
    console.log(numero * 2)
}
```
Explicando:
- Aqui, estamos dizendo: para cada número da ARRAY numeros, vai me mostrar no console numero * 2. E como o for... of sabe que é pra percorrer a array inteira, irá mostrar tudo.

# Materiais de reforço (teoria e exercícios para praticar):
#### For
- https://www.youtube.com/watch?v=dPl3OTOOJwM

#### While e do...while
- https://www.devmedia.com.br/javascript-while-e-do-while/41015

#### For...of
- https://www.devmedia.com.br/javascript-for-for-in-for-of/41018#2 
- https://www.youtube.com/watch?v=HFG_p4K2MAc 
