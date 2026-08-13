# Construindo Arquiteturas No Azure

## Desafio de Laboratório

Este laboratório tem como objetivo apresentar os conceitos básicos de gerenciamento de recursos no **Microsoft Azure**, utilizando o Portal do Azure para criar e organizar recursos em um ambiente de nuvem.

Durante o laboratório, foram apresentados exemplos de criação de recursos e grupos de recursos, demonstrando como organizar os componentes de uma arquitetura dentro do Azure.

## 🎯 Objetivo

Aprender a criar um **Grupo de Recursos (Resource Group)** no Portal do Azure e compreender sua importância para a organização e o gerenciamento dos recursos utilizados em uma arquitetura de nuvem.

---

## ☁️ O que é um Grupo de Recursos?

Um **Grupo de Recursos (Resource Group)** é um contêiner utilizado pelo Azure para organizar recursos relacionados a uma determinada solução.

Por exemplo, uma aplicação pode possuir:

- Máquina Virtual;
- Rede Virtual;
- Banco de Dados;
- Endereço IP;
- Conta de Armazenamento.

Todos esses recursos podem ser colocados dentro de um mesmo grupo de recursos, facilitando seu gerenciamento.

> **Importante:** os recursos de um grupo podem ser gerenciados em conjunto, inclusive em relação a permissões, monitoramento e exclusão.

---

## 📋 Pré-requisitos

Para realizar este laboratório, é necessário:

- Possuir uma conta no Microsoft Azure;
- Ter acesso ao [Portal do Azure](https://portal.azure.com/);
- Possuir uma assinatura (**Subscription**) disponível para criação de recursos.

---

# 🚀 Passo a passo — Criando um Grupo de Recursos

## 1. Acessar o Portal do Azure

Primeiramente, acesse o Portal do Azure:

[https://portal.azure.com/](https://portal.azure.com/)

Faça login utilizando sua conta Microsoft.

Após entrar, será apresentada a página inicial do Portal do Azure.

---

## 2. Localizar os Grupos de Recursos

Na barra de pesquisa localizada na parte superior do portal, pesquise por:

**Grupos de recursos**

Selecione a opção **Grupos de recursos** nos resultados apresentados.

---

## 3. Criar um novo Grupo de Recursos

Na página de grupos de recursos, clique no botão:

**+ Criar**

Será aberta uma tela para configurar o novo grupo de recursos.

---

## 4. Selecionar a assinatura

No campo **Assinatura**, selecione a assinatura do Azure que será utilizada para o laboratório.

A assinatura é responsável por associar os recursos criados ao ambiente do Azure e pelo controle de utilização e cobrança.

---

## 5. Definir o nome do Grupo de Recursos

No campo **Grupo de recursos**, informe um nome para identificar o grupo.

Por exemplo:

```text
rg-laboratorio-azure
