---
title: "Aula 10 — Compartilhamento e permissões"
layout: default
---

# Aula 10 — Compartilhamento e permissões

## 🎯 Objetivo da aula
Transformar um repositório individual em um ambiente de trabalho colaborativo, configurando permissões de acesso e regras de proteção para garantir a segurança do código em equipe.

---

## 🕒 Aquecimento (5 min)
Você já trabalhou em um grupo onde alguém, sem querer, editou o seu arquivo e apagou horas de progresso? Ou pior, onde ninguém sabia qual era a versão final do trabalho? No desenvolvimento profissional, o GitHub resolve isso através de **hierarquia de acesso**.

---

## 📖 Conteúdo Principal (20 min)

### 1. Colaboradores vs. Público
Mesmo que seu repositório seja público (todos podem ver), **apenas você** tem permissão de escrita por padrão. 
* **Convidando:** Para que um colega possa enviar código diretamente, você deve adicioná-lo em `Settings > Collaborators`.

### 2. Níveis de Acesso (Roles)
Em empresas, o acesso é granular:
* **Read:** Pode ver, abrir issues e sugerir mudanças (ideal para revisores).
* **Write:** Pode enviar código diretamente, criar branches e gerenciar tarefas.
* **Admin:** Pode deletar o repositório, mudar visibilidade e gerenciar outros usuários.

### 3. Branch Protection (O "Cinto de Segurança")
A branch `main` (principal) é sagrada. Se ela quebrar, o sistema do cliente para. 
Para evitar desastres, usamos **Regras de Proteção**:
* **Bloqueio de Push Direto:** Ninguém (nem você!) pode enviar código direto para a `main`.
* **Revisão Obrigatória:** Toda mudança deve passar por um **Pull Request** e ser aprovada por outra pessoa.

---

## 🛠️ Atividade Prática: Mão na Massa (10 min)

### Passo 1: Simulando a Equipe
1.  Escolha um colega de classe.
2.  Vá em `Settings > Collaborators` e adicione o nome de usuário dele.
3.  Peça para o colega aceitar o convite no e-mail ou nas notificações do GitHub dele.

### Passo 2: Configurando o "Segurança" do Projeto
1.  No seu repositório, vá em **Settings > Branches**.
2.  Clique em **Add branch protection rule**.
3.  Em "Branch name pattern", digite `main`.
4.  Marque a opção: **"Require a pull request before merging"**.
5.  Marque a opção: **"Require approvals"** (coloque o número 1).
6.  Salve as alterações.

### Passo 3: O Teste de Stress
1.  Peça para o seu colega tentar editar o seu arquivo `README.md` e tentar salvar direto na `main`.
2.  O GitHub irá bloquear e sugerir que ele crie uma **nova branch** e abra um **Pull Request**.

---

## 💬 Discussão: Ética e Segurança (5 min)
Se você fosse o dono de uma startup, daria acesso de "Admin" para todos os seus desenvolvedores? Quais são os riscos de um ex-funcionário ainda ter acesso de "Write" a um repositório?

---

## 📝 Exercícios de Fixação
1.  Qual a diferença entre um usuário que dá "Star" no seu projeto e um "Collaborator"?
2.  Por que a regra de proteção de branch é considerada uma boa prática em grandes empresas como Google e Netflix?

---

## 📚 Referências e Leitura Complementar
* [Gerenciando acesso em repositórios pessoais](https://docs.github.com/pt/account-and-profile/setting-up-and-managing-your-github-user-account/managing-access-to-your-personal-repositories/)
* [Sobre as regras de proteção de branch](https://docs.github.com/pt/repositories/configuring-branches-and-merges-in-your-repository/defining-the-mergeability-of-pull-requests/about-protected-branches)