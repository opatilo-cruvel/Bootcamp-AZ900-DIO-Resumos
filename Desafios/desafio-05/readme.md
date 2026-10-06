# AZ-900 — Máquinas Virtuais: Dimensionamento e Disponibilidade

## 1. Criando uma Máquina Virtual

No **Portal do Azure**:

**Máquinas virtuais → Criar → Máquina virtual do Azure**

Durante a criação, configuramos:

* **Subscription:** assinatura que pagará pelos recursos.
* **Resource Group:** grupo que organiza os recursos.
* **Region:** região onde a VM será hospedada.
* **Image:** sistema operacional, como Windows ou Linux.
* **Size:** quantidade de CPU, memória e capacidade de processamento.
* **Availability:** opções de disponibilidade.
* **Disks:** armazenamento da VM.
* **Networking:** VNet, Subnet, IP e NSG.
* **Management:** opções de gerenciamento.
* **Monitoring:** monitoramento da VM.

---

# 2. Dimensionamento

O **tamanho (Size/SKU)** da VM determina seus recursos, como:

* vCPUs
* Memória RAM
* Desempenho de rede
* Desempenho de armazenamento

A escolha depende da carga de trabalho.

### Scale Up / Scale Down

Alterar o tamanho da mesma VM.

```text
Scale Up
2 vCPU → 4 vCPU

Scale Down
8 vCPU → 4 vCPU
```

É chamado de **dimensionamento vertical**.

No Portal:

**VM → Disponibilidade + escala → Tamanho**

> O redimensionamento pode exigir reinicialização ou desalocação da VM.

---

# 3. Dimensionamento Horizontal

Em vez de aumentar uma VM, podemos aumentar a quantidade de VMs.

### Scale Out

```text
VM1 → VM1 + VM2 + VM3
```

### Scale In

```text
VM1 + VM2 + VM3 → VM1 + VM2
```

É chamado de **dimensionamento horizontal**.

Para isso, podemos utilizar **Virtual Machine Scale Sets (VMSS)**.

---

# 4. Autoscale

O **Autoscale** permite aumentar ou diminuir automaticamente a quantidade de VMs conforme a demanda.

Exemplo:

```text
CPU > 70%
    ↓
Adicionar VM
```

Quando a demanda diminui:

```text
CPU < 30%
    ↓
Remover VM
```

Assim, a aplicação consegue acompanhar a demanda sem manter recursos excessivos funcionando o tempo todo.

---

# 5. Disponibilidade

**Dimensionamento** responde:

> "Preciso de mais recursos?"

**Disponibilidade** responde:

> "Como mantenho a aplicação funcionando durante uma falha?"

Os principais conceitos são:

* Availability Zones
* Availability Sets
* VM Scale Sets
* Load Balancer

---

## Availability Zones

São zonas físicas separadas dentro de uma região do Azure.

```text
Região
├── Zona 1 → VM1
├── Zona 2 → VM2
└── Zona 3 → VM3
```

Se uma zona apresentar problema, as outras podem continuar funcionando.

**Para lembrar:**

> Availability Zone = separação física para aumentar a disponibilidade.

---

## Availability Sets

Organizam VMs utilizando:

* **Fault Domains:** reduzem o impacto de falhas de infraestrutura.
* **Update Domains:** distribuem operações de manutenção.

**Para lembrar:**

> Availability Set = Fault Domains + Update Domains.

---

# 6. Disco

As VMs utilizam principalmente **Managed Disks**.

### OS Disk

Contém o sistema operacional.

### Data Disk

Armazena dados da aplicação.

Exemplo:

```text
VM
├── OS Disk → Sistema operacional
└── Data Disk → Dados
```

Tipos comuns:

* Standard HDD
* Standard SSD
* Premium SSD
* Ultra Disk

A escolha depende de **custo e desempenho**.

---

# 7. Rede

Uma VM normalmente utiliza:

```text
VM
 ↓
NIC
 ↓
Subnet
 ↓
VNet
```

### VNet

Rede virtual do Azure.

### Subnet

Divide a VNet em redes menores.

### NIC

Conecta a VM à rede.

### IP

Pode ser privado ou público.

### NSG

**Network Security Group** controla o tráfego através de regras.

Exemplo:

```text
Porta 80  → Permitida
Porta 443 → Permitida
Porta 22  → Bloqueada
```

---

# 8. Gerenciamento

Depois de criar a VM, podemos:

* Iniciar
* Parar
* Reiniciar
* Redimensionar
* Adicionar discos
* Configurar rede
* Conectar à VM
* Configurar segurança
* Configurar monitoramento

---

# 9. Monitoramento

O **Azure Monitor** acompanha a saúde e o desempenho dos recursos.

Podemos monitorar:

* CPU
* Disco
* Rede
* Disponibilidade
* Logs
* Métricas

Também podemos criar **Alertas**.

Exemplo:

```text
CPU > 80%
    ↓
Azure Monitor
    ↓
Alerta
```

---

# 10. Resumo para a prova

| Conceito              | Lembre-se                    |
| --------------------- | ---------------------------- |
| **VM Size**           | Define CPU, RAM e desempenho |
| **Scale Up**          | VM maior                     |
| **Scale Down**        | VM menor                     |
| **Scale Out**         | Mais VMs                     |
| **Scale In**          | Menos VMs                    |
| **VMSS**              | Grupo de VMs                 |
| **Autoscale**         | Escala automaticamente       |
| **Availability Zone** | Zonas físicas separadas      |
| **Availability Set**  | Fault + Update Domains       |
| **Load Balancer**     | Distribui tráfego            |
| **OS Disk**           | Sistema operacional          |
| **Data Disk**         | Dados                        |
| **VNet**              | Rede virtual                 |
| **Subnet**            | Divisão da VNet              |
| **NIC**               | Conecta VM à rede            |
| **NSG**               | Controla tráfego             |
| **Azure Monitor**     | Monitoramento e alertas      |

## 🧠 O mais importante

```text
DIMENSIONAMENTO

Vertical:
Scale Up / Scale Down
→ muda o tamanho da VM

Horizontal:
Scale Out / Scale In
→ muda a quantidade de VMs


DISPONIBILIDADE

Availability Zone
→ separa recursos fisicamente

Availability Set
→ Fault Domains + Update Domains


MONITORAMENTO

Azure Monitor
→ métricas + logs + alertas
```
