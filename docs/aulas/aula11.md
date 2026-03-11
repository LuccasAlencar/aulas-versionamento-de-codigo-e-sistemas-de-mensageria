---
title: "Aula 11 — Clonagem e modificação"
layout: default
---

# Aula 11 — Clonagem e modificação

## 🎯 Objetivo da aula
Aprender a trazer projetos da nuvem para o seu computador local, realizar alterações de forma organizada e sincronizar seu trabalho com o servidor remoto, mantendo um histórico limpo.

---

## 🕒 Aquecimento (5 min)
Até agora, mexemos muito na interface web do GitHub. Mas, no dia a dia, os desenvolvedores trabalham em suas próprias máquinas (localmente). 
**Pense o seguinte:** Se o GitHub é o "Google Drive" do código, como fazemos para baixar uma pasta e garantir que tudo o que eu mudar nela possa ser enviado de volta sem bagunçar o trabalho dos outros?

---

## 📖 Conteúdo Principal (15 min)

### 1. Clonagem: O seu "Download" Inteligente
O comando `git clone` é o ponto de partida. Ele não apenas baixa os arquivos, mas traz **todo o histórico de versões** do projeto.
* **Sintaxe:** `git clone <url-do-repositorio>`
* Ao clonar, o Git cria automaticamente uma conexão chamada `origin`, que aponta de volta para o servidor do GitHub.

### 2. O Fluxo de Trabalho Local
Quando você altera um arquivo no seu PC, ele passa por três estados antes de chegar ao GitHub:
1.  **Modified:** Você alterou o arquivo, mas o Git ainda não "marcou" a mudança.
2.  **Staged (`git add`):** Você preparou a mudança para a foto (commit).
3.  **Committed (`git commit`):** A foto foi tirada e salva no seu banco de dados local.

### 3. Sincronização e o Pull Rebase
Antes de enviar seu trabalho (`git push`), você precisa garantir que não há novidades no servidor.
* **`git pull`:** Traz as mudanças da nuvem.
* **O segredo do `--rebase`:** Usar `git pull --rebase` evita que o Git crie "commits de merge" desnecessários. Ele coloca as suas alterações locais "em cima" das alterações que vieram do servidor, mantendo a linha do tempo do projeto reta e fácil de ler.

---

## 🛠️ Atividade Prática: Mão na Massa (15 min)

### Passo 1: Saindo da Web
1.  Abra o terminal (ou Git Bash) no seu computador.
2.  Navegue até uma pasta de sua preferência (ex: `cd Documents`).
3.  Clone o repositório que você criou nas aulas anteriores:
    ```bash
    git clone [https://github.com/SEU_USUARIO/NOME_DO_REPO.git](https://github.com/SEU_USUARIO/NOME_DO_REPO.git)
    ```
4.  Entre na pasta: `cd NOME_DO_REPO`.

### Passo 2: Modificação Local
1.  Abra a pasta no seu editor de código (VS Code, por exemplo).
2.  Crie um novo arquivo chamado `colaboracao.md` e escreva algo sobre o que aprendeu hoje.
3.  No terminal, prepare e salve a mudança:
    ```bash
    git add colaboracao.md
    git commit -m "feat: adiciona notas sobre clonagem local"
    ```

### Passo 3: O Fluxo Profissional de Sincronização
Para garantir que seu histórico fique limpo, execute os comandos nesta ordem:
1.  `git pull --rebase origin main` (Busca atualizações e organiza sua fila).
2.  `git push origin main` (Envia seu trabalho para o GitHub).

---

## 📝 Exercícios de Fixação (5 min)
1.  Qual a principal diferença entre baixar um arquivo `.zip` de um projeto e usar o `git clone`?
2.  Para que serve o comando `git add` antes do commit? (Dica: pense em uma "área de espera").
3.  Por que o `--rebase` é preferido em muitas empresas em vez do pull comum?

---

## 💡 Reflexão Final
> "Trabalhar localmente dá ao desenvolvedor velocidade e ferramentas poderosas. O Git é a ponte que garante que essa velocidade não se torne um caos na hora de juntar o código com o time."

---

## 📚 Referências e Leitura Complementar
* [Git Scm: O comando Clone](https://git-scm.com/docs/git-clone)
* [Entendendo o Git Rebase vs Merge](https://www.atlassian.com/br/git/tutorials/merging-vs-rebasing)
* [Documentação do GitHub: Clonando Repositórios](https://docs.github.com/pt/repositories/creating-and-managing-repositories/cloning-a-repository)