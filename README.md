# 🛡️ Mulher Digital - Trilha de Cibersegurança

![Cisco Networking Academy](https://img.shields.io/badge/Cisco_Networking_Academy-00599C?style=for-the-badge&logo=cisco&logoColor=white)
![Status](https://img.shields.io/badge/Status-Em_Andamento-brightgreen?style=for-the-badge)

Repositório dedicado à documentação de atividades, resumos e laboratórios práticos desenvolvidos durante o programa **Mulher Digital (Junior Achievement Brasil)**, com foco em Cibersegurança e Redes.

---

## 📂 Navegação por Laboratórios

### 🌐 01. Redes Hierárquicas (Cisco Packet Tracer)

#### 📌 Objetivo
Compreender e aplicar a divisão de uma rede corporativa nas três camadas do modelo hierárquico (**Acesso**, **Distribuição** e **Núcleo/Core**), realizando a montagem do cabeamento, atribuição de IP e testes de conectividade de ponta a ponta.

#### 🛠️ Dispositivos Utilizados

| Camada | Dispositivo / Modelo | Quantidade | Função |
| :--- | :--- | :---: | :--- |
| **Core (Núcleo)** | Roteador Cisco 4331 | 1 | Roteamento de alta velocidade |
| **Distribuição** | Switch Cisco 3650-24PS | 1 | Agregação de tráfego e políticas |
| **Acesso** | Switch Cisco 2960-24TT | 2 | Conexão final dos PCs |
| **Dispositivos Finais** | PCs | 4 | Hosts da rede |

#### 🔌 Conexões de Redes
* **PC-Lab01** (`Fa0`) ➡️ **SW-Acesso-Lab** (`Fa0/1`)
* **PC-Lab02** (`Fa0`) ➡️ **SW-Acesso-Lab** (`Fa0/2`)
* **PC-Sec01** (`Fa0`) ➡️ **SW-Acesso-Sec** (`Fa0/1`)
* **PC-Sec02** (`Fa0`) ➡️ **SW-Acesso-Sec** (`Fa0/2`)
* **SW-Acesso-Lab** (`Gi0/1`) ➡️ **SW-Distribuição-3650** (`Gi1/0/1`)
* **SW-Acesso-Sec** (`Gi0/1`) ➡️ **SW-Distribuição-3650** (`Gi1/0/2`)
* **SW-Distribuição-3650** (`Gi1/0/24`) ➡️ **Roteador-Core-4331** (`Gi0/0/0`)

#### ⚙️ Configuração do Roteador (CLI)

```bash
Router> enable
Router# configure terminal
Router(config)# interface gigabitEthernet 0/0/0
Router(config-if)# ip address 192.168.1.1 255.255.255.0
Router(config-if)# no shutdown
Router(config-if)# exit
