# 🌐 Configuração de Servidor DHCP em Roteador Cisco

Neste projeto prático, configurei um roteador Cisco para atuar como servidor DHCP. O objetivo principal foi automatizar a distribuição de IPs, Máscara de Sub-rede, Gateway Padrão e Servidor DNS para os computadores de uma rede local. 

Esta atividade faz parte do meu portfólio de infraestrutura e redes, construído durante minha jornada no programa **Mulher Digital**, e serve como base para a minha graduação e carreira em **Segurança da Informação**.

## 🛠️ O que eu usei
* **Cisco Packet Tracer** para a simulação da infraestrutura.
* **1 Roteador Cisco 2911** (atuando como Gateway e Servidor DHCP).
* **1 Switch Cisco 2960** para a distribuição das conexões locais.
* **2 PCs** (End Devices) simulando os clientes.

## ⚙️ O que eu fiz
Primeiro, montei a topologia interligando os equipamentos com cabo direto. Em seguida, acessei a interface de linha de comando (CLI) do roteador e executei as seguintes etapas:

1. **Configuração da Interface (Gateway):** Acessei a porta `GigabitEthernet0/0`, defini o endereço IP `192.168.1.1` com a máscara `255.255.255.0` e ativei a interface (`no shutdown`).
2. **Criação do Pool DHCP:** Configurei o pool nomeado `MULHER_DIGITAL2026`.
3. **Definição dos Parâmetros:** Declarei a rede local (`192.168.1.0/24`), defini o default gateway apontando para o roteador (`192.168.1.1`) e configurei o DNS público (`8.8.8.8`).
4. **Gravação:** Salvei todas as configurações na memória do equipamento para que não fossem perdidas ao reiniciar (`write`).

## 🚀 Validação e Resultados
Para comprovar o funcionamento, acessei as configurações de rede dos dois PCs no simulador e alterei o método de atribuição de "Estático" para "DHCP". 

Ambos enviaram a requisição à rede e, em poucos segundos, foram atualizados automaticamente pelo roteador, recebendo os IPs `192.168.1.2` e `192.168.1.3`, confirmando que o servidor DHCP estava operando perfeitamente.

> 🎥 **Confira a foto demonstrativa da atividade:** 
<img width="959" height="502" alt="Captura de tela 2026-08-23 234314" src="https://github.com/user-attachments/assets/89c9a151-a336-4644-9973-720d53708388" />
