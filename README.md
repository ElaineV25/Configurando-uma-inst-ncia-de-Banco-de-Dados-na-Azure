# Configurando uma instância de Banco de Dados na Azure

--

## 🛠️ **Passo a Passo: Criando uma Instância de Banco de Dados no Azure (ex: SQL Database)**

### ✅ **1. Acessar o Portal**

* Vá para: [https://portal.azure.com](https://portal.azure.com)
* No menu lateral, clique em **“Criar um recurso”** > **“Banco de Dados”** > **“SQL Database”**

---

### ✅ **2. Preencher as Informações Básicas**

* **Assinatura** e **Grupo de Recursos** (criar novo ou usar existente)
* **Nome do Banco de Dados**: Ex: `db-vendas-prod`
* **Servidor**: Criar novo ou selecionar um existente

  * Nome do servidor, localização, admin e senha.

---

### ✅ **3. Configurar o Preço e Desempenho**

* Escolha o modelo:

  * **DTU**: simples para cargas pequenas
  * **vCore**: mais controle e escalabilidade
* **Camada**: Basic, Standard, Premium
* **Backup e Redundância**: definir onde e como será armazenado.

---

### ✅ **4. Configurar Rede e Segurança**

* **Método de Conexão**: público ou privado
* **Firewall**: permitir IPs específicos para acesso
* **Autenticação**:

  * SQL (login/senha)
  * Azure AD (opcional, mais seguro)

---

### ✅ **5. Aplicar Tags (opcional, mas recomendado)**

Exemplo:

```bash
Environment: production
Owner: equipe-data
CostCenter: 12345
```

---

### ✅ **6. Revisar e Criar**

* Clique em **"Revisar + Criar"**
* Valide as informações e clique em **"Criar"**

---

### ✅ **7. Acessar o Banco de Dados**

* Ir até o recurso criado
* Copiar a **string de conexão**
* Conectar via SSMS, Azure Data Studio ou aplicação

---

## 📌 **Dicas e Resumos Úteis para Banco de Dados no Azure**

* Sempre **configure alertas de performance e uso** (CPU, DTU).
* Use **auditoria integrada** para saber quem acessa o quê.
* Defina **backups automáticos com retenção**.
* Use **geo-replicação ativa** para alta disponibilidade.
* Para ambientes de teste, use camadas **Basic ou Dev/Test** para economizar.

