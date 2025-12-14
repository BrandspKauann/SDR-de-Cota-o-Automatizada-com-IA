# 💰 Agente de IA HIRAYAMA – SDR de Cotação Automatizada

> **SDR especializado em cotações**, focado em entender a demanda do lead, coletar variáveis comerciais e entregar **orçamento claro e rápido**, via conversa automatizada.

---

## 🧭 Visão Geral

Este workflow implementa o **Agente de IA HIRAYAMA**, um **SDR de cotação**, responsável por:

* 📥 Receber solicitações de orçamento
* 🧠 Entender o contexto da necessidade do cliente
* 📋 Coletar variáveis essenciais para cotação
* 🧮 Estruturar a lógica de precificação
* 💬 Apresentar valores de forma clara e consultiva
* 📅 Encaminhar para reunião quando necessário

O agente atua antes do vendedor humano, **eliminando retrabalho**, acelerando o ciclo de vendas e padronizando propostas.

---

## 🏗️ Arquitetura Geral

```
[ Lead / Cliente ]
        |
        v
[ Canal de Entrada ]
        |
        v
[ Webhook HIRAYAMA ]
        |
        v
[ Interpretação da Demanda ]
        |
        v
[ Coleta de Variáveis ]
        |
        v
[ IA de Cotação ]
        |
        +---------> [ Precificação ]
        |
        v
[ Resposta ao Lead ]
        |
        v
[ Reunião ou Encerramento ]
```

---

## 🧰 Tecnologias Utilizadas

| Camada       | Tecnologia           | Função                   |
| ------------ | -------------------- | ------------------------ |
| Orquestração | **n8n**              | Backend conversacional   |
| IA           | **OpenAI / LLM**     | Interpretação + cotação  |
| Memória      | **Redis / Contexto** | Continuidade da conversa |
| Comunicação  | **Webhook / API**    | Entrada de dados         |
| Saída        | **WhatsApp / Chat**  | Envio da cotação         |

---

## 🔌 Entrada do Sistema

**Endpoint:**

```
POST /webhook/hirayama
```

Recebe mensagens contendo:

* Pedido direto de cotação
* Descrição do serviço/produto
* Dúvidas sobre preço

---

## 🧠 Interpretação da Demanda

**Node:** `Agente HIRAYAMA`

A IA analisa:

* Tipo de serviço
* Volume
* Urgência
* Complexidade
* Perfil do cliente

Objetivo: **entender o que precisa ser orçado antes de falar em preço**.

---

## 📋 Coleta de Variáveis de Cotação

O agente conduz a conversa para coletar:

* 📦 Tipo de serviço ou produto
* 📐 Escopo
* 🔢 Quantidade
* ⏱️ Prazo
* 🏢 Tipo de empresa

> Perguntas são feitas apenas se necessárias, mantendo a conversa fluida.

---

## 🧮 Lógica de Precificação

A IA utiliza regras de negócio embutidas no prompt para:

* Definir faixa de preço
* Ajustar valor por complexidade
* Adaptar linguagem ao perfil do lead

Exemplos:

* Cotação fixa
* Cotação por volume
* Cotação sob consulta (com reunião)

---

## 💬 Apresentação da Cotação

**Saída do agente:**

* Valor ou faixa de preço
* O que está incluso
* Próximos passos

Sempre com tom:

* Profissional
* Claro
* Sem jargões desnecessários

---

## 🔁 Memória Conversacional

* Mantém contexto por lead
* Evita repetir perguntas
* Permite ajustes na cotação

---

## 📅 Encaminhamento para Reunião

Quando detectado:

* Escopo complexo
* Valor alto
* Dúvidas recorrentes

O agente:

* Sugere reunião
* Encaminha para SDR humano ou closer

---

## 📐 Formulação do Problema

### 🎯 Objetivo

Reduzir o tempo de resposta em cotações e aumentar taxa de conversão.

---

### 🔢 Variáveis

* **N** = número de pedidos de cotação
* **Q** = quantidade de perguntas necessárias
* **Cᵢ** = custo por interação de IA
* **V** = valor médio da proposta

---

### ⏱️ Complexidade

* Temporal: **O(N × Q)**

---

### 💰 Custo estimado

```
Custo ≈ N × Q × Cᵢ
```

---

## 🌟 Diferenciais do Agente HIRAYAMA

* Cotação em tempo real
* Atendimento 24/7
* Padronização comercial
* Menos fricção com vendas
* Escalável

---

## ✅ Conclusão

O **Agente de IA HIRAYAMA** transforma o n8n em um **SDR de cotação inteligente**, acelerando vendas, reduzindo custo operacional e aumentando a eficiência comercial.
