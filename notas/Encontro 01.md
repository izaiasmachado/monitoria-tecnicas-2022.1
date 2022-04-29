# Encontro 01

## Conteúdo
Abaixo temos dois exemplos para atribuir valor a uma variável baseado em uma condição.

O primeiro é utilizando uma estrutura condicional comum.

```java
String mensagem;

if (valor == 0) {
    mensagem = "Numero é nulo!";
} else {
    mensagem = "Número não é nulo!";
}

System.out.println(mensagem);
```
Já essa segunda forma utiliza o operador ternário. Ou seja, se a condição for verdadeira a mensagem recebe o primeiro valor, caso contrário recebe o segundo.

```java
String mensagem = (valor == 0) ? "Numero é nulo!" : "Número não é nulo!";
System.out.println(mensagem);
```

Se você ainda tem dúvidas, recomendo que leia o [Artigo sobre Operador Ternário](https://www.devmedia.com.br/java-if-else-e-o-operador-ternario/38185).


## Exercícios Propostos
**Exercício 01**
Crie uma função utilizando recursão que imprima todos entre um parâmetro de entrada e outro.

```java
    public static int imprimirOrdem (int i, int n) {
        System.out.println(i);
        
        if (i < n) {
            return imprimirOrdem(i + 1, n);
        }
        
        return i;
    }
```

**Exercício 02**

Modele e implemente um método recursivo que calcule o n-ésimo número da sequência de fibonacci.

**Resolução**
```java
    public static int fib (int n) {
        if (n == 0) return 0;
        if (n == 1) return 1;
        
        return fib(n - 1) + fib(n - 2);
    }
```  

**Exercício 03**

Modele e implemente um método recursivo que calcule o somatório dos números inteiros entre os números k e j, passados como parâmetro.

**Resolução**
```java
    public static int somatorio(int k, int j) {        
        if (k == j) {
            return j;
        }
        
        return k + somatorio(k + 1, j);
    }
```

**Exercício 04**
Modele e implemente um método recursivo que calcule o fatorial de um número inteiro natural qualquer.

```java
    public static int fatorial (int n) {
        if (n == 0 || n == 1) {
            return 1;
        }
        
        return n * fatorial(n - 1);
    }
```

**Exercício 05**

Modele e implemente um método recursivo que recebe um vetor, a posição inicial e um número e retorne um valor booleano para se o número está contido ou não no vetor.

**Resolução**
```java
    public static boolean pesquisa(int v[], int i, int n) {
        if (v[i] == n) return true;
        if (i == (v.length - 1)) return false;
        
        return pesquisa(v, i + 1,  n);
    }
```

**Exercício 06**

Crie uma classe para um Ponto e um método para dizer em qual quadrante ele se encontra.

Para casa: Crie uma classe Triângulo utilizando a classe Ponto e em seu construtor dispare uma exceção caso o triângulo não seja possível.

**Resolução**

**No arquivo Principal.java**
```java
package com.mycompany.projetoteste;

public class Principal {
    public static void main(String[] args) {
        Ponto p = new Ponto(1, 1);       
        System.out.println(p.quadrante());
    }
}
```

**No arquivo Ponto.java**
```java
public class Ponto {
    int x;
    int y;
    
    public Ponto(int x, int y) {
        this.x = x;
        this.y = y;
    }
    
    
    public int quadrante() {
        if (this.x > 0 && this.y > 0) return 1;
        if (this.x < 0 && this.y > 0) return 2;
        if (this.x < 0 && this.y < 0) return 3;
        if (this.x > 0 && this.y < 0) return 4;
        return -1;
    }
}

```


## Referências:

[Exercícios sobre Recursão](https://github.com/PUCRS-Poli-ES-ALAV/2-mais-exercicios-de-recursao)

[Exercícios sobre Orientação a Objetos](https://github.com/ipuma-rd-com-br/ExerciciosOO)