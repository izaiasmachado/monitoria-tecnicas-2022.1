# Encontro 02
## Exemplo de HashMap

```java
package pratica;

import java.util.HashMap;
import java.util.Map;

public class Principal {
    public static void main(String args[]) {
        String listaDeCompras[] = { "Cenoura", "Maçã", "Maçã", "Cenoura", "Laranja", "Acerola", "Pera", "Laranja", "Acerola" };
        Map<String,Integer> mapa = new HashMap<String,Integer>();
        
        for (String item : listaDeCompras) {
            Integer aparicoes = mapa.get(item);

            if (aparicoes == null) {
                aparicoes = 0;
            }
            
            mapa.put(item, aparicoes + 1);
        }

        for (String chave : mapa.keySet()) {
            Integer aparicoes = mapa.get(chave);
            System.out.println(chave + " (x" + aparicoes + ")");
        }
    } 
}
```

## Exercícios Propostos
**Exercício 01**

Defina uma classe Veiculo com os atributos nome, número de rodas, capacidade do tanque de combustível (em litros) e consumo (Km por litro). Além disso, defina um método abastecer, que recebe a quantidade de combustível para encher o tanque; e um método para exibir a autonomia do veículo, ou seja, deve imprimir no console (System.out.println()) a distância que o veículo é capaz de rodar com o combustível existente no tanque.

Por fim, defina uma classe Exercicio01, com método "main()", que instancie 2 veículos, com atributos de capacidade do tanque e consumo diferentes entre si, abasteça os veículos e, em seguida, exiba no console a autonomia de cada um.

**Resolução**
```java
```

## Referências:

[Exercícios sobre Orientação a Objetos](https://github.com/ipuma-rd-com-br/ExerciciosOO)
