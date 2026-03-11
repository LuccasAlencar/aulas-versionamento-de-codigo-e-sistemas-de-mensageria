---
title: "Aula 9 — Histórico e commits via web"
layout: default
---

# Aula 9 — Histórico e commits via web

## 🎯 Objetivo da aula
Compreender a estrutura de um commit, aprender a navegar na linha do tempo de um projeto e dominar a interface web do GitHub para auditoria, comparação de versões e correção de erros.

---

## 🕒 Aquecimento: A Máquina do Tempo (5 min)
Imagine que você está trabalhando em um código complexo e, após horas de trabalho, percebe que uma alteração feita no início do dia quebrou uma função essencial. Sem o Git, você teria que usar o "Ctrl + Z" infinitamente (e rezar para não ter fechado o editor). 

**Para refletir:** Como você organiza as versões dos seus arquivos hoje? Já perdeu algum trabalho por salvar algo por cima de uma versão importante?

---

## 📖 Conteúdo Principal (15 min)

### 1. O que realmente é um Commit?
Diferente de um simples "Salvar" do Word, um commit no Git é um **Snapshot (foto)** do estado atual dos seus arquivos. Ele carrega consigo:
* **Identificador Único (Hash):** Uma sequência alfanumérica (ex: `1a2b3c4`) que garante que aquela versão nunca seja confundida.
* **Metadados:** Autor, data, hora e o estado anterior (pai).
* **Mensagem de Commit:** A explicação humana do que mudou.

### 2. O Poder do "Diff"
No GitHub, ao visualizar o histórico, você verá o "Diff" (Diferença). 
* **Linhas Verdes (+):** Representam o código que você adicionou.
* **Linhas Vermelhas (-):** Representam o código que foi removido ou alterado.
* *Dica:* Sempre revise o Diff antes de confirmar um commit para garantir que não está enviando lixo ou senhas por engano.

### 3. Boas Práticas: Mensagens Profissionais
No mercado de trabalho, mensagens como "ajuste" ou "teste" são proibidas. Tente seguir o padrão:
* **Estrutura:** `Tipo: Descrição curta`
* *Exemplo:* `feat: adiciona seção de biografia no perfil`
* *Exemplo:* `fix: corrige alinhamento do botão de contato`

---

## 🛠️ Atividade Prática: Mão na Massa (15 min)

### Passo 1: O Registro Histórico
1.  Acesse o repositório que você criou para o seu perfil.
2.  Abra o arquivo `index.html` ou `README.md`.
3.  Faça uma alteração significativa (mude uma cor, adicione um parágrafo).
4.  No campo de commit, escreva um título e uma descrição detalhada. **Não use apenas uma palavra!**

### Passo 2: Investigação via Web
1.  Clique no botão **"Commits"** (localizado acima da lista de arquivos).
2.  Clique em um dos commits da lista.
3.  Explore a visualização: mude de "Unified" para "Split" para ver o código antigo e o novo lado a lado.

### Passo 3: O Botão de Pânico (Revert)
1.  Simule um erro: apague uma linha importante do seu código e faça o commit com a mensagem "Remoção acidental".
2.  Vá ao histórico de commits, abra esse commit específico.
3.  No canto superior direito, clique nos três pontinhos `...` e selecione **"Revert"**. 
4.  O GitHub criará um novo commit desfazendo a alteração. Aceite e veja a mágica acontecer.

---

## 📝 Exercícios de Fixação (5 min)
1.  Por que é melhor fazer vários commits pequenos do que um único commit gigante no final do dia?
2.  O que acontece com o código original quando usamos a função "Revert"?

---

## 📚 Referências e Leitura Complementar
* [Documentação Oficial: Visualizando Commits](https://docs.github.com/pt/pull-requests/committing-changes-to-your-project/viewing-and-comparing-commits)
* [Convenções de Mensagens de Commit](https://www.conventionalcommits.org/pt-br/v1.0.0/)