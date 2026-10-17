# Quizz Copas

Quiz interativo com 10 perguntas sobre a Copa do Mundo de futebol masculino da FIFA (edição Catar 2022).

## Estrutura do repositório

```
quizz-copas/
├── index.html   # Aplicação completa (HTML + CSS + JavaScript) em um único arquivo
└── README.md    # Este documento
```

## Como funciona

- São 10 perguntas de múltipla escolha, cada uma com **uma única resposta válida**.
- Ao escolher uma alternativa, o quiz indica se a resposta está correta e destaca a resposta certa.
- Uma barra de progresso mostra o andamento.
- Ao final é exibida a pontuação (acertos de 10) e uma mensagem de resultado.
- O botão **Refazer o quiz** reinicia o jogo, embaralhando a ordem das perguntas.

## Como executar

Não há dependências nem build. Basta abrir o `index.html` no navegador, ou servir localmente:

```bash
python -m http.server 8080
```

e acessar http://localhost:8080.

## Personalização

As perguntas ficam no array `questions` dentro do `index.html`. Cada item tem o formato:

```js
{ q: "Pergunta", options: ["A", "B", "C", "D"], answer: 0 } // answer = índice da opção correta
```
