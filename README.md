# 🛡️ Laboratório de Detecção de Ameaças: Wazuh SIEM + Sysmon

Este projeto demonstra a implementação de um ambiente de monitoramento e detecção de ameaças utilizando **Wazuh (SIEM)** e **Microsoft Sysmon**, simulando um ataque de força bruta via RDP originado a partir do **Kali Linux**.

---

## 🏗️ Arquitetura do Laboratório

* **Wazuh Server & Dashboard:** Centralização e análise de logs.
* **Windows 11 (Vítima/Agente):** Coleta de telemetria detalhada via Agente Wazuh e Sysmon.
* **Kali Linux (Atacante):** Reconhecimento (Nmap) e força bruta (Hydra).

---

## ⚙️ Configuração e Implantação

### 1. Instalação e Configuração do Sysmon
O Sysmon foi instalado no Windows 11 com o arquivo de regras do *SwiftOnSecurity* para capturar eventos de criação de processos e conexões de rede:

```powershell
.\Sysmon64.exe -i sysmonconfig-export.xml

'''

## 📊 Evidências do Laboratório

### 1. Configuração do Agente Wazuh (ossec.conf)
![Configuração Sysmon no Wazuh](ossec-config.png)

### 2. Simulação de Força Bruta RDP (Kali Linux)
![Execução do Hydra](hydra-attack.jpeg)

### 3. Alertas de Detecção em Tempo Real (Wazuh Dashboard)
![Alertas de Segurança](wazuh-alerts.png)
