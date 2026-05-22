# 🐞 Erros_Identificados.md – FoodConnect

## 📖 Introdução

Durante o desenvolvimento do projeto FoodConnect foram identificados erros de lógica, execução e validação que poderiam comprometer o funcionamento correto do sistema.

Este documento registra os principais problemas encontrados no projeto antes das correções.

---

# 🔥 1. Login sem Validação

## Problema
O sistema permitia que o usuário realizasse login mesmo deixando os campos vazios.

## Tipo de Erro
- Lógica
- Validação

## Impacto
Usuários poderiam acessar funcionalidades do sistema sem autenticação adequada.

## Trecho Problemático

```javascript
function login() {
  alert("Login realizado com sucesso!");
}
```

---

# 🛒 2. Pedido sem Usuário Logado

## Problema
O sistema permitia realizar pedidos sem verificar se o usuário estava autenticado.

## Tipo de Erro
- Lógica

## Impacto
Pedidos poderiam ser criados sem identificação do cliente.

## Trecho Problemático

```javascript
function pedido() {
  document.getElementById("status").innerText =
    "Pedido realizado!";
}
```

---

# 🚴 3. Rastreamento sem Pedido

## Problema
O usuário conseguia rastrear entregas mesmo sem ter realizado um pedido.

## Tipo de Erro
- Execução
- Lógica

## Impacto
O sistema apresentava informações incoerentes.

## Trecho Problemático

```javascript
function rastrear() {
  document.getElementById("status").innerText =
    "Entregador saiu para entrega";
}
```

---

# 🌐 4. Falta de Tratamento de Rotas no Backend

## Problema
O servidor Node.js não tratava rotas inexistentes.

## Tipo de Erro
- Execução

## Impacto
O sistema poderia retornar respostas incorretas ou falhar em acessos inválidos.

## Trecho Problemático

```javascript
app.listen(3000);
```

---

# 🗄️ 5. Campos do Banco sem Restrição

## Problema
Os campos do banco de dados aceitavam valores nulos.

## Tipo de Erro
- Modelagem
- Lógica

## Impacto
Dados incompletos poderiam ser cadastrados no sistema.

## Trecho Problemático

```sql
CREATE TABLE usuarios (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100),
    email VARCHAR(100),
    senha VARCHAR(100)
);
```

---

# ⚠️ 6. Falta de Feedback ao Usuário

## Problema
O sistema não exibia mensagens claras em caso de erro.

## Tipo de Erro
- Usabilidade

## Impacto
O usuário poderia não entender o motivo da falha.

---

# 🎨 7. Interface sem Responsividade

## Problema
A interface apresentava dificuldades em telas menores.

## Tipo de Erro
- Interface
- Layout

## Impacto
Má experiência do usuário em dispositivos móveis.

---

# 🔒 8. Ausência de Proteção de Dados

## Problema
As senhas eram armazenadas sem criptografia.

## Tipo de Erro
- Segurança

## Impacto
Risco de vazamento de dados sensíveis.

---

# 📊 Resumo dos Erros Encontrados

| Nº | Tipo de Erro | Área |
|----|--------------|------|
| 1 | Lógica | Login |
| 2 | Lógica | Pedidos |
| 3 | Execução | Rastreamento |
| 4 | Execução | Backend |
| 5 | Modelagem | Banco de Dados |
| 6 | Usabilidade | Interface |
| 7 | Layout | Front-end |
| 8 | Segurança | Dados |

---

# ✅ Conclusão

A identificação dos erros permitiu compreender falhas importantes no sistema FoodConnect, principalmente relacionadas à validação, segurança e fluxo de execução.

Esses problemas foram posteriormente corrigidos para melhorar a confiabilidade, clareza e eficiência do projeto.
