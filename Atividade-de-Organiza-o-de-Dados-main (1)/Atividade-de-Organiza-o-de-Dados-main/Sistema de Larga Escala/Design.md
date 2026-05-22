# 🎨 Design do Sistema – FoodConnect

## 📖 Visão Geral

O FoodConnect foi projetado utilizando princípios de pensamento computacional e engenharia de software para criar uma plataforma moderna de delivery e gestão de restaurantes.

O sistema foi dividido em módulos independentes para facilitar manutenção, escalabilidade e organização do desenvolvimento.

---

# 🧠 Pensamento Computacional Aplicado

## 🔹 Decomposição

O sistema foi separado em partes menores para facilitar o desenvolvimento.

### Módulos Principais

### 1. Autenticação
Responsável pelo cadastro, login e gerenciamento de usuários.

Funções:
- Cadastro de clientes
- Login seguro
- Recuperação de senha
- Controle de permissões

---

### 2. Gestão de Restaurantes
Responsável pelo gerenciamento dos restaurantes cadastrados.

Funções:
- Cadastro de restaurantes
- Gerenciamento de cardápios
- Atualização de preços
- Controle de pedidos recebidos

---

### 3. Sistema de Pedidos
Responsável pelo fluxo principal da aplicação.

Funções:
- Criação de pedidos
- Carrinho de compras
- Pagamentos
- Histórico de pedidos

---

### 4. Rastreamento de Entregas
Responsável pelo acompanhamento do pedido em tempo real.

Funções:
- Status da entrega
- Localização do entregador
- Tempo estimado de chegada

---

### 5. Sistema Inteligente
Responsável pelas recomendações personalizadas.

Funções:
- Sugestão de refeições
- Análise de preferências
- Recomendações baseadas em histórico

---

# 🔍 Reconhecimento de Padrões

O FoodConnect utiliza padrões encontrados em sistemas modernos de delivery.

## Exemplos

- Estrutura semelhante ao iFood e Uber Eats
- Login baseado em aplicações bancárias
- Interface inspirada em marketplaces digitais
- Organização modular semelhante a plataformas SaaS

---

# 🧩 Abstração

Foi criado um modelo simplificado do sistema para representar apenas os componentes essenciais.

## Componentes Principais

- Usuário
- Restaurante
- Pedido
- Entregador
- Pagamento
- Administração

A abstração permite compreender o funcionamento geral sem analisar detalhes internos do código.

---

# ⚙️ Algoritmos Utilizados

## 🔹 Algoritmo de Recomendação
Analisa:
- Histórico de pedidos
- Categorias favoritas
- Avaliações anteriores

Objetivo:
Sugerir refeições compatíveis com o perfil do usuário.

---

## 🔹 Algoritmo de Rastreamento
Responsável por:
- Atualizar status da entrega
- Calcular tempo estimado
- Informar localização em tempo real

---

## 🔹 Algoritmo de Organização de Pedidos
Organiza automaticamente:
- Pedidos em andamento
- Pedidos entregues
- Prioridade de entrega

---

# 🏗️ Arquitetura do Sistema

O sistema segue arquitetura modular dividida em:

## Front-end
Interface gráfica do usuário.

Tecnologias:
- HTML
- CSS
- JavaScript

---

## Back-end
Responsável pelas regras de negócio.

Tecnologia:
- Node.js

---

## Banco de Dados
Responsável pelo armazenamento das informações.

Tecnologia:
- MySQL

---

# 🔐 Segurança do Sistema

O projeto utiliza princípios de segurança baseados em Saltzer & Schroeder.

## Medidas Aplicadas

- Criptografia de senhas
- Controle de acesso
- Autenticação segura
- Proteção de dados sensíveis
- Validação de informações

---

# 📈 Escalabilidade

O sistema foi pensado para suportar:

- Grande número de usuários simultâneos
- Alto volume de pedidos
- Expansão futura da plataforma

## Estratégias

- Modularização
- Banco de dados escalável
- Separação entre front-end e back-end

---

# 🛠️ Metodologia Utilizada

## Scrum

O desenvolvimento foi organizado utilizando:

- Sprints de 2 semanas
- Planejamento incremental
- Kanban
- Controle de tarefas pelo GitHub Projects

---

# 📂 Estrutura Relacionada ao Design

```bash
FoodConnect/
│
├── Design.md
├── Diagrama.png
└── src/
```

---

# ✅ Conclusão

O FoodConnect demonstra a aplicação prática do pensamento computacional na construção de sistemas modernos de larga escala, utilizando decomposição, abstração, reconhecimento de padrões e algoritmos para resolver problemas reais de forma organizada e eficiente.
