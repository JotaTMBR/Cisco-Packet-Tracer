# Aulas de Redes
## *Usando o Cisco Packet Tracer*

!["Cisco Packet Tracer"](./image/cisco.webp)

Nessas aulas usamos varias ferramentas importantes para desenvolvermos as atividades propostas pelo docente, e uma delas era o programa Cisco Packet Tracer.

O Packet Tracer é um programa educacional gratuito que permite simular uma rede de computadores, através de equipamentos e configurações presente em situações reais. O programa apresenta uma interface gráfica simples, com suportes multimídia que auxiliam na confecção das simulações. 

---
## Comandos Utilizados:

**en (enable)** -> acesso ao "Super Usuário" ou "modo privilegiado";

**conf t (configure terminal)** -> Modo de configuração do terminal;

**hostname "R-1"** -> muda o nome do roteador ou switch Cisco;

**enable secret "cisco"** -> para criar uma senha criptografada;

**banner motd #** -> para criar uma mensagem na tela inícial do roteador(para finalizar a mensagem basta inserir "#" no final);

**line console 0** -> para entrar na linha de console;

**line vty 0 4** -> linha de comando que permite acesso a um dispositivo Cisco via Telnet;

**password "cisco"** -> para inserir uma senha nas linhas de console e comando;

**login** -> para ativar as portas das linhas de console e comando;

**exit** -> para sair ou voltar;

**interface g0/1** -> para acessar uma porta Gigabit;

**interface s0/0/0** -> para acessar uma porta Serial;

**ip address "192.168.10.254" "255.255.255.0"** -> para acrecentar o ip e a mascara na porta;

**no shutdown** -> para liberar o acesso a porta;

**description "Conexao com Roteador R-2"** -> adiciona uma descrição para a porta;

**end** -> volta para a area inicial do roteador;

**copy running-config startup-config** -> comando para salvar todas as configurações(pode usar também o simples "wr").

---

### RIP e OSPF

**router rip** -> para entrar na configuração do protocolo rip;

**network "192.168.10.0"** -> para apontar a rede;

**router ospf 1** -> para entrar na configuração do protocolo ospf;

**network "192.168.10.0" "0.0.0.255" "area 0"** -> para apontar a rede.

---

### DHCP no Roteador

**ip dhcp pool "REDE"** -> Para iniciar o processo com o nome "REDE";

**network "192.168.10.0" "255.255.255.0"** -> Adiciona a rede e a mascara;

**dns-server "8.8.8.8"** -> Adiciona um DNS para o protocolo

**default-router "192.168.5.1"** -> Define o roteador padrão da rede;

**ip dhcp excluded-address "192.168.10.1" "192.168.5.10"** -> para remover um ip que não queira que seja entrege para alguma máquina.

---

### Outros Comandos

**show ?** -> O comando "show ?" fornece uma lista dos comandos show disponíveis;

**show arp** -> Exibe a tabela ARP do roteador;

**show interfaces** -> Verifica detalhadamente as configurações das interfaces;

**show ip interface brief** -> Verifica resumidamente as configurações das interfaces;

**show ip route** -> Verifica a tabela de roteamento;

**show running-config** -> Verifica as configirações ativas na RAM;

**show startup-config** -> Verifica as configurações da NVRAM;

**sh flash** -> Verifica os arquivos de sistema operacional da Flash.