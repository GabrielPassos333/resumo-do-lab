# 💾 Laboratório Prático: Configurando um Banco de Dados no Azure

## Descrição do Desafio

Este laboratório tem como objetivo praticar o processo de configuração de uma instância de Banco de Dados na plataforma Microsoft Azure. Como entregável, o desafio proposto é a criação de um repositório contendo resumos, anotações e dicas sobre o uso da Azure, servindo como material de apoio para estudos e futuras implementações.

---

### 🎯 Objetivos de Aprendizagem

- Entender as principais opções de serviços de banco de dados no Azure.
- Provisionar uma instância do **Banco de Dados SQL do Azure**.
- Criar e configurar um **servidor SQL lógico**.
- Configurar **regras de firewall** para permitir o acesso seguro.
- Obter a **cadeia de conexão** (connection string) para conectar aplicações.
- Praticar o gerenciamento de recursos e a limpeza do ambiente.

### ✅ Pré-requisitos

- Uma **assinatura do Azure ativa**. Se você não tiver uma, pode criar uma **Conta Gratuita do Azure**.

---

## 🚀 Passo a Passo: Criando seu Banco de Dados SQL

### Passo 1: Criar o Recurso "Banco de Dados SQL"

1. Faça login no **Portal do Azure**.
2. Na barra de busca, digite **`Banco de Dados SQL`** e selecione o serviço na lista.
3. Na página de Bancos de Dados SQL, clique em **`+ Criar`**.

### Passo 2: Configurar as Informações Básicas

Você será direcionado para a tela de criação. Preencha os campos na aba **"Básico"**:

- **Grupo de Recursos**: Crie um novo grupo para organizar os recursos deste laboratório. Ex: `lab-database-rg`.
- **Nome do Banco de Dados**: Escolha um nome para o seu banco. Ex: `MeuPrimeiroDB`.

#### Criando o Servidor SQL Lógico
O seu banco de dados precisa ser hospedado em um servidor lógico.

- **Servidor**: Clique em **`Criar novo`**.
- **Nome do servidor**: Escolha um nome **globalmente único** (ex: `meuservidor-sql-2025`). O Azure informará se o nome está disponível.
- **Localização**: Escolha a mesma região dos seus outros recursos ou a mais próxima de você.
- **Autenticação**: Mantenha **`Usar autenticação SQL`**.
- **Logon de administrador do servidor**: Crie um nome de usuário (ex: `sqladmin`).
- **Senha**: Crie uma senha forte e **ANOTE-A EM UM LOCAL SEGURO**. Você precisará dela para se conectar.
- Clique em **`OK`** para confirmar a criação do servidor.

- **Computação + armazenamento**: Para um laboratório, clique em **`Configurar banco de dados`** e escolha um nível de baixo custo, como **Básico** ou **Serverless (Sem Servidor)**, para evitar custos altos.

Após preencher tudo, clique em **`Avançar: Rede`**.

### Passo 3: Configurar a Rede (Firewall)

Esta é uma etapa **CRÍTICA** para conseguir se conectar ao banco de dados.

1.  **Método de conectividade**: Selecione **`Ponto de extremidade público`**.
2.  **Permitir que os serviços e recursos do Azure acessem este servidor**: Marque **`Sim`**. Isso é útil se você tiver uma aplicação rodando no Azure que precise se conectar ao DB.
3.  **Adicionar endereço IP do cliente atual**: Marque **`Sim`**. Isso cria uma regra no firewall que permite que o seu computador atual se conecte ao banco de dados.

Clique em **`Revisar + criar`**, verifique o resumo e, em seguida, clique em **`Criar`**. A implantação levará alguns minutos.

### Passo 4: Obter a Cadeia de Conexão

1.  Quando a implantação terminar, clique em **`Ir para o recurso`**.
2.  No menu esquerdo da página do seu banco de dados, procure por **`Cadeias de conexão`** (em "Configurações").
3.  Aqui você encontrará as cadeias de conexão para diversas linguagens de programação (`ADO.NET`, `JDBC`, `PHP`, etc.). Copie a que for relevante para você, **lembrando de substituir `{your_password}` pela senha que você criou**.

### Passo 5: 🧹 Limpeza de Recursos

Para não gerar custos desnecessários, lembre-se de excluir os recursos após o término do laboratório.

1.  Vá para a página do **Grupo de Recursos** que você criou (`lab-database-rg`).
2.  Clique em **`Excluir grupo de recursos`**.
3.  Digite o nome do grupo de recursos para confirmar e clique em **`Excluir`**.

> ⚠️ **Aviso:** Esta ação é permanente e excluirá **TODOS** os recursos contidos no grupo, incluindo o servidor e o banco de dados.
