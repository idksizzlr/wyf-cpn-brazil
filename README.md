# CPN · GT Comunicação — Formulário de Inscrição

Página de inscrição de voluntários para o **Grupo de Trabalho de Comunicação do CPN/WYF Brasil**, hospedada via GitHub Pages.

## Acesso

🔗 **[idksizzlr.github.io/wyf-cpn-brazil](https://idksizzlr.github.io/wyf-cpn-brazil)**

## O que é

Formulário web para seleção de voluntários do GT de Comunicação. Os candidatos respondem perguntas sobre ferramentas, formatos, disponibilidade e cenários práticos. As respostas são enviadas para uma planilha Google Sheets via Apps Script, onde cada inscrito recebe uma **pontuação automática de 0 a 100** e entra no ranking.

## Como funciona o ranking

O Apps Script calcula a nota com base em 5 critérios:

| Critério | Peso |
|---|---|
| Domínio de Ferramentas Digitais | 25% |
| Criatividade e Estética | 25% |
| Proatividade | 20% |
| Organização e Compromisso | 20% |
| Interesse pela Causa | 10% |

A nota final é multiplicada por um fator de disponibilidade (horas/semana), podendo chegar até 130 pontos antes do teto de 100.

## Estrutura

```
wyf-cpn-brazil/
└── index.html   # formulário completo (HTML + CSS + JS inline)
```

O formulário é um arquivo único sem dependências externas além de fontes Google. Não requer build, servidor ou framework.

## Atualizar o formulário

1. Edite ou substitua `index.html`
2. Faça commit e push na branch `main`
3. O GitHub Pages atualiza em ~1 minuto

## Apps Script (backend)

O script que recebe as respostas, salva na planilha e gera o ranking está vinculado à planilha Google Sheets do GT. Para reimplantar:

1. Abra a planilha → **Extensões > Apps Script**
2. Cole o código do Apps Script v3
3. **Implantar > Nova implantação** → Tipo: App da Web → Acesso: Qualquer pessoa
4. Copie a URL gerada e atualize a constante `ENDPOINT` no `index.html`
