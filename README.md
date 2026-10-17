# Quizz Copas

Quiz interativo com 10 perguntas sobre a Copa do Mundo de futebol masculino da FIFA (edição Catar 2022).

## Estrutura do repositório

```
quizz-copas/
├── .github/workflows/pages.yml   # Deploy automático no GitHub Pages
├── index.html                    # Aplicação completa (HTML + CSS + JavaScript) em um único arquivo
└── README.md                     # Este documento
```

## Site publicado

https://groffedemos.github.io/quizz-copas/

## Deploy (GitHub Pages)

A cada push na `main` (ou manualmente via *Actions > Deploy GitHub Pages > Run workflow*), o workflow `pages.yml` publica o `index.html` no GitHub Pages. A fonte do Pages está configurada como **GitHub Actions**.

## Como funciona

- São 10 perguntas de múltipla escolha, cada uma com **uma única resposta válida**.
- Ao escolher uma alternativa, o quiz indica se a resposta está correta e destaca a resposta certa.
- Uma barra de progresso mostra o andamento.
- Ao final é exibida a pontuação (acertos de 10) e uma mensagem de resultado.
- Há um botão no canto do card para alternar entre o **modo normal** e o **modo dark**. A escolha é salva no `localStorage`; na primeira visita é usado o tema do sistema (`prefers-color-scheme`).
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
