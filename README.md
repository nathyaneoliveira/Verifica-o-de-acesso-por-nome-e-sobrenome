# 🛡 Verificação de Acesso por Nome e Sobrenome em Java

## Descrição
Este projeto implementa um programa em **Java** que realiza **verificação de acesso** com base no nome e sobrenome do usuário.  
Dependendo do nome ou sobrenome informado, o programa retorna mensagens específicas:  

- **Acesso liberado** para sobrenomes autorizados (ex.: Wayne);  
- **Avisos de rejeição** para outros nomes ou sobrenomes (ex.: Kent, nomes não autorizados);  
- Mensagem especial para certos nomes (ex.: Diana).  

---

## Funcionalidades

- Solicita ao usuário **nome** e **sobrenome**;  
- Verifica combinações específicas de nomes/sobrenomes;  
- Exibe mensagens personalizadas de acordo com a entrada;  
- Diferencia maiúsculas e minúsculas automaticamente (`equalsIgnoreCase`).

---

## Código Principal

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Digite seu nome: ");
        String nome = scanner.nextLine();

        System.out.print("Digite seu sobrenome: ");
        String sobrenome = scanner.nextLine();

        if (sobrenome.equalsIgnoreCase("Wayne")) {
            System.out.println("Acesso liberado, Sr. Wayne");
        } else if (sobrenome.equalsIgnoreCase("Kent")) {
            System.out.println("Saí daí, mané!");
        } else if (nome.equalsIgnoreCase("Diana")) {
            System.out.println("Bem-vinda, Princesa de Themyscara");
        } else {
            System.out.println("Cai fora!");
        }

        scanner.close();
    }

}
````

---

## Requisitos

* Java JDK 11 ou superior;
* IDE ou editor de texto (IntelliJ, Eclipse, VS Code, etc.);
* Conhecimentos básicos de terminal ou console para execução.

---

## Execução

1. Abra o terminal ou console;
2. Navegue até a pasta do arquivo `Main.java`;
3. Compile o programa:

```bash
javac Main.java
```

4. Execute o programa:

```bash
java Main
```

5. Insira seu **nome** e **sobrenome** quando solicitado.

---

## Exemplo de Uso

```text
Digite seu nome: Bruce
Digite seu sobrenome: Wayne
Acesso liberado, Sr. Wayne
```

```text
Digite seu nome: Clark
Digite seu sobrenome: Kent
Saí daí, mané!
```

```text
Digite seu nome: Diana
Digite seu sobrenome: Prince
Bem-vinda, Princesa de Themyscara
```

```text
Digite seu nome: Arthur
Digite seu sobrenome: Curry
Cai fora!
```

---

## Contribuição

Este projeto pode ser expandido com:

* Suporte a múltiplos usuários autorizados;
* Cadastro de nomes e sobrenomes em **arquivo externo**;
* Mensagens personalizadas adicionais;
* Interface gráfica simples com Swing ou JavaFX;
* Sistema de autenticação completo com login e senha.

---

## Licença

Uso acadêmico.
