---
title: "Meu Primeiro Post"
date: 2025-04-20 16:50:00 +0000
categories: [Blog]
tags: [aws, nat, egress, egressonly, ipv4. ipv6, cloud, subnet, vpc, jekyll, chirpy, conhecimento]
---

![Top Image](/assets/img/natxegress.jpeg)

☁️ Falando de AWS

✍ NAT Gateway x Egress-Only Internet Gateway

Durante meus estudos e conversas, notei que muitos colegas de TI, que não necessariamente atuam como analistas de network, frequentemente confundem os serviços de NAT Gateway e Egress-Only Internet Gateway.

Tentando ser o mais direto possível, vamos entender os casos de uso:

1️⃣ - AWS NAT Gateways: esse recurso é de fácil entendimento pois está na cabeça do profissional de TI desde os seus primeiros estudos. Com certeza, na sua faculdade em alguma aula foi citado e explicado o conceito de NAT. 
Nada mais é que a tradução de endereços IPv4 (NAT - Network Address Translation), de modo que seja possível acessar a Internet a partir de um servidor privado utilizando o IP público da interface do NAT.

No cenário AWS o NAT Gateway funciona em modo stateful: a conexão originada no servidor privado pode ser respondida pelo destino público porque o seu estado foi salvo. O stateful é importante pois proporciona proteção ao seu servidor privado contra os riscos associados à exposição na rede pública, bloqueando todo o tráfego da internet que não tenha sido originado em seu servidor privado.

2️⃣ - O Egress-Only Internet Gateway (para facilitar chamarei de EIGW) segue o mesmo conceito, mas adaptado ao IPv6!
Quando usamos Pv6 sabemos que existem três tipos, sendo eles Unicast, Anycast e Multicast. No tipo Unicast temos alguns “subtipos”, sendo um deles o Global Unicast, equivalente aos endereços IPv4 públicos. No cenário da AWS os IPv6 são tratados por default como públicos.

💭 “IPv6 addresses are globally unique, and are therefore public by default.” ~Documentação AWS, link na lista de fontes.

Então não é possível ter uma subnet privada em IPv6 na AWS? Nada disso, é possível graças ao Egress-Only Internet Gateway!

O EIGW opera em sua subnet privada IPv6 de maneira semelhante ao NAT, estabelecendo uma conexão stateful entre seu servidor privado e a internet, enquanto o protege do tráfego gerado na rede pública. A principal distinção é que o EIGW é projetado para IPv6 e não realiza tradução de endereços IP.

🤓 👆 anota para não esquecer:
Subnets privadas IPv4? NAT!
Subnets privadas IPv6? EIGW!

Fontes:
AWS NAT Gateway: https://lnkd.in/d_i4aWdg
AWS EIGW: https://lnkd.in/dxQJJEPZ 
IPv6: https://lnkd.in/dPheSPcW 
Conceito de NAT: https://lnkd.in/dPZqCYbT 