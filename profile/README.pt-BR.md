<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./assets/logo-primary-dark.svg">
    <img alt="CypherGrid" src="./assets/logo-primary-light.svg" width="320">
  </picture>
</p>

<p align="center"><sub><a href="https://github.com/CypherGrid">English</a> · <b>Português (Brasil)</b></sub></p>

<p align="center">
  <strong>Autenticação contínua por biometria comportamental.</strong><br>
  Saiba que ainda é a mesma pessoa, do login à última transação.
</p>

---

## O problema

A autenticação acontece uma vez, no login. A fraude acontece depois.

Tomada de conta, engenharia social, transações sob coação e scripts
automatizados operam dentro de sessões que já passaram por todos os fatores
de autenticação. Senhas, códigos de uso único e verificações de dispositivo
confirmam quem abriu a sessão. Não dizem nada sobre quem a está operando
alguns minutos depois.

## O que construímos

O **CypherGrid Collect** verifica a identidade de forma contínua e
silenciosa, a partir de *como* a pessoa interage com a aplicação, e não do
que ela digita.

- **DNA comportamental.** Um SDK leve observa a forma da interação - ritmo de
  digitação, dinâmica de toque e de ponteiro, movimento do dispositivo,
  cadência de navegação - e constrói, ao longo do tempo, um perfil
  comportamental de cada usuário.
- **Score de risco.** Cada sessão é avaliada contra esse perfil e contra
  sinais de automação, para distinguir o usuário legítimo de um terceiro, de
  um script ou de um agente operando a aplicação.
- **Pontos de avaliação e ações.** O integrador marca os momentos sensíveis
  dos próprios fluxos - login, pagamentos, cadastro de beneficiário, troca de
  senha - e define regras simples para cada um: por exemplo, pedir
  autenticação adicional quando o risco for alto.
- **Decisões verificáveis.** Cada avaliação devolve um token de decisão
  assinado e de curta duração, que o backend do integrador verifica antes de
  autorizar a operação. A decisão é um controle no servidor, não uma
  sugestão no dispositivo.
- **Sem atrito extra.** O usuário legítimo não vê nenhuma etapa nova. O
  atrito só aparece quando o risco justifica.

A CypherGrid entrega o sinal comportamental e a decisão em cada ponto de
avaliação. A plataforma foi pensada para complementar, e não substituir, os
motores de fraude e risco que nossos clientes já operam.

## Privacidade desde a concepção

Dado comportamental é sensível, e a plataforma foi construída a partir desse
fato.

- **Forma, não conteúdo.** O SDK nunca captura o que é digitado, colado ou
  exibido - apenas características de tempo e de movimento.
- **Pseudônimo por padrão.** Usuários e dispositivos são identificados por
  identificadores pseudônimos, distintos para cada cliente.
- **Minimização de dados.** Dados brutos de interação só são retidos quando
  uma sessão precisa de investigação, e por tempo limitado.
- **Feita para ambientes regulados.** Projetada com a LGPD e o GDPR europeu
  em mente, para organizações que precisam justificar cada dado pessoal que
  tratam.

## Plataformas

| Plataforma | Status |
|---|---|
| Web - JavaScript, React, Vue, Angular | **Beta** · totalmente funcional |
| Android - Kotlin nativo | Em desenvolvimento |
| iOS - Swift nativo | Planejado |

A captura e a extração de características vivem num único núcleo em Rust,
compartilhado por todos os SDKs: o mesmo comportamento produz o mesmo sinal
em qualquer plataforma.

## Para quem é

Bancos, instituições de pagamento, fintechs e qualquer produto digital em que
uma única sessão comprometida custa caro: transações financeiras,
recuperação de conta, troca de credenciais, abertura de conta e operações de
alto valor.

## Acesso antecipado

A CypherGrid está em **acesso antecipado**, trabalhando com um pequeno grupo
de design partners para validar a plataforma em fluxos reais de produção. Os
canais de contato serão publicados aqui em breve.

---

<p align="center"><sub>© CypherGrid · São Paulo, Brasil</sub></p>
