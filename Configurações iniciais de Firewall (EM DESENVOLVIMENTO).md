<h1>🔐 Firewall Rules</h1>

<h2>🎯 Objetivos:</h2>

<b>1️⃣ Proxy (Squid):</b>

Definir políticas de acesso à web.

<b>2️⃣ Regras de Firewall – Usuários (VLAN 10):</b>

Definir quem pode acessar o quê.

Permitir saída para o proxy se ele for transparente ou explícito.

<b>3️⃣ Regras de Firewall – Servidores (VLAN 20):</b>

Permitir apenas os serviços necessários.

Bloquear qualquer acesso desnecessário.

<b>4️⃣ Instalação e Configuração do Wazuh:</b>

Depois de tudo seguro e segmentado, subir o SIEM pra começar as configurações.</br></br>

<h2>🧰 Instalação do Proxy (Squid)</h2>

Será utilizado o serviço de proxy Squid, disponível no OPNsense, para controle de acesso à web dos usuários da rede.

<a href="https://imgur.com/a/e4oUy4A"><img src="https://i.imgur.com/xcl6c9x.png" title="source: imgur.com" /></a>

<h2>🚧 Firewall Rules – VLAN 10 (Usuários)</h2>

As regras aplicadas na VLAN 10 têm como objetivo garantir que os dispositivos dos usuários acessem apenas o necessário, permitindo explicitamente protocolos necessários enquanto o que não for permitido estará em implicit block.

<a href="https://imgur.com/a/QRX2FHt"><img src="https://i.imgur.com/8gIId9e.png" title="source: imgur.com" /></a>

<h2>🖥️ Firewall Rules – VLAN 20 (Servidores)</h2>

A VLAN 20, destinada aos servidores, tem regras mais restritivas para garantir a segurança do ambiente.

<a href="https://imgur.com/a/IGWHNYl"><img src="https://i.imgur.com/nP8dAbR.png" title="source: imgur.com" /></a>

<h2>⚙️ Zenarmor</h2>
O Zenarmor é um plugin moderno de inspeção de tráfego (Next-Gen Firewall) integrado ao OPNsense, que oferece visibilidade detalhada, controle granular e proteção avançada para a rede.<br><br>

<b>Principais benefícios do Zenarmor:</b><br>

✅ Inspeção profunda de pacotes para identificar aplicações, usuários e ameaças.<br>
✅ Controle baseado em políticas para bloquear ou permitir serviços e sites.<br>
✅ Monitoramento em tempo real do uso de banda e atividade da rede.<br>
✅ Fácil integração com regras e segmentação do OPNsense.<br><br>

Com o Zenarmor, é possível reforçar a segurança do laboratório, aplicando filtros e analisando tráfego em múltiplas VLANs, ampliando o controle sobre a comunicação entre segmentos da rede e para a internet.<br><br>

<a href="https://imgur.com/a/nPP88IR"><img src="https://i.imgur.com/lt3g10D.png" title="source: imgur.com" /></a>
<a href="https://imgur.com/a/nPP88IR"><img src="https://i.imgur.com/cR1jFWK.png" title="source: imgur.com" /></a>
