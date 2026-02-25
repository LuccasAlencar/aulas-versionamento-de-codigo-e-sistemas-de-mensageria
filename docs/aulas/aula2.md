# Aula 2 – Por que versionar um código?
**Duração:** ~50 minutos  
**Unidade:** Fundamentos do versionamento de código  

---

## 🎯 Objetivos da Aula
- Refletir sobre os benefícios reais do versionamento.  
- Analisar casos de falhas que aconteceram por falta de controle.  
- Entender como o versionamento traz segurança ao desenvolvimento.  

---

## 🧠 1. Relembrando

Com versionamento, cada mudança registrada contém:

- autor,  
- data,  
- descrição,  
- arquivos alterados.

Isso cria uma **documentação viva do projeto**.

Sem isso, estamos no escuro.

---

## 💸 2. Caso real: Knight Capital Group (2012)

Um dos maiores desastres de TI da história.

### O que aconteceu?
- Deploy manual em 8 servidores diferentes.  
- Um servidor ficou com **uma versão antiga** do software.  
- O sistema passou a comprar/vender ações errado.

### Em **45 minutos**:
- Perderam **460 milhões de dólares**,  
- O mercado travou,  
- A empresa quase faliu.

### Por quê?
- Sem histórico confiável,  
- Sem rollback,  
- Mudanças não rastreadas,  
- Deploy sem controle.

---

## 🧩 3. Sem versionamento x com versionamento

### 🔴 Sem versionamento:
- Não sabemos quem mudou o quê.  
- Não dá para comparar versões.  
- Não dá para voltar atrás.  
- Arquivos podem ser sobrescritos.  
- Bugs surgem do nada e ninguém identifica.

### 🟢 Com versionamento:
- Histórico completo.  
- Autoria e data registradas.  
- É possível reverter versões.  
- Times inteiros trabalham juntos.  
- Segurança e rastreabilidade.

---

## ✏️ 4. Atividade: Simulador de problemas (versão no caderno)

Imagine que 4 pessoas editam o mesmo arquivo.  

1. Uma apaga um trecho que achou inútil.  
2. Outra modifica algo que depende do trecho apagado.  
3. Uma terceira tem uma versão antiga.  
4. Surge um bug — e vocês precisam voltar **2 versões**.

### Agora responda:

- O arquivo final faz sentido?  
- É possível recuperar a versão antiga?  
- Como descobrir quem apagou algo?  
- Como o Git resolveria isso?  

---

## 🔒 5. Segurança no versionamento

Com versionamento você tem:

- cópias distribuídas do código,  
- integridade garantida (hash),  
- histórico rastreável,  
- recuperação rápida,  
- proteção contra perda acidental.

---

## 🔁 6. Recuperação: a máquina do tempo do código

Alguns exemplos do que é possível fazer com versionamento:

- Voltar para versões anteriores.  
- Recuperar arquivos apagados.  
- Rastrear o commit que introduziu um bug.  
- Marcar versões importantes com tags.  
- Comparar mudanças linha a linha.

---

## 🧠 7. Pergunta final (anote no caderno)

**Qual é o problema mais crítico ao desenvolver sem versionamento? Explique com suas palavras.**

- ( ) Uso de muito espaço no HD  
- ( ) Código mais lento  
- ( ) Dificuldade de aprender  
- (✔) Perda irreversível de trabalho  

---

## ✅ Encerramento

Agora você entende por que **nenhuma equipe profissional trabalha sem versionamento**.  
Na próxima fase, vamos aprender como usar **Git e GitHub** na prática.