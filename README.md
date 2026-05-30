# Avalia-o-P2
Avaliação P2 - Dupla Edgar de Souza Pereira & Vitor Nunes Santos.
Avaliação, siga as instruções.
 
Descrição: No software de uma máquina de café com 6 sabores utilizou-se POO com JAVA para acessar o menu e posteriormente fazer os controles para funcionar uma simulação. Dentro dessa aplicação foi utilizado uma classe abstrata Drink e uma concreta Cafe, e para executar a classe principal. Dentro desse programa explique como foi aplicado os três paradigmas da Programação Orientada a Objetos e como seria o uso do polimorfismo (Uma classe que tem característica de duas ou mais classes concretas)?
R: Aplicação dos Paradigmas da Programação Orientada a Objetos (POO)

No desenvolvimento do software da máquina de café foram utilizados os principais conceitos da Programação Orientada a Objetos: Encapsulamento, Herança e Abstração.

1. Encapsulamento

O encapsulamento foi aplicado na classe abstrata Drink.

//private String sabor;
//private double valor;

Os atributos foram declarados como private, impedindo o acesso direto por outras classes. O acesso ocorre por meio dos métodos getters e setters:

//public void setValor(double valor)
//public double getValor()

Dessa forma, os dados ficam protegidos e são manipulados de forma controlada.


2. Herança

A herança ocorre quando a classe Cafe herda as características da classe Drink.

public class Cafe extends Drink

Com isso, a classe Cafe recebe automaticamente os atributos e métodos da classe Drink, como:

* sabor
* valor
* getSabor()
* setSabor()
* getValor()
* setValor()

Isso evita repetição de código e facilita a manutenção do sistema.


3. Abstração

A abstração foi utilizada através da classe:

//public abstract class Drink

A classe Drink representa uma bebida de forma genérica, armazenando apenas as características comuns a qualquer bebida, como sabor e valor.

Ela não é criada diretamente no programa. Em vez disso, serve como base para classes mais específicas, como Cafe, que implementam comportamentos concretos da aplicação.


4. Como seria aplicado o Polimorfismo

No código atual o polimorfismo ainda não foi implementado de forma completa, pois existe apenas uma classe concreta (Cafe).

O polimorfismo ocorreria quando várias classes diferentes herdassem de Drink e fossem tratadas como um mesmo tipo.

Exemplo:

//public class Cafe extends Drink { ... }
//public class Cha extends Drink { ... }
//public class Chocolate extends Drink { ... }

Na classe principal:

//Drink bebida;
//bebida = new Cafe("Tradicional", 1.30);
//bebida = new Cha("Camomila", 2.00);
//bebida = new Chocolate("Quente", 3.50);

Nesse caso, a variável bebida possui o tipo Drink, mas pode armazenar objetos de diferentes classes concretas.

Cada bebida poderia ter um método próprio:

//public void preparar()

E o Java executaria automaticamente a versão correta conforme o objeto criado.

Por exemplo:

//bebida.preparar();

Se o objeto for Cafe, será preparado café. Se for Cha, será preparado chá. Esse comportamento caracteriza o polimorfismo, pois um mesmo comando produz ações diferentes dependendo do objeto utilizado.
