<!-- ═══════════════════════════════  HEADER  ═══════════════════════════════ -->
<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,45:3b2f8f,100:6C63FF&height=230&section=header&text=Pedro%20Garcia&fontSize=68&fontColor=ffffff&fontAlignY=36&desc=Full%20Stack%20Developer%20%C2%B7%20SaaS%20%C2%B7%20IA%20%C2%B7%20Web%20Imersiva&descSize=18&descAlignY=58&animation=fadeIn" width="100%" alt="Pedro Garcia — Full Stack Developer" />

<a href="https://www.pedrogarciadev.com.br/">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&duration=2800&pause=900&color=6C63FF&center=true&vCenter=true&width=640&height=44&lines=Do+banco+de+dados+ao+pixel+%E2%80%94+ponta+a+ponta.;APIs+seguras+em+Node.js+%2B+MongoDB;Agentes+de+IA+no+WhatsApp+em+produ%C3%A7%C3%A3o;Experi%C3%AAncias+3D+com+Three.js+%26+GSAP;Shipping+desde+o+primeiro+commit." alt="Typing SVG" />
</a>

<br/>

<a href="https://www.pedrogarciadev.com.br/"><img src="https://img.shields.io/badge/Portfólio-pedrogarciadev.com.br-6C63FF?style=for-the-badge&logo=googlechrome&logoColor=white&labelColor=1a1b27" alt="Portfólio" /></a>
<a href="https://www.linkedin.com/in/pedrogarcia-tech"><img src="https://img.shields.io/badge/LinkedIn-Conectar-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=1a1b27" alt="LinkedIn" /></a>
<a href="https://www.instagram.com/pedrocadev"><img src="https://img.shields.io/badge/Instagram-@pedrocadev-E4405F?style=for-the-badge&logo=instagram&logoColor=white&labelColor=1a1b27" alt="Instagram" /></a>
<a href="https://www.tiktok.com/@pedrogarciadev"><img src="https://img.shields.io/badge/TikTok-@pedrogarciadev-ff0050?style=for-the-badge&logo=tiktok&logoColor=white&labelColor=1a1b27" alt="TikTok" /></a>

<br/>

<img src="https://img.shields.io/badge/status-dispon%C3%ADvel%20para%20projetos-2ea043?style=flat-square&labelColor=1a1b27" alt="Disponível" />
<img src="https://img.shields.io/badge/local-Monte%20Aprazível%2C%20SP%20%C2%B7%20Remoto-6C63FF?style=flat-square&labelColor=1a1b27" alt="Localização" />
<img src="https://komarev.com/ghpvc/?username=pedrogarcialeite04&style=flat-square&color=6C63FF&label=visitas" alt="Visitas" />

</div>

<br/>

<!-- ═══════════════════════════════  SOBRE  ═══════════════════════════════ -->

## Sobre mim

Sou **desenvolvedor Full Stack** e construo produtos completos — da modelagem do banco e da API até a interface que o usuário toca. Meu trabalho vive no cruzamento entre **engenharia sólida** e **experiência memorável**: sistemas SaaS com autenticação, painéis administrativos, integrações com **WhatsApp e IA generativa** rodando em produção, e front-ends imersivos com **Three.js** e **GSAP**.

```js
// pedro.config.js
export default {
  role:       "Full Stack Developer",
  location:   "Monte Aprazível, SP · remoto",
  frontend:   ["JavaScript", "TypeScript", "HTML/CSS/SCSS", "Three.js", "GSAP"],
  backend:    ["Node.js", "Express", "Python", "FastAPI", "Serverless (Vercel Functions)"],
  data:       ["MongoDB", "PostgreSQL", "Redis", "Firebird"],
  ai:         ["Gemini / Vertex AI", "Groq (Llama + Whisper)", "WhatsApp Cloud API"],
  infra:      ["Docker", "filas com workers (arq)", "Sentry", "GitHub Actions"],
  security:   ["JWT", "bcrypt", "Helmet", "Rate limiting", "Sanitização (XSS / NoSQL injection)"],
  shipping:   ["Vercel", "Render", "Git"],
  mindset:    "produção primeiro: seguro, observável, rápido",
  available:  true,
};
```

<!-- ═══════════════════════════════  O QUE ENTREGO  ═══════════════════════════════ -->

## O que eu entrego

<table>
  <tr>
    <td width="33%" valign="top">
      <h3>Front-end</h3>
      Interfaces responsivas, animadas e rápidas. Cenas 3D em <b>Three.js</b>, scroll storytelling com <b>GSAP ScrollTrigger / SplitText</b> e micro-interações que fazem o produto parecer vivo.
    </td>
    <td width="33%" valign="top">
      <h3>Back-end</h3>
      APIs em <b>Node.js/Express</b> e <b>Python/FastAPI</b>, filas com workers, PostgreSQL e MongoDB, JWT, validação, rate limit, Helmet, upload e processamento de imagem (<b>Multer + Sharp</b>) e logs estruturados (<b>Winston</b>).
    </td>
    <td width="33%" valign="top">
      <h3>IA & Automação</h3>
      Agentes conversacionais no <b>WhatsApp</b> com <b>Gemini</b>, base de conhecimento editável, guarda contra prompt injection e <b>handoff para atendente humano</b> em tempo real.
    </td>
  </tr>
</table>

<!-- ═══════════════════════════════  CASE  ═══════════════════════════════ -->

## Case em produção — Plataforma de atendimento com IA

> Projeto privado para cliente · **em produção** · serverless + painel em tempo real

Assistente virtual que atende clientes no **site e no WhatsApp**, responde com base em conhecimento curado pela equipe e, quando precisa, **transfere a conversa para um atendente humano** — que responde por um painel web com push notification, citação de mensagens, foto e áudio.

```mermaid
flowchart LR
    U(["Cliente"]) -->|WhatsApp| W["WhatsApp Cloud API"]
    U -->|Site| S["Chat web"]
    W --> H["Webhook · Vercel Functions"]
    S --> H
    H --> G{"Prompt guard\n+ rate limit"}
    G --> AI["Gemini / Vertex AI"]
    AI <--> KB[("Base de\nconhecimento")]
    H <--> R[("Redis\nsessões · fila · estado")]
    H -->|handoff| P["Painel do atendente\nRender · Web Push"]
    P <--> DB[("Firebird\nERP do cliente")]
    T["Admin de treino\nExpress · Blob"] --> KB
```

<sub>**Destaques de engenharia:** autenticação de sessão própria · proteção contra prompt injection · fila de atendimento com expediente e renovação automática via cron · agrupamento de mensagens em rajada · mídia (foto/áudio) com prazo · observabilidade e verificação de origem.</sub>

<!-- ═══════════════════════════════  PROJETOS  ═══════════════════════════════ -->

## Projetos em destaque

<table>
  <tr>
    <td width="50%" valign="top">
      <h3>SaaS de Cheques</h3>
      Sistema SaaS para gestão e controle de cheques, com interface animada (GSAP) e elementos 3D.
      <br/><br/>
      <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" />
      <img src="https://img.shields.io/badge/SCSS-CC6699?style=flat-square&logo=sass&logoColor=white" />
      <img src="https://img.shields.io/badge/GSAP-88CE02?style=flat-square&logo=greensock&logoColor=black" />
      <img src="https://img.shields.io/badge/Three.js-000000?style=flat-square&logo=threedotjs&logoColor=white" />
      <br/><br/>
      <a href="https://saa-s-cheques.vercel.app">Demo</a> · <a href="https://github.com/pedrogarcialeite04/SaaS-cheques">Código</a>
    </td>
    <td width="50%" valign="top">
      <h3>Museu 3D</h3>
      Museu virtual navegável no navegador: cena WebGL com iluminação, tone mapping ACES e transições cinematográficas.
      <br/><br/>
      <img src="https://img.shields.io/badge/Three.js-000000?style=flat-square&logo=threedotjs&logoColor=white" />
      <img src="https://img.shields.io/badge/GSAP-88CE02?style=flat-square&logo=greensock&logoColor=black" />
      <img src="https://img.shields.io/badge/WebGL-990000?style=flat-square&logo=webgl&logoColor=white" />
      <img src="https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white" />
      <br/><br/>
      <a href="https://museupedroca.vercel.app">Demo</a> · <a href="https://github.com/pedrogarcialeite04/museu3d">Código</a>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>Plataforma FJR — site + painel + API</h3>
      Produto completo em 3 camadas: landing, painel administrativo e API com JWT em cookie, bcrypt, Helmet, rate limit, sanitização contra XSS/NoSQL injection, upload com Sharp e logs com Winston.
      <br/><br/>
      <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white" />
      <img src="https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white" />
      <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white" />
      <img src="https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white" />
      <br/><br/>
      <a href="https://teste-remoto.vercel.app">Site</a> · <a href="https://paineladmfjr.vercel.app">Painel</a> · <a href="https://github.com/pedrogarcialeite04/backend-fjr">API</a>
    </td>
    <td width="50%" valign="top">
      <h3>Assistente Financeiro no WhatsApp</h3>
      Agente que entende <b>texto e áudio</b> (Whisper), registra gastos e receitas e responde com relatórios e alertas de orçamento. Webhook com validação HMAC responde em ms e enfileira; o <b>worker</b> processa com idempotência e lock.
      <br/><br/>
      <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" />
      <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
      <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" />
      <img src="https://img.shields.io/badge/Groq-F55036?style=flat-square&logoColor=white" />
      <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
      <br/><br/>
      <a href="https://github.com/pedrogarcialeite04/bot_whatsapp">Código</a>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>Plataforma de Casamento</h3>
      Convite digital + painel administrativo + API serverless de confirmação de presença (RSVP), com token de admin e CORS restrito por origem.
      <br/><br/>
      <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" />
      <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white" />
      <img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white" />
      <br/><br/>
      <a href="https://convite-nu-cyan.vercel.app">Convite</a> · <a href="https://paginaadm-casamento.vercel.app">Admin</a> · <a href="https://github.com/pedrogarcialeite04/backend-casamento">Código</a>
    </td>
    <td width="50%" valign="top">
      <h3>Foco — app de produtividade</h3>
      Aplicação full stack com contas de usuário, autenticação JWT e API protegida com Helmet e rate limiting.
      <br/><br/>
      <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" />
      <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white" />
      <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white" />
      <img src="https://img.shields.io/badge/GSAP-88CE02?style=flat-square&logo=greensock&logoColor=black" />
      <br/><br/>
      <a href="https://foco-delta.vercel.app">Demo</a> · <a href="https://github.com/pedrogarcialeite04/app-foco">Front</a> · <a href="https://github.com/pedrogarcialeite04/backend-foco">API</a>
    </td>
  </tr>
</table>

<details>
<summary><b>Mais projetos</b></summary>
<br/>

| Projeto | O que é | Stack |
|---|---|---|
| [**PGFlow**](https://pgflow.vercel.app) | Dashboard com gráficos e fundo 3D de partículas | Three.js · Chart.js · GSAP |
| [**Portfólio**](https://www.pedrogarciadev.com.br) | Meu portfólio — performance e micro-interações | Three.js · GSAP · AOS |
| [**Theze Sistema**](https://github.com/pedrogarcialeite04/theze-sistema) | Sistema de gestão local rodando como serviço Windows | Node.js · Express · node-windows |
| [**Spider-Man LP**](https://github.com/pedrogarcialeite04/homem-aranha-lp) | Landing cinematográfica guiada pelo scroll | GSAP ScrollSmoother · SplitText |
| [**Theze Caminhão**](https://github.com/pedrogarcialeite04/theze-caminhao) | Gestão de serviços de caminhão prancha | JavaScript · GSAP |
| [**Armazenamento de notas**](https://github.com/pedrogarcialeite04/sistema-de-armazenamento-de-dados) | Organização e armazenamento de notas fiscais | JavaScript |
| [**Sistema de Posto**](https://github.com/pedrogarcialeite04/projeto-de-posto-) | Login e registro de abastecimentos | HTML · CSS · JS |

</details>

<!-- ═══════════════════════════════  STACK  ═══════════════════════════════ -->

## Stack

<div align="center">

<table>
  <tr>
    <td align="center"><b>Front-end</b></td>
    <td><img src="https://skillicons.dev/icons?i=js,ts,html,css,sass,threejs&perline=8" /> <img src="https://img.shields.io/badge/GSAP-88CE02?style=for-the-badge&logo=greensock&logoColor=black" height="44" /></td>
  </tr>
  <tr>
    <td align="center"><b>Back-end</b></td>
    <td><img src="https://skillicons.dev/icons?i=nodejs,express,python,fastapi,php&perline=8" /></td>
  </tr>
  <tr>
    <td align="center"><b>Dados</b></td>
    <td><img src="https://skillicons.dev/icons?i=mongodb,postgres,redis&perline=8" /> <img src="https://img.shields.io/badge/Firebird-F40F02?style=for-the-badge&logo=firebird&logoColor=white" height="44" /></td>
  </tr>
  <tr>
    <td align="center"><b>IA & Cloud</b></td>
    <td><img src="https://skillicons.dev/icons?i=gcp,vercel,docker&perline=8" /> <img src="https://img.shields.io/badge/Gemini-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white" height="44" /> <img src="https://img.shields.io/badge/Render-46E3B7?style=for-the-badge&logo=render&logoColor=black" height="44" /></td>
  </tr>
  <tr>
    <td align="center"><b>Ferramentas</b></td>
    <td><img src="https://skillicons.dev/icons?i=git,github,githubactions,postman,vscode,figma&perline=8" /></td>
  </tr>
  <tr>
    <td align="center"><b>Acadêmico</b></td>
    <td><img src="https://skillicons.dev/icons?i=c,cs&perline=8" /></td>
  </tr>
</table>

</div>

<!-- ═══════════════════════════════  PRINCÍPIOS  ═══════════════════════════════ -->

## Como eu trabalho

- **Segurança por padrão** — nada vai pra produção sem autenticação, validação de entrada, rate limit e segredos fora do código.
- **Produção é a fonte da verdade** — logs, observabilidade e testes de regressão antes de cada deploy.
- **Performance é feature** — animação a 60 fps, assets otimizados e serverless onde faz sentido.
- **Código que outro dev entende** — documentação viva, commits descritivos e decisões registradas.

<!-- ═══════════════════════════════  MÉTRICAS  ═══════════════════════════════ -->

## Atividade

<div align="center">

<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=pedrogarcialeite04&layout=compact&langs_count=8&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=6C63FF&text_color=c9d1d9&card_width=520&custom_title=Linguagens%20mais%20usadas" width="520" alt="Top Langs" />

<br/><br/>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/pedrogarcialeite04/pedrogarcialeite04/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/pedrogarcialeite04/pedrogarcialeite04/output/github-snake.svg" />
  <img alt="Snake comendo meu gráfico de contribuições" src="https://raw.githubusercontent.com/pedrogarcialeite04/pedrogarcialeite04/output/github-snake-dark.svg" width="100%" />
</picture>

</div>

<!-- ═══════════════════════════════  CTA + FOOTER  ═══════════════════════════════ -->

<div align="center">

### Vamos construir algo juntos?

Tem um SaaS, uma automação com IA ou uma experiência web que precisa sair do papel?

<a href="https://www.pedrogarciadev.com.br/"><img src="https://img.shields.io/badge/Fale%20comigo-6C63FF?style=for-the-badge" alt="Fale comigo" /></a>
<a href="https://www.linkedin.com/in/pedrogarcia-tech"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:6C63FF,55:3b2f8f,100:0d1117&height=120&section=footer" width="100%" />

</div>
