# 🌐 Configuração de Serviços (HTTP/DNS) e Análise de Protocolos

Neste laboratório prático, construi uma rede funcional do zero para configurar serviços de aplicação e analisar o comportamento dos protocolos na camada de transporte. 

---

## 🛠️ O que eu usei
* **Simulador:** Cisco Packet Tracer
* **1 Servidor Central** (atuando como Web Server e DNS Server)
* **1 Switch Cisco 2960**
* **1 PC-Cliente** (End Device)

## ⚙️ O que eu fiz
A arquitetura foi montada conectando o PC e o Servidor ao Switch utilizando cabeamento direto. Após a montagem física, executei as seguintes configurações:

1. **Endereçamento IP Estático:** 
   * Configurei o Servidor com o IP `192.168.1.10`.
   * Configurei o PC-Cliente com o IP `192.168.1.5` e apontei o seu Servidor DNS para o IP do Servidor Central.
2. **Configuração do Servidor Web (HTTP):** Acessei a aba de serviços do Servidor, garanti a ativação do HTTP/HTTPS e editei o código do arquivo `index.html`. Personalizei a página web com a mensagem: *"Bem-vinda à aula de Redes! Esta é a nossa primeira página web configurada e testada no laboratório!"*.
3. **Configuração do DNS:** No mesmo servidor, ativei o serviço DNS e criei um registro mapeando o domínio amigável `www.aula.com` para o endereço IP `192.168.1.10`.

## 🚀 Validação e Análise de Tráfego
Para comprovar o funcionamento da rede e dos serviços, realizei duas fases de testes:

* **Testes no Prompt de Comando:** 
  * Executei o comando `ping 192.168.1.10` para confirmar a conectividade de rede (ICMP), obtendo respostas com 0% de perda.
  * Executei o `nslookup www.aula.com` para garantir que o serviço de resolução de nomes estava traduzindo o domínio corretamente para o IP do servidor.
* **Análise de Camadas (Modo Simulação):** 
  * Acessei o navegador web do PC-Cliente e acessei a URL `www.aula.com`. 
  * Utilizando o modo de simulação do Packet Tracer (filtrando apenas os protocolos DNS, TCP, HTTP e ICMP), capturei os pacotes trafegando pela rede.
  * Inspecionei as informações das PDUs (Protocol Data Units), observando na prática as mudanças e o encapsulamento de cabeçalhos ocorrendo nas **Camadas 4 (Transporte)** e **7 (Aplicação)**.

---
### 📸 
<img width="959" height="503" alt="lab28 07" src="https://github.com/user-attachments/assets/f10575cb-fb93-4fc2-ab96-148003dec9a2" />
