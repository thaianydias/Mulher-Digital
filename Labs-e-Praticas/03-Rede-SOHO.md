# 🌐 Configuração de Rede SOHO (Small Office/Home Office)

Neste projeto prático, simulei e configurei a infraestrutura de rede de um pequeno escritório (SOHO). O objetivo foi integrar conectividade cabeada e sem fio (Wi-Fi), garantindo a segurança básica da rede e a distribuição automática de endereços IP.

---

## 🛠️ O que eu usei
* **Simulador:** Cisco Packet Tracer
* **Emulação WAN:** 1 Cloud-PT (Nuvem) e 1 Cable Modem
* **Roteador Wireless:** Modelo Cisco WRT300N (Switch, AP e DHCP)
* **Dispositivos Cabeados:** 2 PCs e 1 Impressora de Rede
* **Dispositivos Sem Fio:** 1 Notebook (Laptop) e 1 Smartphone

## ⚙️ O que eu fiz
Construí a rede do zero, passando pela infraestrutura física até a configuração lógica de segurança e serviços. As principais etapas foram:

1. **Cabeamento e WAN:** Conectei a nuvem ao Cable Modem via cabo coaxial e interliguei o modem à porta de Internet do roteador WRT300N utilizando cabo de rede direto. Os dispositivos cabeados (PCs e Impressora) foram conectados às portas Ethernet do roteador.
2. **Configuração da Rede Sem Fio (WLAN):** 
   * Acessei a interface gráfica (GUI) do roteador e alterei o SSID padrão para `Escritorio_Firma`.
   * Para proteger a rede contra acessos não autorizados, implementei o protocolo de segurança **WPA2 Personal** e defini uma senha de acesso.
3. **Adaptação de Hardware (Notebook):** No simulador, acessei as configurações físicas do notebook, desliguei o equipamento virtualmente e substituí a placa de rede FastEthernet nativa por um módulo de rede Wi-Fi (`WPC300N`).
4. **Conexão dos Dispositivos Mobile:** Autentiquei o Smartphone e o Notebook na nova rede Wi-Fi `Escritorio_Firma`, inserindo a chave WPA2 configurada.
5. **Configuração de DHCP:** Acessei as configurações de IP de todos os dispositivos finais (PCs, Impressora, Notebook e Smartphone) e alterei de Estático para DHCP. O roteador WRT300N atribuiu perfeitamente os endereços na faixa `192.168.0.X`.

## 🚀 Validação e Resultados
Para comprovar que todos os equipamentos do escritório estavam se comunicando corretamente, fiz uma validação via linha de comando:
* Abri o *Command Prompt* do PC0 e verifiquei o IP recebido via DHCP usando o comando `ipconfig`.
* Em seguida, disparei um teste de `ping` para o endereço IP atribuído à impressora de rede. 
* O teste retornou respostas positivas com 0% de perda, confirmando que a infraestrutura SOHO foi implantada e validada com sucesso!

> 🎥 **Confira o vídeo demonstrativo da atividade:**
https://github.com/user-attachments/assets/3b465203-e44b-4527-8b9c-0f50830616f6
