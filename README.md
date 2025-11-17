# ♟️ Projeto: Sistema de Jogo de Xadrez em Java (Console)

## 🌟 Visão Geral

Este projeto é uma implementação completa de um sistema de jogo de xadrez, desenvolvido em **Java** e executado em ambiente de console. O objetivo principal foi aplicar e solidificar os conceitos de **Programação Orientada a Objetos (POO)**, focando em design de classes, herança, polimorfismo e tratamento de exceções.

O sistema simula a lógica completa do jogo, incluindo o movimento de todas as peças, regras especiais (como *en passant*, roque e promoção), e a detecção de xeque e xeque-mate.

## 🎯 Destaques Técnicos e Conceitos de POO

Este projeto é uma excelente demonstração da minha capacidade de modelar problemas complexos do mundo real utilizando princípios de POO:

*   **Modelagem de Domínio (POO):** O projeto foi estruturado em três camadas principais (`boardgame`, `chess` e `application`), garantindo a separação de responsabilidades e a reutilização de código.
    *   **Herança e Polimorfismo:** As diferentes peças de xadrez (`King`, `Rook`, `Bishop`, etc.) herdam da classe base `Piece`, e o polimorfismo é usado para implementar o comportamento de movimento específico de cada peça.
    *   **Encapsulamento:** O tabuleiro (`Board`) e as posições (`Position`) são encapsulados, garantindo que as regras do jogo sejam aplicadas de forma consistente e que o estado interno seja protegido.
*   **Lógica de Jogo Complexa:** Implementação de todas as regras do xadrez, incluindo:
    *   Cálculo de movimentos possíveis para cada peça.
    *   Validação de movimentos (impedindo movimentos que coloquem o próprio rei em xeque).
    *   Regras especiais: *Castling* (Roque), *En Passant* e *Promotion* (Promoção do peão).
    *   Detecção de **Xeque** e **Xeque-Mate**.
*   **Tratamento de Exceções:** Uso de exceções personalizadas (`BoardException`, `ChessException`) para lidar com erros de movimento ou de tabuleiro de forma controlada e amigável ao usuário.
*   **Interface de Usuário (Console):** Desenvolvimento de uma interface simples, mas funcional, no console, utilizando recursos como cores ANSI para melhor visualização do tabuleiro e das peças.

## 🛠️ Tecnologias Utilizadas

| Categoria | Tecnologia | Descrição |
| :--- | :--- | :--- |
| **Linguagem** | Java | Linguagem principal de desenvolvimento. |
| **Ambiente** | Console (Terminal) | Interface de usuário para interação com o jogo. |
| **Conceitos** | Programação Orientada a Objetos (POO) | Design de classes, Herança, Polimorfismo, Encapsulamento. |
| **Recursos** | Cores ANSI | Utilizadas para melhorar a visualização do tabuleiro no console. |

## ⚙️ Estrutura do Projeto

O projeto é organizado em pacotes que refletem a separação de conceitos:

```
.
├── src/
│   ├── application/      # Ponto de entrada e interface de usuário
│   ├── boardgame/        # Camada de lógica de tabuleiro genérica (reutilizável)
│   └── chess/            # Camada de regras específicas do xadrez
│       └── pieces/       # Implementação das peças de xadrez
└── ...
```

## 🚀 Como Executar o Projeto

### Pré-requisitos

*   Java Development Kit (JDK) instalado (versão 8 ou superior).

### Passos para Execução

1.  **Clone o Repositório:**
    ```bash
    git clone https://github.com/EduardoJuvenasso/chess-system-java.git
    cd chess-system-java
    ```
2.  **Compile e Execute:**
    *   Se estiver usando uma IDE (como Eclipse ou IntelliJ), execute a classe principal em `src/application/Program.java`.
    *   Se estiver usando o terminal (como Git Bash, que suporta cores ANSI), compile e execute o projeto.

### Interação

O jogo é totalmente interativo via console. O usuário deve inserir as coordenadas de origem e destino (ex: `a1` para `a3`) para mover as peças.

## 💡 Lições Aprendidas e Próximos Passos

A construção deste sistema de xadrez foi fundamental para aprofundar o entendimento de:

*   **Modelagem Abstrata:** A capacidade de criar uma camada genérica de tabuleiro (`boardgame`) que pode ser reutilizada para outros jogos, separada da lógica específica do xadrez (`chess`).
*   **Design Patterns Implícitos:** A aplicação de conceitos que se assemelham a padrões de projeto, como o *Strategy Pattern* (no comportamento de movimento das peças) e o *Factory Method* (na criação das peças).

**Melhorias Futuras:**

*   Implementar uma **Interface Gráfica (GUI)**, utilizando JavaFX ou Swing, para substituir a interface de console.
*   Adicionar um módulo de **Inteligência Artificial (IA)** para permitir que o usuário jogue contra o computador (ex: utilizando o algoritmo Minimax).
*   Implementar a funcionalidade de **Salvar/Carregar** o estado do jogo.

---

*Desenvolvido por Eduardo Juvenasso como parte de um curso acadêmico.*
