![banner](https://i.postimg.cc/kgqnr1Z1/banner-desafio2-vnw.png)

Desafio da escola [Vai na Web](https://www.linkedin.com/company/vainaweb/): Criar uma biblioteca (lib) em Java sem instanciar objetos, utilizando apenas a classe para realizar operações matemáticas diversas. O objetivo é empacotar o código realizado em um arquivo JAR para facilitar a reutilização.

## 📚 Sobre a Biblioteca

A biblioteca `CalculationUtils` oferece uma variedade de operações matemáticas básicas e avançadas em Java. Ela foi projetada para ser fácil de usar, permitindo que os usuários realizem cálculos sem a necessidade de instanciar objetos.

## 🔎 Desafios Encontrados

- Permitir que o usuário some, subtraia, multiplique e divida quantos números desejar.

  - Para lidar com a necessidade de permitir que o usuário realize operações com quantos números desejar, busquei pelas melhores práticas em Java. Com conhecimento prévio em JavaScript, pesquisei pela existência do recurso de parâmetros rest, que permite representar um número indefinido de argumentos como um array no parametro, no Java. Pesquisando, encontrei a solução utilizando parâmetros varargs (variadic arguments). Os parâmetros varargs também são usados para definir um parâmetro que pode receber um número indefinido de argumentos. Com o uso de um loop `for` e `for-each`, consegui iterar sobre os argumentos e realizar as operações desejadas.

    ```Java
      // Exemplo de uso:
      double soma = Calculadora.somar(1, 2, 3, 4, 5);
      System.out.println(soma); // Saída: 15
    ```

- Trazer um pouco mais de carinho e personalização para a biblioteca ao considerar erros simples e comuns ao fazer o cálculo de alguns métodos, como passar apenas um argumento para a divisão ou tentar dividir por zero.

  -  Para tornar a biblioteca mais amigável e evitar erros comuns, implementei verificações e mensagens descritivas de erro. Utilizei estruturas condicionais para identificar situações como passar apenas um argumento para a divisão (que requer no mínimo dois números) e tentar dividir por zero (que é indefinido). Além disso, lancei exceções com mensagens informativas para indicar claramente quando ocorre um erro.

      ```Java
        // Exemplo de uso:
        try {
          double divisao = Calculadora.dividir(10, 0, 2);
          System.out.println(divisao);
        } catch (IllegalArgumentException e | ArithmeticException e) {
          System.err.println("Erro: " + e.getMessage()); // Saída: Erro: Não é possível dividir por zero.
        }
      ```

## ⚙️ Funcionalidades Principais

A biblioteca inclui as seguintes funcionalidades:

### ➗ Operações Aritméticas Básicas

- Soma
- Subtração
- Multiplicação
- Divisão

## 🛠️ Tecnologias

| Tecnologia  | Versão |
| ------------- | ------- |
| [Java SE](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html) | JDK 17.0.9 |

## 🧑‍🏫 Instrutor e Facilitador

<table>
  <tr>
    <td align="center"><a href="https://www.linkedin.com/in/samuel-silveriom/"><img style="border-radius: 50%;" src="https://avatars.githubusercontent.com/u/103957897?v=4" width="100px;" alt=""/><br /><sub><b>Samuel Silvério</b></sub></a><br /><a href="https://github.com/Samuel-prata" title="Samuel Silvério">🧑‍🏫</a></td>
    <td align="center"><a href="https://www.linkedin.com/in/leno-rafael-85a2ab1ba/"><img style="border-radius: 50%;" src="https://avatars.githubusercontent.com/u/73203800?v=4" width="100px;" alt=""/><br /><sub><b>Leno Rafael</b></sub></a><br /><a href="https://github.com/lenors" title="Leno Rafael">🧑‍🏫</a></td>
  </tr>
</table>

## 👩‍💻 Autora

<table>
  <tr>
    <td align="center">
      <a href="https://www.linkedin.com/in/alinemelofrontend">
        <img style="border-radius: 50%;" src="https://avatars.githubusercontent.com/u/109696840?v=4" width="100px;" alt="" />
        <br />
        <sub><b>Aline Melo</b></sub>
      </a>
      <br />
      <a href="https://www.linkedin.com/in/alinemelofrontend" title="Aline Melo"></a>
    </td>
  </tr>
</table>

Esse projeto esta sob a licença [MIT](https://github.com/alinemello29/CalculoSoma/blob/main/LICENCE).
