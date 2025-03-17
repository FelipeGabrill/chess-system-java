# Sistema de Jogo de Xadrez

## Objetivo geral

Este projeto proporciona uma experiência completa no desenvolvimento de um sistema de jogo de xadrez utilizando conceitos avançados de POO, estrutura de dados e boas práticas de programação em Java.

## Configuração Inicial do Projeto e Git

# Desenvolvimento do Projeto

## 1. Primeira Classe: Position
### Checklist:
- Criar a classe `Position` [public].

### Conceitos de POO abordados:
- Encapsulamento
- Construtores
- Sobrescrita do método `toString()`

---

## 2. Implementação de Tabuleiro e Peça
### Checklist:
- Criar as classes `Piece` e `Board` [public].

### Conceitos de POO abordados:
- Associações
- Modificadores de acesso / Encapsulamento

### Estruturas de dados abordadas:
- Matriz

---

## 3. Camada de Xadrez e Impressão do Tabuleiro
### Checklist:
- Criar os seguintes métodos e classes:
  - `Board.Piece(row, column)` e `Board.Piece(position)`
  - `Enum Chess.Color`
  - Classes `Chess.ChessPiece`, `Chess.ChessMatch`, `ChessConsole.UI`

### Conceitos de POO abordados:
- Enumerações
- Encapsulamento / Modificadores de acesso
- Herança
- Downcasting
- Membros estáticos
- Padrão de camadas

### Estruturas de dados abordadas:
- Matriz

---

## 4. Posicionando Peças no Tabuleiro
### Checklist:
- Criar o método `Board.PlacePiece(piece, position)`.
- Criar as classes `Rook` e `King` [public].
- Criar o método `ChessMatch.InitialSetup`.

### Conceitos de POO abordados:
- Herança
- Sobrescrita
- Polimorfismo (`toString()`)

---

## 5. Exceções e Programação Defensiva
### Checklist:
- Criar a classe `BoardException` [public].
- Criar os métodos `Board.PositionExists` e `Board.ThereIsAPiece`.
- Implementar programação defensiva nos métodos da classe `Board`.

### Conceitos de POO abordados:
- Exceções
- Construtores com mensagem obrigatória

---

## 6. Exceções e Posições de Xadrez
### Checklist:
- Criar as classes `ChessException` e `ChessPosition` [public].
- Refatorar `ChessMatch.InitialSetup`.

### Conceitos de POO abordados:
- Exceções
- Encapsulamento
- Construtores com mensagem obrigatória
- Sobrescrita
- Membros estáticos
- Padrão de camadas

---

## 7. Melhorias na Impressão do Tabuleiro
### Checklist:
- Adicionar mais peças ao tabuleiro.
- Diferenciar cores das peças no método `UI.PrintPiece`.

---

## 8. Movimento das Peças
### Checklist:
- Criar os métodos:
  - `Board.RemovePiece`
  - `UI.ReadChessPosition`
  - `ChessMatch.PerformChessMove`
  - `ChessMatch.MakeMove`
  - `ChessMatch.ValidateSourcePosition`

### Conceitos de POO abordados:
- Exceções
- Encapsulamento

---

## 9. Tratamento de Exceções e Limpeza da Tela
### Checklist:
- Implementar a limpeza de tela no Java.
- Adicionar tratamento de exceções `ChessException` e `InputMismatchException`.

---

## 10. Movimentos Possíveis de uma Peça
### Checklist:
- Criar os métodos na classe `Piece`:
  - `PossibleMoves` [abstract]
  - `PossibleMove`
  - `IsThereAnyPossibleMove`
- Implementar `PossibleMove` para `Rook` e `King`.
- Atualizar `ChessMatch.ValidateSourcePosition`.

### Conceitos de POO abordados:
- Métodos e classes abstratas
- Exceções

---

## 11. Implementação dos Movimentos do Rook
### Checklist:
- Criar o método `ChessPiece.IsThereOpponentPiece(position)` [protected].
- Implementar `Rook.PossibleMoves`.
- Criar o método `ChessMatch.ValidateTargetPosition`.

---

## 12. Implementação dos Movimentos do King
### Checklist:
- Criar o método `King.CanMove(position)` [private].
- Implementar `King.PossibleMoves`.

---

## 13. Alternância de Turnos
### Checklist:
- Criar na classe `ChessMatch`:
  - Propriedades `Turn`, `CurrentPlayer` [private set]
  - Método `NextTurn` [private]
- Atualizar `PerformChessMove`.
- Atualizar `ValidateSourcePosition`.
- Criar o método `UI.PrintMatch`.

---

## 14. Captura de Peças
### Checklist:
- Criar o método `UI.PrintCapturedPieces`.
- Atualizar `UI.PrintMatch`.
- Atualizar a lógica do programa.
- Criar listas em `ChessMatch`:
  - `_piecesOnTheBoard`
  - `_capturedPieces`

---

## 15. Implementação da Lógica de Xeque
### Checklist:
- Criar propriedade `ChessPiece.ChessPosition` [get].
- Implementar métodos na classe `ChessMatch`:
  - `UndoMove`
  - `Check` [private set]
  - `Opponent(color)` [private]
  - `King(color)` [private]
  - `TestCheck`
- Atualizar `PerformChessMove`.

---

## 16. Implementação da Lógica de Xeque-Mate
### Checklist:
- Criar a propriedade `Checkmate` [private set].
- Criar o método `TestCheckmate` [private].

---

## 17. Contagem de Movimentos das Peças
### Checklist:
- Criar propriedade `MoveCount` na classe `ChessPiece`.
- Criar os métodos:
  - `IncreaseMoveCount`
  - `DecreaseMoveCount`
- Atualizar `MakeMove` e `UndoMove`.

---

## 18. Implementação de Peças Especiais
### Checklist:
- Criar classes:
  - `Pawn`
  - `Bishop`
  - `Knight`
  - `Queen`

---

## 19. Implementação de Movimentos Especiais
### Checklist:
- Roque (Castling)
- En Passant
- Promoção de Peão

---
