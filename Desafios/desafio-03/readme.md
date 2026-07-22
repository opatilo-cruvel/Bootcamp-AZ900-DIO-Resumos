# Laboratório - Configuração de uma Instância de Banco de Dados no Microsoft Azure

---

# O que é Azure SQL Managed Instance?

O Azure SQL Managed Instance é um serviço de banco de dados totalmente gerenciado pela Microsoft, compatível com o SQL Server.

Entre suas principais vantagens estão:

- Alta disponibilidade;
- Backups automáticos;
- Atualizações gerenciadas pela Microsoft;
- Escalabilidade sob demanda;
- Segurança integrada;
- Compatibilidade com aplicações que utilizam SQL Server.

---

# Pré-requisitos

Antes da criação da instância é necessário possuir:

- Conta Microsoft Azure;
- Assinatura Azure ativa;
- Permissões para criação de recursos;
- Grupo de Recursos (Resource Group).

---

# Passo a Passo da Configuração

## 1. Acessar o Portal Azure

Entrar no Portal Azure e acessar:

```
Azure SQL
```

Selecionar:

```
SQL Managed Instances
```

Depois clicar em:

```
+ Create
```

---

## 2. Configuração Básica

Preencher as informações obrigatórias:

- Subscription
- Resource Group
- Nome da Instância
- Região
- Método de autenticação
- Usuário Administrador
- Senha

Esses dados serão utilizados para provisionar a instância.

---

## 3. Configurações de Segurança

Nesta etapa podem ser definidos:

- Método de autenticação
- Endpoint público
- Configurações de acesso
- Regras de rede

Para ambientes de produção recomenda-se utilizar autenticação Microsoft Entra ID.

---

## 4. Configurações Adicionais

É possível definir:

- Performance
- Quantidade de vCores
- Armazenamento
- Tipo da Instância
- Tags para organização dos recursos

---

## 5. Revisão

O Azure apresenta um resumo com todas as configurações.

Após validar todas as informações basta selecionar:

```
Create
```

O provisionamento pode levar vários minutos.

---

## 6. Monitoramento

Durante a criação é possível acompanhar o progresso através das notificações do Portal Azure.

Após a conclusão, a instância ficará disponível no Resource Group criado.

---

## 7. Criação do Banco de Dados

Depois da Instância criada:

Selecionar:

```
+ New Database
```

Informar:

- Nome do banco
- Fonte de dados (vazio ou backup)
- Configurações adicionais

Finalizar em:

```
Review + Create
```

---

# Dicas

✔ Utilizar nomes padronizados para os recursos.

✔ Criar Tags para facilitar gerenciamento e custos.

✔ Escolher corretamente a região para reduzir latência.

✔ Evitar liberar acesso público sem necessidade.

✔ Sempre revisar as configurações antes do deploy.


---

# Referências

Microsoft Learn

https://learn.microsoft.com/pt-br/azure/azure-sql/managed-instance/instance-create-quickstart

Documentação Microsoft Azure

https://learn.microsoft.com/pt-br/azure/

GitHub Docs

https://docs.github.com/

