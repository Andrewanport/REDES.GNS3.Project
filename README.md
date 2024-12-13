# 📡 Projeto de Redes de Computadores no GNS3

Este projeto foi desenvolvido para a disciplina de **Redes de Computadores** com o objetivo de criar e configurar uma rede segmentada utilizando o simulador **GNS3**. A rede apresenta duas sub-redes (LANs) conectadas por um roteador, simulando um ambiente prático de comunicação e roteamento interno.

---

## 📑 Informações Gerais

- **Curso**: Sistemas para Internet  
- **Disciplina**: Redes de Computadores  
- **Semestre**: 2024.2  

---

## 📋 Estrutura e Topologia da Rede

### 🖧 Componentes Principais
- **Roteador**: Conecta e roteia o tráfego entre as duas LANs.
- **Switches**: Um switch por LAN, interligando os computadores.
- **Computadores**:
  - **LAN 1 (192.168.0.0/24)**: André, Keven, Breno
  - **LAN 2 (10.0.0.0/24)**: Lua, Pedro, Felipe

### 🌐 Endereçamento IP
- **LAN 1**:
  - Faixa de IP: `192.168.0.x`
  - Máscara: `255.255.255.0` (/24)
  - Gateway: `192.168.0.254`
- **LAN 2**:
  - Faixa de IP: `10.0.0.x`
  - Máscara: `255.255.255.0` (/24)
  - Gateway: `10.0.0.254`

---

## 🛠️ Configurações

### 📶 Configuração do Roteador
```bash
enable
configure terminal
# Interface conectada à LAN 1
interface FastEthernet0/0
ip address 192.168.0.254 255.255.255.0
no shutdown
# Interface conectada à LAN 2
interface FastEthernet1/0
ip address 10.0.0.254 255.255.255.0
no shutdown
# Ativar roteamento
ip routing
end
```

### 🖥️ Configurações dos Computadores
- **LAN 1**:
  - Andre
    ```bash
    set pcname ANDRE
    ip 192.168.0.2 255.255.255.0
    ip gateway 192.168.0.254

  - Keven
    ```bash
    set pcname KEVEN
    ip 192.168.0.3 255.255.255.0
    ip gateway 192.168.0.254

  - Breno
    ```bash
    set pcname BRENO
    ip 192.168.0.4 255.255.255.0
    ip gateway 192.168.0.254


- **LAN 2**:
  - Lua
    ```bash
    set pcname LUA
    ip 10.0.0.2 255.255.255.0
    ip gateway 10.0.0.254

  - Pedro
    ```bash
    set pcname PEDRO
    ip 10.0.0.3 255.255.255.0
    ip gateway 10.0.0.254

  - Felipe
    ```bash
    set pcname FELIPE
    ip 10.0.0.4 255.255.255.0
    ip gateway 10.0.0.254

## 🔗 Para testes de funcionalidade e mais informações, segue o link:
[Clique aqui! Projeto Completo.](https://www.canva.com/design/DAGX3s0q3LY/EZBiTtYRwA-u0GDSVbtDBg/view?utm_content=DAGX3s0q3LY&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=h55a429acf4)
