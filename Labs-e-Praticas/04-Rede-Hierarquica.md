# 🌐 Configuração e Análise de Redes Hierárquicas Cisco

Neste projeto prático, avancei na complexidade da infraestrutura e implementei uma topologia baseada no modelo hierárquico de 3 camadas da Cisco. 

---

## 🛠️ O que eu usei
* **Simulador:** Cisco Packet Tracer
* **Camada de Núcleo (Core):** 1 Roteador Cisco 4331 (Responsável pelo roteamento de alta velocidade)
* **Camada de Distribuição:** 1 Switch Cisco 3650 (Agregação de tráfego e aplicação de políticas)
* **Camada de Acesso:** Switches Cisco 2950 (Conectividade direta aos hosts finais)
* **Cabeamento:** Cabos Diretos (Straight-Through)
* **Dispositivos Finais:** Computadores (PCs)

## ⚙️ O que eu fiz
Construí a rede focando na separação de responsabilidades para otimizar o desempenho e a segurança:

1. **Topologia Física:** Realizei a montagem do cabeamento estruturado, interligando corretamente os switches de acesso ao switch de distribuição, e este ao roteador do núcleo.
2. **Configuração Base (CLI):** Acessei o Roteador 4331 via terminal e ativei as interfaces de rede (`configure terminal`, `interface`, `ip address`, `no shutdown`), estabelecendo o gateway padrão da rede.
3. **Endereçamento:** Apliquei endereçamento IP fixo nos hosts para garantir a previsibilidade no roteamento e facilitar os testes.

## 🚀 Validação e Resultados
Após a configuração das três camadas, foquei em garantir que o tráfego estivesse operando sem gargalos ou falhas de rota:

* **Conectividade Fim-a-Fim:** Executei testes de `ping` (ICMP) entre os dispositivos da camada de acesso, validando que os pacotes conseguiam transitar perfeitamente até o Core e retornar.
* **Análise de Tráfego:** Utilizei o modo de simulação do Packet Tracer para dissecar os pacotes PDU, observando na prática como os dados se movem e são tratados em cada camada do modelo.

---
### 📸 
<div align="center">
  <img width="1600" height="839" alt="1786539636895" src="https://github.com/user-attachments/assets/1fd0022e-eff0-4f59-a458-ae0389b39e8a" />
 
