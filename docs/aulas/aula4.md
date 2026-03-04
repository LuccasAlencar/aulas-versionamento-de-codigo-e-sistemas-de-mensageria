---
title: "Aula 4 — Visão geral das ferramentas de versionamento"
layout: default
---

## Antes de começar

Antes de mergulharmos no mundo do Git e GitHub, pense um pouco sobre o seguinte:

- Como você gerenciaria as alterações em seu app sem algum tipo de sistema para rastrear e organizar essas mudanças?

## O que você vai aprender nesta aula

Nesta aula, você irá:
- Entender o conceito de versionamento de código.
- Conhecer e usar o Git como ferramenta básica de controle de versão.
- Criar e gerenciar branches no Git para evitar conflitos durante o desenvolvimento.
- Navegar e colaborar em projetos usando a plataforma GitHub.

## Versionamento de Código

Hoje vamos falar sobre um tópico que pode parecer complicado, mas é essencial na programação e no desenvolvimento de software. Quando você joga seu jogo favorito ou posta uma foto nas redes sociais, tudo isso acontece graças a código por trás das telas. E esse código precisa ser gerenciado com cuidado.

### Entendendo o que é Versionamento de Código

Imagine que você está criando um novo app para compartilhar fotos. À medida que você e sua equipe adicionam novos recursos, corrigem bugs e melhoram a interface do usuário, surgem muitas versões diferentes desse aplicativo. O versionamento de código é como manter um diário detalhado dessas mudanças.

### A Importância do Versionamento

Sem versionamento, seria muito difícil voltar a uma versão anterior se algo der errado. Com um bom sistema de controle de versões, você pode facilmente ver o que foi alterado, quem fez as alterações e quando. Isso é crucial para manter projetos grandes funcionando bem.

### Exemplo Prático: Usando Git

Vamos usar o **Git**, um dos sistemas mais populares para versionamento de código. Vou guiar vocês através do processo básico:

1. Primeiro, crie uma pasta no seu computador para o projeto.
2. Inicialize essa pasta como um repositório git com `git init`.
3. Adicione e faça o primeiro commit (salva) das alterações com `git add .` seguido de `git commit -m "Primeiro commit"`.

Agora você tem seu próprio sistema de versionamento funcionando!

### Atividade

Abra uma nova janela no terminal do seu computador e siga os passos acima. Depois, faça mais algumas alterações em algum arquivo dentro da pasta criada e comite essas mudanças também.

> 🤔 **Para refletir:** Como o versionamento de código facilitou a manutenção e colaboração nesse projeto?

## Entendendo o Git

Olá pessoal! Hoje vamos falar sobre algo que é essencial para muitos profissionais de tecnologia e que vai mudar a forma como você trabalha com projetos de software.

### O que é o Git?

Você já deve ter usado aplicativos de redes sociais ou jogos onde suas informações são armazenadas em um servidor. Mas, e se eu te disser que existem ferramentas que permitem que você controle suas próprias informações? Isso mesmo, estamos falando do **Git**! O Git é uma ferramenta distribuída e segura para gerenciar o versionamento de código. Ele permite que você crie cópias locais dos seus projetos, trabalhe neles offline e depois sincronize suas alterações com outras versões.

### Criando uma branch

Agora vamos a um exemplo prático: Imagine que está desenvolvendo um novo recurso para um aplicativo de redes sociais. Você não quer interromper o código existente enquanto cria essa nova funcionalidade, certo? Aqui é onde as **branches** entram em jogo!

1. Primeiro, você precisa criar uma branch chamada `nova-funcionalidade`. No terminal, digite:
   ```
   git checkout -b nova-funcionalidade
   ```

2. Agora, faça os ajustes necessários no código e depois comite suas alterações usando o comando:
   ```
   git commit -m "Adicionando a nova funcionalidade"
   ```

### Para refletir:

> 🤔 **Para refletir:** Como você usaria branches em um projeto real para evitar conflitos de desenvolvimento?

## Navegando no GitHub

Bem-vindo ao mundo do desenvolvimento de software! Você já deve ter notado que, assim como você usa redes sociais e aplicativos para se conectar com amigos, os programadores usam plataformas específicas para trabalhar juntos. O GitHub é uma dessas plataformas.

### O Que É o GitHub?

Imagine o GitHub como um grande armazém de código onde desenvolvedores compartilham projetos e colaboram uns com os outros. Além disso, ele oferece muitas ferramentas além do controle de versão, como issue tracking (rastreamento de problemas) e pull requests (solicitações de incorporação).

### Exemplo Prático: Colaborando em um Projeto

Vamos ver como você pode usar o GitHub para colaborar com os colegas na sua turma. Crie uma conta no GitHub se ainda não tiver uma. Depois, siga esses passos:

1. **Criação do Repositório:** Faça login e crie um novo repositório público.
2. **Adicionar Arquivos:** Adicione alguns arquivos de código ao seu repositório para começar.
3. **Convidar Amigos:** Convide seus colegas para colaborar no projeto, adicionando-os como contribuidores.

> 🤔 **Para refletir:** Como a cooperação e o compartilhamento em um ambiente online podem melhorar a qualidade do seu trabalho?

## Para fechar — com as suas palavras

Escreva uma breve descrição de tudo que você aprendeu hoje sobre versionamento de código, Git e GitHub.

## O que fica desta aula
```markdown
- Versionamento: Sistema para rastrear alterações em projetos.
- Git: Ferramenta distribuída para controle de versão.
- Branches: Ramificações no desenvolvimento para evitar conflitos.
```

## Para ir além

1. [Documentação oficial do Git](https://git-scm.com/doc)
2. [Guia prático sobre GitHub](https://guides.github.com/)

## Referências
- Pro Git, Scott Chacon e Ben Straub (http://git-scm.com/book/en/v2)
- GitHub Learning Lab (https://lab.github.com/)