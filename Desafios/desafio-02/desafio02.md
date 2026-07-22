# Desafio de Projeto - Criando uma Máquina Virtual na Microsoft Azure

---

# Objetivos

- Compreender os benefícios da computação em nuvem.
- Entender os conceitos de disponibilidade, escalabilidade e elasticidade.
- Conhecer os recursos de segurança e governança da Azure.
- Criar uma Máquina Virtual utilizando o Portal da Microsoft Azure.
- Documentar o processo de aprendizado.

---

# Benefícios da Computação em Nuvem

## 1. Alta Disponibilidade

Alta disponibilidade é a capacidade de um sistema permanecer operacional mesmo quando ocorre alguma falha de infraestrutura.

Na Azure, a Microsoft projeta seus serviços para minimizar interrupções. Caso um servidor apresente falha, outro poderá assumir sua função. Da mesma forma, dependendo da arquitetura utilizada, aplicações podem continuar funcionando mesmo que um datacenter inteiro fique indisponível.

### SLA (Service Level Agreement)

O SLA é o compromisso da Microsoft em relação ao tempo de disponibilidade de um serviço durante um determinado período (geralmente mensal).

Alguns exemplos são:

- 99%
- 99,9%
- 99,95%
- 99,99%
- 99,999%

Quanto maior o SLA, menor será o tempo máximo esperado de indisponibilidade.

### Relação entre Alta Disponibilidade e SLA

A alta disponibilidade é justamente o que permite que a Microsoft ofereça SLAs elevados.

Por exemplo:

**Cenário 1**

- Apenas uma Máquina Virtual.

Caso essa VM apresente problemas, a aplicação ficará indisponível.

**Cenário 2**

- Duas Máquinas Virtuais;
- Distribuídas em diferentes Zonas de Disponibilidade;
- Atrás de um Azure Load Balancer.

Se uma VM falhar, a outra continuará atendendo os usuários, reduzindo significativamente o risco de indisponibilidade e aumentando o SLA da solução.

---

## 2. Escalabilidade

Escalabilidade é a capacidade de aumentar ou reduzir recursos conforme a demanda da aplicação.

Na Azure, é possível aumentar recursos como:

- CPU
- Memória RAM
- Armazenamento

Uma dúvida comum é:

> O custo aumenta ao adicionar recursos?

Sim, porém o modelo da computação em nuvem é baseado em consumo.

Isso significa que:

- paga-se apenas pelos recursos utilizados;
- quando a demanda diminui, é possível reduzir os recursos e, consequentemente, reduzir os custos.

### Escala Vertical

Consiste em aumentar a capacidade da própria máquina virtual.

Exemplo:

- aumentar de 2 para 4 vCPUs;
- aumentar a memória RAM de 8 GB para 16 GB.

---

## 3. Elasticidade

Elasticidade é a capacidade de expandir ou reduzir recursos automaticamente (ou manualmente), acompanhando as oscilações de demanda.

Exemplo:

Durante uma promoção de uma loja virtual, a quantidade de acessos aumenta rapidamente.

A Azure pode criar novas máquinas virtuais automaticamente para atender esse aumento.

Quando o volume de acessos diminuir, essas instâncias extras poderão ser removidas, reduzindo custos.

---

## 4. Confiabilidade

A Azure possui uma infraestrutura distribuída mundialmente.

Isso significa que aplicações podem ser implantadas em diversas regiões geográficas.

Mesmo que uma região inteira fique indisponível por algum desastre natural ou falha crítica, outras regiões poderão continuar operando normalmente, garantindo maior resiliência.

---

## 5. Previsibilidade

A previsibilidade permite estimar tanto o desempenho quanto os custos da solução.

Esse benefício é baseado nas boas práticas do **Microsoft Azure Well-Architected Framework**, permitindo construir ambientes mais eficientes, seguros e econômicos.

---

## 6. Segurança

A Azure disponibiliza diversos recursos para proteção dos ambientes.

Entretanto, a responsabilidade pela segurança depende do modelo de serviço utilizado.

### Infraestrutura como Serviço (IaaS)

O cliente é responsável por:

- sistema operacional;
- atualizações;
- aplicação de patches;
- softwares instalados.

### Plataforma como Serviço (PaaS)

Grande parte das atualizações e manutenção são realizadas automaticamente pela Microsoft.

---

## 7. Governança

Governança consiste em garantir que os recursos da nuvem estejam em conformidade com as políticas da organização.

Entre os principais benefícios estão:

- auditorias automáticas;
- identificação de recursos fora de conformidade;
- aplicação automática de políticas;
- atualizações e patches automatizados.

Uma boa estratégia de governança torna o ambiente mais seguro, organizado e fácil de administrar.

---

## 8. Gerenciabilidade

A Azure oferece diversas formas de gerenciamento dos recursos.

### Gerenciamento da nuvem

Relaciona-se à administração dos próprios recursos.

Exemplos:

- escalabilidade automática;
- implantação através de templates;
- automação de recursos.

### Gerenciamento na nuvem

Refere-se às ferramentas utilizadas para administrar o ambiente.

Entre elas:

- Portal do Azure;
- Azure CLI;
- Azure PowerShell;
- APIs REST.

---

# Criando uma Máquina Virtual na Azure

Para este desafio foi utilizado o Portal da Microsoft Azure seguindo a documentação oficial.

Documentação utilizada:

https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal

## Etapas realizadas

1. Acessar o Portal da Azure.
2. Criar um novo Grupo de Recursos.
3. Selecionar **Máquina Virtual**.
4. Informar:
   - Nome da VM;
   - Região;
   - Imagem do sistema operacional;
   - Tamanho da máquina.
5. Criar usuário e senha de administrador.
6. Liberar a porta RDP (3389) para acesso remoto.
7. Revisar as configurações.
8. Criar a Máquina Virtual.
9. Aguardar a implantação.
10. Conectar-se à VM utilizando Área de Trabalho Remota (Remote Desktop).

---

# O que aprendi

Durante este desafio foi possível compreender que uma Máquina Virtual na Azure vai muito além da simples criação de um servidor.

Foi possível entender como os benefícios da computação em nuvem impactam diretamente na construção de aplicações modernas, destacando conceitos como:

- Alta disponibilidade;
- SLA;
- Escalabilidade;
- Elasticidade;
- Confiabilidade;
- Segurança;
- Governança;
- Gerenciabilidade.

Além disso, a utilização do Portal da Azure permitiu conhecer o fluxo de criação e gerenciamento de uma Máquina Virtual de forma prática.

---

# Conclusão

A criação de uma Máquina Virtual na Microsoft Azure demonstrou como a computação em nuvem facilita o provisionamento de infraestrutura de maneira rápida, escalável e segura.

O estudo dos benefícios da nuvem complementou a prática, permitindo compreender como recursos como alta disponibilidade, elasticidade e governança contribuem para o desenvolvimento de soluções resilientes e preparadas para diferentes cenários de utilização.

---

# Referências

- Microsoft Learn – Criar uma Máquina Virtual no Azure  
  https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal

- Microsoft Learn – Conceitos Fundamentais da Microsoft Azure  
  https://learn.microsoft.com/pt-br/training/paths/microsoft-azure-fundamentals-describe-cloud-concepts/
