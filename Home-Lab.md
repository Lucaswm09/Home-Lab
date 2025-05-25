<h1>🔐 Home Lab de Segurança</h1>

<h2>🎯 Objetivo do Projeto</h2>

Este projeto tem como objetivo criar um home lab de segurança de redes, simulando um ambiente corporativo com firewall, segmentação em VLANs e monitoramento de segurança.</br></br>
A proposta é entender na prática como funciona uma infraestrutura segmentada e protegida, aplicando conceitos essenciais de redes e cibersegurança.</br></br>

<b>Componentes do laboratório:</b></br>
🔥 <b>Firewall OPNsense</b> – Controle de tráfego, roteamento entre VLANs e aplicação de regras de segurança.</br>
🖥️ <b>Servidor Ubuntu Server</b> – Hospeda o Wazuh (SIEM) e seu banco de dados, simulando um servidor corporativo.</br>
💻 <b>Host Windows 11</b> – Simula uma estação de trabalho de um usuário comum conectado na rede de usuários.</br>

---

<h2>🗺️ Topologia da Rede</h2>

<a href="https://imgur.com/a/e4oUy4A"><img src="https://imgur.com/a/e4oUy4A" /></a>

<b>🌐 Descrição da Topologia:</b></br>
- O <b>OPNsense</b> faz a interligação entre as redes internas (VLANs) e a internet (WAN).</br>
- Três VLANs são configuradas para segmentação:</br>
🔸 <b>VLAN 10 – Rede de usuários</b> (Windows 11)</br>
🔸 <b>VLAN 20 – Rede de servidores</b> (Ubuntu + Wazuh)</br>
🔸 <b>VLAN 99 – Rede de gerenciamento</b> (Rede de acesso para ADMs)</br>
- A interface WAN conecta o ambiente à internet via NAT e DHCP.</br>

---

<h2>🧠 Descrição dos Componentes</h2>

<table border="1">
<tr>
<th>Dispositivo</th>
<th>Função</th>
<th>IP</th>
<th>VLAN</th>
<th>Descrição</th>
</tr>

<tr>
<td>OPNsense (WAN)</td>
<td>Firewall (Internet)</td>
<td>DHCP ou estático</td>
<td>-</td>
<td>Conexão externa</td>
</tr>

<tr>
<td>OPNsense (LAN)</td>
<td>Gateway VLAN 10</td>
<td>192.168.10.1</td>
<td>VLAN 10</td>
<td>Rede de usuários</td>
</tr>

<tr>
<td>OPNsense (SERV)</td>
<td>Gateway VLAN 20</td>
<td>192.168.20.1</td>
<td>VLAN 20</td>
<td>Rede de servidores</td>
</tr>

<tr>
<td>OPNsense (MGMT)</td>
<td>Gateway VLAN 99</td>
<td>192.168.99.1</td>
<td>VLAN 99</td>
<td>Rede de gerenciamento</td>
</tr>

<tr>
<td>Windows 11</td>
<td>Estação de trabalho</td>
<td>192.168.10.2</td>
<td>VLAN 10</td>
<td>Usuário comum</td>
</tr>

<tr>
<td>Ubuntu Server</td>
<td>Servidor com Wazuh</td>
<td>192.168.20.2</td>
<td>VLAN 20</td>
<td>Servidor para SIEM (Wazuh)</td>
</tr>
</table>

---

<h2>🚧 Importância da Segmentação em VLANs</h2>

Segmentar a rede utilizando VLANs é uma prática fundamental em segurança da informação.</br>
Além de organizar a rede, isso impede que dispositivos de diferentes funções se comuniquem diretamente sem passar pelo firewall, elevando significativamente o nível de segurança.</br></br>

<b>🔑 Benefícios da segmentação:</b></br>
✅ Isolamento das redes (usuários, servidores e gerenciamento).</br>
✅ Dificulta movimentações laterais em caso de um ataque.</br>
✅ Permite aplicar regras específicas para cada rede.</br>
✅ Reduz a superfície de ataque.</br>
✅ Facilita o monitoramento e a gestão da rede.</br>

---

<h2>🛡️ Aplicações na Segurança da Informação</h2>

Este home lab permite colocar em prática vários conceitos importantes de redes e segurança:</br></br>
- Configuração de firewall e roteamento entre VLANs.</br>
- Controle de tráfego interno e externo.</br>
- Aplicação de políticas de segurança para cada segmento.</br>
- Monitoramento de eventos, geração de alertas e análise de segurança utilizando um SIEM (<b>Wazuh</b>).</br>
- Simulação de cenários reais de ambientes corporativos.</br>

---
