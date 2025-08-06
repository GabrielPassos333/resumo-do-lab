# 💻 Laboratório Prático: Criação de Máquinas Virtuais no Azure

## Descrição do Desafio

Este laboratório tem como objetivo consolidar seus conhecimentos em máquinas virtuais da Azure. Ao seguir este guia, você irá criar, configurar e acessar sua primeira Máquina Virtual (VM) com Windows no portal do Azure.

---

### 🎯 Objetivos de Aprendizagem

- Navegar no portal do Azure para encontrar e criar recursos.
- Entender e configurar os componentes essenciais de uma VM:
    - Grupo de Recursos.
    - Imagem do Sistema Operacional.
    - Tamanho (poder de computação).
    - Rede Virtual e Portas de Entrada (RDP).
- Conectar-se a uma VM Windows remotamente.
- Excluir os recursos para evitar custos inesperados.

### ✅ Pré-requisitos

- Uma **assinatura do Azure ativa**. Se você não tiver uma, pode criar uma que oferece créditos para começar.

---

## 🚀 Passo a Passo: Criando sua VM Windows no Portal

### 1. Login e Acesso ao Portal
Acesse o **[Portal do Azure](https://portal.azure.com)** e faça login com sua conta.

### 2. Criar um Novo Recurso
1. Na barra de busca do portal, digite **`máquinas virtuais`** e selecione o serviço correspondente.
2. Na página de Máquinas Virtuais, clique em **`+ Criar`** e selecione **`Máquina virtual do Azure`**.


### 3. Configuração da Aba "Básico"
Esta é a etapa mais importante. Preencha os seguintes campos:

- **Assinatura**: Selecione sua assinatura do Azure.
- **Grupo de Recursos**: Clique em **`Criar novo`**, dê um nome (ex: `lab-vm-recursos`) e clique em `OK`.
- **Nome da máquina virtual**: Escolha um nome único para sua VM (ex: `MinhaVMWindows`).
- **Região**: Escolha a região mais próxima de você para menor latência (ex: `(US) East US` ou `(South America) Brazil South`).
- **Imagem**: Selecione **`Windows Server 2022 Datacenter: Azure Edition - x64 Gen2`**.
- **Tamanho**: O Azure sugere um tamanho padrão. Para este laboratório, o tamanho `Standard_B2s` (geralmente incluído no nível gratuito) é suficiente.
- **Conta de administrador**:
    - **Nome de usuário**: Crie um nome de usuário (ex: `adminuser`).
    - **Senha**: Crie uma senha forte e **anote-a em um local seguro**, pois você precisará dela para se conectar à VM.
- **Regras de porta de entrada**:
    - Marque a opção **`Permitir portas selecionadas`**.
    - Selecione **`RDP (3389)`** na lista. Isso abrirá a porta necessária para a conexão remota.

### 4. Revisar e Criar a VM
1. Você pode navegar pelas outras abas (`Discos`, `Rede`, etc.) para ver as configurações padrão, mas para este laboratório básico, elas não precisam ser alteradas.
2. Clique no botão **`Revisar + criar`** na parte inferior da tela.
3. O Azure validará suas configurações. Se tudo estiver correto, uma mensagem "Validação aprovada" aparecerá.
4. Revise o resumo e clique em **`Criar`**.

A implantação começará e levará alguns minutos. Você pode acompanhar o progresso na área de notificações (o ícone de sino 🔔).

### 5. Conectando-se à Máquina Virtual
1. Após a conclusão da implantação, clique em **`Ir para o recurso`**.
2. Na página da sua nova VM, clique em **`Conectar`** e selecione **`RDP`**.
3. O Azure mostrará o endereço IP público e a porta (3389). Clique em **`Baixar Arquivo RDP`**.
4. Abra o arquivo `.rdp` que você baixou.
5. Clique em **`Conectar`** e, quando solicitado, insira o **nome de usuário** e a **senha** que você criou na etapa 3.
6. Você pode receber um aviso de certificado. Marque a caixa e clique em **`Sim`** para prosseguir.

Pronto! A área de trabalho remota da sua VM Windows Server será aberta.

### 6. 🧹 Limpando os Recursos 
Para evitar cobranças contínuas, é crucial excluir os recursos que você criou quando não precisar mais deles.

1. No portal do Azure, procure por **`Grupos de recursos`**.
2. Selecione o grupo de recursos que você criou (ex: `lab-vm-recursos`).
3. Na página do grupo de recursos, clique em **`Excluir grupo de recursos`**.
4. Digite o nome do grupo de recursos para confirmar a exclusão e clique em **`Excluir`**.

> **Aviso:** Esta ação é irreversível e excluirá **TODOS** os recursos dentro do grupo, incluindo a VM, a rede e o disco.

---
