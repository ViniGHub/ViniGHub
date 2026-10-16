# Vinicius Rodrigues da Silva

Desenvolvedor full stack, com TypeScript, React e Node.js no dia a dia. Me interessam os problemas
em que o detalhe técnico decide se a coisa funciona: dois navegadores que precisam se achar sem um
servidor no meio, um pagamento que não pode ser cobrado duas vezes, uma fila que não pode perder
mensagem.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/vini-rodri)
[![E-mail](https://img.shields.io/badge/E--mail-555?style=flat&logo=gmail&logoColor=white)](mailto:Vinicius.rodrigues2004@gmail.com)

---

## Projetos em destaque

### [Sinal](https://github.com/ViniGHub/sinal-app) · [abrir o app](https://vinighub.github.io/sinal-app/)

Voz e compartilhamento de tela entre navegadores, ponto a ponto via WebRTC. Áudio e vídeo vão
direto de uma pessoa para a outra; só o aperto de mão inicial passa por um broker de sinalização.

- **Salas sem servidor próprio.** Um canal é um ID de peer no broker, e o broker garante um único
  dono por ID. Quem consegue registrar o ID vira o ponto de encontro da sala; os outros discam para
  ele. Quando esse participante sai, os demais disputam o ID com atraso aleatório e a sala continua.
- **Credenciais TURN efêmeras** emitidas por um Cloudflare Worker, para que nenhuma senha de relay
  acabe embutida no bundle público.
- **Lógica de conexão separada do React**, exposta por `useSyncExternalStore` sobre um snapshot.
  O código é organizado por domínio (`session`, `media`, `channels`, `chat`).
- **Testes onde o bug aparece:** Vitest para a lógica isolada e Playwright com dois navegadores
  reais se conectando. O pipeline do GitHub Actions bloqueia o deploy com erro de tipo, lint ou teste.

`React 19` `TypeScript` `WebRTC` `PeerJS` `Cloudflare Workers` `Vitest` `Playwright` `GitHub Actions`

### [TicketFlow](https://github.com/ViniGHub/TicketFlow) · em desenvolvimento

Plataforma de venda de ingressos com Stripe Checkout, projetada a partir do que costuma quebrar em
sistemas de pagamento: estoque disputado, webhook repetido, job perdido.

- Webhook idempotente: o `event.id` do Stripe é gravado com `UNIQUE` na mesma transação do
  processamento, e evento repetido é ignorado.
- Transactional outbox: nenhuma transação de negócio enfileira direto no BullMQ. O worker lê a
  tabela `outbox` com `SKIP LOCKED` e publica, com entrega *at-least-once* e jobs idempotentes.
- Nenhuma chamada HTTP externa dentro de transação de banco; chamadas ao Stripe usam
  `idempotencyKey` derivada do pedido.
- Arquitetura, modelo de dados e roadmap documentados antes do código, com ADRs e testes de
  integração em Postgres e Redis reais via Testcontainers.

`Next.js` `NestJS` `PostgreSQL` `Prisma` `Redis` `BullMQ` `Stripe` `Turborepo`

### Outros projetos

| Projeto | O que é | Stack |
|---|---|---|
| [diplomas-microservices](https://github.com/ViniGHub/diplomas-microservices) | API que recebe pedidos de diploma e delega a geração a um worker por fila | Node.js, RabbitMQ, MySQL, Redis, Docker Compose |
| [Santander_BI](https://github.com/ViniGHub/Santander_BI) | ETL de dados de clientes e transações para SQLite, API REST e painel de análise | Python, Node.js, SQLite |
| [meetup-app](https://github.com/ViniGHub/meetup-app) | App de meetups com banco, autenticação e migrations no Supabase | React, TypeScript, Supabase, PL/pgSQL |
| [crypto-monitor](https://github.com/ViniGHub/crypto-monitor) · [crypto-report](https://github.com/ViniGHub/crypto-report) | Apps Android de acompanhamento de criptomoedas | Kotlin |
| [poh-roulette](https://github.com/ViniGHub/poh-roulette) | Roleta com presets salvos, animação com desaceleração e efeitos sonoros | React, TypeScript, Framer Motion, Web Audio API |

---

## Como eu trabalho

- TypeScript em modo estrito e lint type-aware como ponto de partida.
- Cada tipo de risco tem o teste que o pega: unitário para regra de negócio, integração com banco
  real para concorrência, e2e quando a falha só existe entre dois navegadores.
- CI que impede o deploy de código quebrado.
- Decisões e limites ficam escritos no README. O do Sinal tem uma seção de limites conhecidos.
- Segredo fica fora do repositório e fora do bundle.

## Stack

| Área | Tecnologias |
|---|---|
| Linguagens | TypeScript, JavaScript, PHP, Kotlin, Python, Dart |
| Front-end | React, Angular, Tailwind CSS, Vite |
| Back-end | Node.js, Laravel |
| Dados e mensageria | PostgreSQL, MySQL, SQLite, Redis, RabbitMQ, Supabase |
| Mobile | Android (Kotlin), Flutter |
| Infra e qualidade | Docker, GitHub Actions, GitHub Pages, Cloudflare Workers, Vitest, Playwright |

## Formação

Sistemas de Informação na FIAP, com projetos acadêmicos desenvolvidos em parceria com empresas
como Santander e Eurofarma.
