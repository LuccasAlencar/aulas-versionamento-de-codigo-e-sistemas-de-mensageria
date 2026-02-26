# Aula 3 – Conceitos de repositório e histórico
**Componente:** Versionamento de Código e Sistemas de Mensageria  
**Unidade 1:** Fundamentos do versionamento de código  
**Código da aula:** SISANO2C5B1S1A3  
**Duração aproximada:** 50 minutos  
**Ano:** 3º ano do Ensino Médio Técnico (ANO2)

---

# 1. Você está aqui!

Imagine que você está construindo uma história em quadrinhos. Você desenha, apaga, melhora, testa novas ideias... Agora imagine se você pudesse salvar **cada versão** dessa história, com data, hora e uma anotação do que mudou. E mais: pudesse voltar para qualquer página do passado.

Pois é exatamente isso que o **versionamento de código** faz com o seu projeto de software. E hoje vamos conhecer o coração disso: o **repositório** e o **histórico**.

---

# 2. O diário mágico e os saves dos games

Vamos começar com duas histórias que você provavelmente conhece.

> **Ana mantém um diário há 5 anos. Mas não é um diário comum:**
> - Cada entrada tem **data e hora**;
> - Ela **nunca apaga nada**, só adiciona;
> - Pode **ver como estava em qualquer dia**;
> - Guarda uma **cópia no cofre da escola**;
> - Às vezes, **compartilha páginas** com amigas.

> **Pedro tem todos os seus jogos salvos:**
> - **Save local** no computador;
> - **Backup na nuvem**;
> - Pode **voltar para qualquer fase**;
> - **Compartilha saves** com amigos;
> - **Nunca perde progresso**.

---

## Pause e reflita (no caderno)

1. O que o diário da Ana e os saves do Pedro têm em comum?  
2. Como isso pode se parecer com um sistema de versionamento de código?

---

# 3. Construindo o conceito: o que é um repositório?

Um **repositório** (ou só “repo”) é o **local de armazenamento** de todo o histórico do seu projeto.  
Pense nele como uma **casa do código** – dentro dela moram:

- Todos os arquivos do projeto;
- Todas as versões (desde a primeira linha de código);
- Um “diário” completo de quem fez o quê e quando.

### Analogias para fixar

| Você conhece... | ...funciona como um repositório |
|----------------|----------------------------------|
| Biblioteca | Guarda todos os livros (arquivos) organizados |
| Banco | Guarda dinheiro com segurança (código) |
| Armazém | Organiza produtos em versões |
| Arquivo histórico | Preserva documentos importantes (commits) |
| Memory card | Salva o progresso do jogo (estados) |

---

# 4. A anatomia de um repositório

Visualmente, um repositório tem essa cara:

meu-projeto/
├── .git/ ← “Cérebro” do repositório (histórico, configurações)
├── arquivos/ ← Seu código atual
└── README.md ← Documentação


**Tome nota:**  
> Repositório = Código + Histórico + Metadados  
> É um **projeto com memória**!

---

# 5. Repositório local vs. remoto

Existem dois tipos principais de repositório:

- **Local**: está no seu computador. Você trabalha, testa, experimenta à vontade.
- **Remoto**: está em um servidor (como o GitHub). É o backup na nuvem e o ponto de encontro para times.

A comunicação entre eles é simples:

[ Seu PC ] <-- push / pull --> [ GitHub ]
Local Remoto
↓ Trabalha ↓ Compartilha


### Benefícios de cada um

| Local                          | Remoto                          |
|--------------------------------|----------------------------------|
| Velocidade total               | Backup automático               |
| Funciona offline               | Colaboração fácil               |
| Privacidade para experimentos  | Acesso de qualquer lugar        |
| Controle total                 | Portfólio público (se quiser)   |

**Curiosidade:** O GitHub hospeda **mais de 100 milhões de repositórios**!

---

# 6. O coração do versionamento: o commit

Um **commit** é um **snapshot** (uma foto) do seu projeto em um momento específico.  
Cada commit vem com uma mensagem explicando **o que mudou**.

### Anatomia de um commit
commit a7f8d9e ← ID único (hash)
Author: João Silva
Date: 2024-07-20 14:30
Message: "Adiciona validação de CPF"
Mudanças:

    function validaCPF(cpf) {

    return cpf.length === 11;

    }


### O que todo commit contém

- **Hash**: identificador único (tipo um CPF do commit);
- **Autor**: nome e e-mail de quem fez;
- **Timestamp**: data e hora exatos;
- **Mensagem**: descrição da mudança;
- **Parent**: commit anterior (forma a corrente);
- **Diff**: exatamente o que mudou no código.

Os commits se ligam em uma corrente:

[Início] → [Commit 1] → [Commit 2] → [Commit 3] → [HEAD (versão atual)]
"Setup" "Add Login" "Fix bug" "Você está aqui"


---

# 7. O poder do log (histórico)

O **log** é a **linha do tempo completa** do seu projeto.  
Com ele, você descobre:

- Quem fez cada mudança;
- Quando foi feita;
- Por que foi feita;
- O que exatamente mudou;
- Como o projeto evoluiu.

### Visualizações comuns

| Comando                     | Mostra                     |
|-----------------------------|----------------------------|
| `git log --oneline`         | Resumo compacto            |
| `git log --graph`           | Árvore visual              |
| `git log --stat`            | Arquivos mudados           |
| `git log -p`                | Mudanças detalhadas        |
| `git log --author="João"`   | Só commits do João         |

---

# 8. Boas práticas: mensagens de commit

Uma boa mensagem conta a história **claramente**. Compare:

### ❌ Ruins (comuns)
- “fix”
- “mudanças”
- “teste”
- “asdfasdf”
- “commit final”
- “agora vai”

### ✅ Boas (profissionais)
- “Corrige validação de CPF para aceitar pontos”
- “Adiciona autenticação por biometria”
- “Remove código duplicado no módulo de pagamento”
- “Atualiza dependências para versões seguras”
- “Implementa cache para melhorar performance”

### Formato recomendado


---

# 7. O poder do log (histórico)

O **log** é a **linha do tempo completa** do seu projeto.  
Com ele, você descobre:

- Quem fez cada mudança;
- Quando foi feita;
- Por que foi feita;
- O que exatamente mudou;
- Como o projeto evoluiu.

### Visualizações comuns

| Comando                     | Mostra                     |
|-----------------------------|----------------------------|
| `git log --oneline`         | Resumo compacto            |
| `git log --graph`           | Árvore visual              |
| `git log --stat`            | Arquivos mudados           |
| `git log -p`                | Mudanças detalhadas        |
| `git log --author="João"`   | Só commits do João         |

---

# 8. Boas práticas: mensagens de commit

Uma boa mensagem conta a história **claramente**. Compare:

### ❌ Ruins (comuns)
- “fix”
- “mudanças”
- “teste”
- “asdfasdf”
- “commit final”
- “agora vai”

### ✅ Boas (profissionais)
- “Corrige validação de CPF para aceitar pontos”
- “Adiciona autenticação por biometria”
- “Remove código duplicado no módulo de pagamento”
- “Atualiza dependências para versões seguras”
- “Implementa cache para melhorar performance”

### Formato recomendado

[Tipo]: [Descrição breve no imperativo]

[Corpo opcional com mais detalhes]

[Rodapé com issues/referências]


**Exemplo:**
feat: Adiciona exportação para PDF

Implementa função para gerar relatórios em PDF
usando a biblioteca PDFKit. Inclui opções de
formatação e marca d’água.

Closes #123


---

# 9. Atividade no caderno – Criando um repositório: app de receitas

**Em duplas (ou individual)**

Vocês vão **projetar** (apenas no papel) um repositório para um aplicativo de receitas.  
Siga os passos e registre tudo no caderno.

## Passo 1 – Nome do repositório
Crie um nome criativo. Exemplo: `app-receitas-da-vovo`

## Passo 2 – Primeiros cinco commits
Escreva as mensagens dos **cinco primeiros commits** que você faria, em ordem lógica.  
Use o estilo profissional que acabamos de ver.

- Commit 1: ________________________________________
- Commit 2: ________________________________________
- Commit 3: ________________________________________
- Commit 4: ________________________________________
- Commit 5: ________________________________________

## Passo 3 – Estrutura de pastas
Desenhe (ou escreva) a estrutura de pastas que seu projeto teria. Exemplo:

📁 app-receitas/
├── 📁 src/
│ ├── 📁 components/
│ ├── 📁 pages/
│ ├── 📁 services/
│ └── 📁 assets/
├── 📁 docs/
├── 📄 README.md
├── 📄 .gitignore
└── 📄 LICENSE


---

# 10. Hora da revisão entre grupos

Troque seu caderno com outra dupla (ou, se estiver sozinho, releia o seu com olhar crítico).  
Analisem:

1. As mensagens de commit são **claras**?
2. Dá para entender a **evolução** do projeto?
3. A estrutura de pastas **faz sentido**? (componentes separados, assets organizados...)
4. O que vocês **melhorariam**? Liste pelo menos uma melhoria.

**Melhorias possíveis:**  
- Usar prefixos como `feat:`, `fix:`, `docs:`;  
- Incluir um arquivo `CONTRIBUTING.md`;  
- Adicionar testes simples;  
- Criar um arquivo de exemplo de configuração (`.env.example`).

---

# 11. Pause e responda

**Pergunta:** Qual é a principal diferença entre repositório local e remoto?

- [ ] O local é grátis; o remoto é pago.
- [ ] O local é mais seguro que o remoto.
- [ ] Não há diferença, são sinônimos.
- [x] **O local está no seu PC; o remoto está em um servidor.**

> **Feedback:** O repositório local fica no computador do desenvolvedor, permitindo editar e versionar offline. Já o remoto, em servidores como o GitHub, garante acesso compartilhado, colaboração e backup – essencial para trabalho em equipe.

---

# 12. O que nós aprendemos hoje?

✅ Que o **repositório** é a “casa do código”, com toda a sua história.  
✅ Que o **commit** é a “foto do momento”, com autor, data e mensagem.  
✅ Que **boas mensagens** contam a história de forma clara e profissional.  
✅ A diferença entre **repositório local e remoto**.  
✅ Como **planejar a estrutura** e os primeiros commits de um projeto.

---

# 13. Para explorar (desafio)

Se você tiver acesso à internet em casa, entre no [GitHub Explore](https://github.com/explore) e dê uma olhada em repositórios famosos como **React**, **Vue.js** ou **Visual Studio Code**.

Observe:
- Como eles organizam as pastas?
- Como são as mensagens de commit?
- Eles têm arquivos como `README.md`, `LICENSE`, `.gitignore`?

Isso vai te ajudar a entender como os profissionais fazem na prática!

---

**Bônus:** No GitHub, você pode navegar pelo histórico de qualquer repositório público. É como viajar no tempo dentro do código!


---

# 10. Hora da revisão entre grupos

Troque seu caderno com outra dupla (ou, se estiver sozinho, releia o seu com olhar crítico).  
Analisem:

1. As mensagens de commit são **claras**?
2. Dá para entender a **evolução** do projeto?
3. A estrutura de pastas **faz sentido**? (componentes separados, assets organizados...)
4. O que vocês **melhorariam**? Liste pelo menos uma melhoria.

**Melhorias possíveis:**  
- Usar prefixos como `feat:`, `fix:`, `docs:`;  
- Incluir um arquivo `CONTRIBUTING.md`;  
- Adicionar testes simples;  
- Criar um arquivo de exemplo de configuração (`.env.example`).

---

# 11. Pause e responda

**Pergunta:** Qual é a principal diferença entre repositório local e remoto?

- [ ] O local é grátis; o remoto é pago.
- [ ] O local é mais seguro que o remoto.
- [ ] Não há diferença, são sinônimos.
- [x] **O local está no seu PC; o remoto está em um servidor.**

> **Feedback:** O repositório local fica no computador do desenvolvedor, permitindo editar e versionar offline. Já o remoto, em servidores como o GitHub, garante acesso compartilhado, colaboração e backup – essencial para trabalho em equipe.

---

# 12. O que nós aprendemos hoje?

✅ Que o **repositório** é a “casa do código”, com toda a sua história.  
✅ Que o **commit** é a “foto do momento”, com autor, data e mensagem.  
✅ Que **boas mensagens** contam a história de forma clara e profissional.  
✅ A diferença entre **repositório local e remoto**.  
✅ Como **planejar a estrutura** e os primeiros commits de um projeto.

---

# 13. Para explorar (desafio)

Se você tiver acesso à internet em casa, entre no [GitHub Explore](https://github.com/explore) e dê uma olhada em repositórios famosos como **React**, **Vue.js** ou **Visual Studio Code**.

Observe:
- Como eles organizam as pastas?
- Como são as mensagens de commit?
- Eles têm arquivos como `README.md`, `LICENSE`, `.gitignore`?

Isso vai te ajudar a entender como os profissionais fazem na prática!

---

**Bônus:** No GitHub, você pode navegar pelo histórico de qualquer repositório público. É como viajar no tempo dentro do código!