# ✅ Projeto_Corrigido.md – FoodConnect

## 📖 Introdução

Após a identificação dos erros presentes no projeto FoodConnect, foram realizadas correções para melhorar a segurança, funcionamento, clareza e organização do sistema.

Este documento apresenta as alterações realizadas e suas respectivas justificativas.

---

# 🔧 1. Correção no Sistema de Login

## ❌ Problema Encontrado
O login era realizado mesmo com os campos vazios.

## ✅ Correção Aplicada
Foi adicionada validação para verificar se usuário e senha foram preenchidos corretamente.

## Código Corrigido

```javascript
let usuarioLogado = false;

function login() {

  const usuario = document.getElementById("usuario").value;
  const senha = document.getElementById("senha").value;

  if (usuario === "" || senha === "") {
    alert("Preencha usuário e senha!");
    return;
  }

  usuarioLogado = true;

  alert("Login realizado com sucesso!");
}
```

## ✔ Justificativa
A validação impede acessos inválidos e melhora a segurança do sistema.

---

# 🛒 2. Correção na Realização de Pedidos

## ❌ Problema Encontrado
Pedidos podiam ser realizados sem login.

## ✅ Correção Aplicada
Foi criada verificação de autenticação antes da criação do pedido.

## Código Corrigido

```javascript
let pedidoRealizado = false;

function pedido() {

  if (!usuarioLogado) {
    alert("Faça login antes de realizar um pedido.");
    return;
  }

  pedidoRealizado = true;

  document.getElementById("status").innerText =
    "Pedido realizado! Restaurante preparando...";
}
```

## ✔ Justificativa
Garantir que apenas usuários autenticados possam utilizar o sistema.

---

# 🚴 3. Correção no Rastreamento

## ❌ Problema Encontrado
O sistema permitia rastrear pedidos inexistentes.

## ✅ Correção Aplicada
Foi adicionada verificação para garantir que exista um pedido ativo.

## Código Corrigido

```javascript
function rastrear() {

  if (!pedidoRealizado) {
    alert("Realize um pedido antes de rastrear.");
    return;
  }

  document.getElementById("status").innerText =
    "Entregador saiu para entrega 🚴";
}
```

## ✔ Justificativa
Evita inconsistências nas informações exibidas ao usuário.

---

# 🌐 4. Correção do Backend

## ❌ Problema Encontrado
Rotas inválidas não eram tratadas pelo servidor.

## ✅ Correção Aplicada
Foi criado tratamento de erro para páginas inexistentes.

## Código Corrigido

```javascript
app.use((req, res) => {

  res.status(404).json({
    erro: "Rota não encontrada"
  });

});
```

## ✔ Justificativa
Melhora a estabilidade do sistema e evita falhas inesperadas.

---

# 🗄️ 5. Correção do Banco de Dados

## ❌ Problema Encontrado
Os campos do banco aceitavam valores nulos.

## ✅ Correção Aplicada
Foram adicionadas restrições `NOT NULL`.

## Código Corrigido

```sql
CREATE TABLE usuarios (

    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL,
    email VARCHAR(100) NOT NULL,
    senha VARCHAR(100) NOT NULL

);
```

## ✔ Justificativa
Impede o armazenamento de dados incompletos.

---

# 🎨 6. Correção da Interface

## ❌ Problema Encontrado
A interface não era totalmente responsiva.

## ✅ Correção Aplicada
Foi utilizado `flex-wrap` e ajustes de layout.

## Código Corrigido

```css
main {
  display: flex;
  justify-content: center;
  gap: 20px;
  flex-wrap: wrap;
}
```

## ✔ Justificativa
Melhora a visualização em dispositivos móveis.

---

# 🔒 7. Melhoria na Segurança

## ❌ Problema Encontrado
As senhas eram armazenadas sem proteção.

## ✅ Correção Aplicada
Foi planejada a utilização de criptografia de senhas no backend.

## Exemplo

```javascript
const bcrypt = require('bcrypt');
```

## ✔ Justificativa
Aumenta a proteção dos dados dos usuários.

---

# 📊 Resultado das Correções

| Área | Situação Antes | Situação Depois |
|------|----------------|----------------|
| Login | Sem validação | Validado |
| Pedidos | Sem autenticação | Protegido |
| Rastreamento | Sem controle | Verificado |
| Backend | Sem tratamento | Tratamento 404 |
| Banco de Dados | Campos nulos | Campos obrigatórios |
| Interface | Pouco responsiva | Responsiva |
| Segurança | Vulnerável | Mais protegida |

---

# ✅ Resultado Final

Após as correções:

- O sistema ficou mais seguro.
- O fluxo de funcionamento ficou mais organizado.
- Os erros de execução foram reduzidos.
- A experiência do usuário foi melhorada.
- O projeto ficou mais preparado para crescimento futuro.

---

# 🧠 Conclusão

O tratamento de erros permitiu melhorar significativamente o projeto FoodConnect.

As correções aplicadas demonstram a importância da validação, organização e segurança no desenvolvimento de sistemas modernos.
