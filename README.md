<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&height=200&color=0:0d1117,100:1f7a4d&text=Vinicius%20Rodrigues&fontColor=ffffff&fontSize=44&fontAlignY=36&desc=Desenvolvedor%20Full%20Stack%20%C2%B7%20TypeScript%20%C2%B7%20React%20%C2%B7%20Node.js&descAlignY=58&descSize=17" width="100%" alt="Vinicius Rodrigues, desenvolvedor full stack" />

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/vini-rodri)
[![E-mail](https://img.shields.io/badge/E--mail-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:Vinicius.rodrigues2004@gmail.com)
[![Sinal ao vivo](https://img.shields.io/badge/Sinal_ao_vivo-1f7a4d?style=for-the-badge&logo=webrtc&logoColor=white)](https://vinighub.github.io/sinal-app/)

Gosto de problemas em que o detalhe técnico decide se a coisa funciona:
conexão direta entre navegadores, pagamento que não pode ser cobrado duas vezes, fila que não pode perder mensagem.

</div>

## Projetos em destaque

### 📡 [Sinal](https://github.com/ViniGHub/sinal-app)

Voz e tela **ponto a ponto** entre navegadores. [**Abrir o app →**](https://vinighub.github.io/sinal-app/)

<a href="https://vinighub.github.io/sinal-app/"><img src="assets/sinal.png" alt="Tela do Sinal" width="100%" /></a>

<table>
<tr>
<td align="center" width="25%">🕸️<br/><b>Malha WebRTC</b><br/><sub>sem servidor de mídia</sub></td>
<td align="center" width="25%">🔑<br/><b>Salas sem backend</b><br/><sub>o broker garante um dono por canal</sub></td>
<td align="center" width="25%">🛡️<br/><b>TURN efêmero</b><br/><sub>credenciais via Cloudflare Worker</sub></td>
<td align="center" width="25%">🎭<br/><b>E2E real</b><br/><sub>dois navegadores conectando no CI</sub></td>
</tr>
</table>

![React](https://img.shields.io/badge/React_19-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![WebRTC](https://img.shields.io/badge/WebRTC-333333?style=flat-square&logo=webrtc&logoColor=white)
![Cloudflare Workers](https://img.shields.io/badge/Cloudflare_Workers-F38020?style=flat-square&logo=cloudflareworkers&logoColor=white)
![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

### 🎟️ [TicketFlow](https://github.com/ViniGHub/TicketFlow) <sub>em desenvolvimento</sub>

Venda de ingressos com Stripe, projetada em torno do que costuma quebrar em pagamentos.

```mermaid
flowchart LR
    W["Next.js + BFF"] --> A["API NestJS"]
    S["Stripe"] -- "webhook assinado<br/>e idempotente" --> A
    A -- "pedido + outbox<br/>na mesma transação" --> P[("PostgreSQL")]
    P -- "SKIP LOCKED" --> R["Worker"]
    R <--> Q[("Redis / BullMQ")]
    R --> E["E-mail"]
    R -- "expirar / reembolsar" --> S
```

![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)
![Redis](https://img.shields.io/badge/Redis_+_BullMQ-DC382D?style=flat-square&logo=redis&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-635BFF?style=flat-square&logo=stripe&logoColor=white)
![Turborepo](https://img.shields.io/badge/Turborepo-EF4444?style=flat-square&logo=turborepo&logoColor=white)

## Outros projetos

<table>
<tr>
<td width="50%" valign="top">

**[diplomas-microservices](https://github.com/ViniGHub/diplomas-microservices)**<br/>
API e worker de geração de diplomas desacoplados por fila

<img src="https://skillicons.dev/icons?i=nodejs,rabbitmq,mysql,redis,docker" height="32" alt="Node.js, RabbitMQ, MySQL, Redis, Docker" />

</td>
<td width="50%" valign="top">

**[Santander_BI](https://github.com/ViniGHub/Santander_BI)**<br/>
ETL de transações, API REST e painel de análise

<img src="https://skillicons.dev/icons?i=py,nodejs,sqlite,js" height="32" alt="Python, Node.js, SQLite, JavaScript" />

</td>
</tr>
<tr>
<td valign="top">

**[meetup-app](https://github.com/ViniGHub/meetup-app)**<br/>
App de meetups com banco e autenticação no Supabase

<img src="https://skillicons.dev/icons?i=react,ts,supabase,postgres,tailwind" height="32" alt="React, TypeScript, Supabase, PostgreSQL, Tailwind" />

</td>
<td valign="top">

**[crypto-monitor](https://github.com/ViniGHub/crypto-monitor) · [crypto-report](https://github.com/ViniGHub/crypto-report)**<br/>
Apps Android de acompanhamento de criptomoedas

<img src="https://skillicons.dev/icons?i=kotlin,androidstudio" height="32" alt="Kotlin, Android Studio" />

</td>
</tr>
<tr>
<td valign="top">

**[poh-roulette](https://github.com/ViniGHub/poh-roulette)**<br/>
Roleta com presets, animação física e efeitos sonoros

<img src="https://skillicons.dev/icons?i=react,ts,tailwind,vite" height="32" alt="React, TypeScript, Tailwind, Vite" />

</td>
<td valign="top">

**[Controle-series](https://github.com/ViniGHub/Controle-series)**<br/>
Controle de séries assistidas, com autenticação e CRUD

<img src="https://skillicons.dev/icons?i=laravel,php" height="32" alt="Laravel, PHP" />

</td>
</tr>
</table>

## Como eu trabalho

<table>
<tr>
<td align="center" width="25%">🔒<br/><b>Tipagem estrita</b><br/><sub>TS strict e lint type-aware</sub></td>
<td align="center" width="25%">🧪<br/><b>Teste certo</b><br/><sub>unitário, integração e e2e</sub></td>
<td align="center" width="25%">🚦<br/><b>CI como portão</b><br/><sub>código quebrado não sobe</sub></td>
<td align="center" width="25%">📝<br/><b>Decisões escritas</b><br/><sub>ADRs e limites conhecidos</sub></td>
</tr>
</table>

## Stack

<table>
<tr><td><b>Linguagens</b></td><td><img src="https://skillicons.dev/icons?i=ts,js,php,kotlin,py,dart" alt="TypeScript, JavaScript, PHP, Kotlin, Python, Dart" /></td></tr>
<tr><td><b>Front-end</b></td><td><img src="https://skillicons.dev/icons?i=react,angular,tailwind,vite" alt="React, Angular, Tailwind, Vite" /></td></tr>
<tr><td><b>Back-end</b></td><td><img src="https://skillicons.dev/icons?i=nodejs,laravel" alt="Node.js, Laravel" /></td></tr>
<tr><td><b>Dados e filas</b></td><td><img src="https://skillicons.dev/icons?i=postgres,mysql,sqlite,redis,rabbitmq,supabase" alt="PostgreSQL, MySQL, SQLite, Redis, RabbitMQ, Supabase" /></td></tr>
<tr><td><b>Mobile</b></td><td><img src="https://skillicons.dev/icons?i=androidstudio,flutter" alt="Android, Flutter" /></td></tr>
<tr><td><b>Infra e testes</b></td><td><img src="https://skillicons.dev/icons?i=docker,githubactions,cloudflare,vitest" alt="Docker, GitHub Actions, Cloudflare, Vitest" /></td></tr>
</table>

## Formação

[![FIAP](https://img.shields.io/badge/FIAP-Sistemas_de_Informação-ED145B?style=for-the-badge)](https://www.fiap.com.br/)

Projetos acadêmicos em parceria com Santander e Eurofarma.

<img src="https://capsule-render.vercel.app/api?type=waving&height=100&color=0:1f7a4d,100:0d1117&section=footer" width="100%" alt="" />
