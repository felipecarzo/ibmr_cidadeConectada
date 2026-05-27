# GOD BACKLOG — Cidade Conectada

> A existência completa do software em micro-esforços.
> Cada linha que você riscar é um passo real da sua jornada.
> **Riscou, fez. Sem abstração.**

| Dono | Equipe Cidade Conectada |
| :--- | :--- |
| **Início** | — |
| **Término** | — |
| **Stack** | WebApp + API REST + Banco relacional |
| **Contexto** | A3 Engenharia de Software — IBMR |

---

## PREÂMBULO — Como usar este documento

Este guia divide a **existência completa do software** em 9 PARTES.

```
PARTE 0  → Gênese         (a ideia)
PARTE 1  → Descoberta     (o que construir)
PARTE 2  → Planejamento    (como e quando)
PARTE 3  → Product Backlog (o estoque)
PARTE 4  → Sprints         (a execução ágil)
PARTE 5  → Implementação   (o código)
PARTE 6  → Testes          (a validação)
PARTE 7  → Produção Acadêmica (diagramas + docs)
PARTE 8  → Entrega         (apresentação)
```

Cada item tem um `[ ]` — risque quando concluir.
Use como seu diário de bordo pessoal.

---

## PARTE 0 — GÊNESE (Concepção do Projeto)

*O momento zero. O projeto ainda não existe, só a necessidade.*

### 0.1 Identificar o problema

- [ ] **P0.1.1** — Problemas urbanos (buracos, lixo, esgoto, iluminação) sem canal fácil de denúncia
- [ ] **P0.1.2** — Prefeitura sem visibilidade em tempo real dos problemas
- [ ] **P0.1.3** — Cidadão sem retorno sobre denúncias feitas
- [ ] **P0.1.4** — Definir o contexto acadêmico: A3 Engenharia de Software

### 0.2 Pesquisar o domínio

- [ ] **P0.2.1** — Estudar ODS 11 (Cidades e Comunidades Sustentáveis)
- [ ] **P0.2.2** — Analisar concorrentes: Colab, 156, e-Ouve
- [ ] **P0.2.3** — Identificar fluxo: ocorrência → obstáculo → acúmulo → falta de dados → agravamento

### 0.3 Definir o propósito

- [ ] **P0.3.1** — Redigir a visão do produto (1 parágrafo)
- [ ] **P0.3.2** — Definir objetivos mensuráveis
- [ ] **P0.3.3** — Documentar em `docs/po/vision.md`

---

## PARTE 1 — DESCOBERTA (PO / BSA)

*O trabalho de Product Owner. Levantar, modelar, validar.*

### 1.1 Levantar requisitos

- [ ] **P1.1.1** — Entrevistar o "cliente" (professor)
- [ ] **P1.1.2** — Coletar requisitos funcionais (RF-01 a RF-16)
- [ ] **P1.1.3** — Coletar requisitos não-funcionais (RNF-01 a RNF-15)
- [ ] **P1.1.4** — Coletar regras de negócio (RNG-01 a RNG-12)

### 1.2 Mapear entidades do domínio

- [ ] **P1.2.1** — Listar entidades: Usuario, PerfilAcesso, Denuncia, Categoria, HistoricoStatus
- [ ] **P1.2.2** — Identificar atributos de cada entidade
- [ ] **P1.2.3** — Identificar chaves primárias e estrangeiras
- [ ] **P1.2.4** — Classificar entidades: independentes vs dependentes

### 1.3 Modelar banco de dados

- [ ] **P1.3.1** — Desenhar DER conceitual
- [ ] **P1.3.2** — Desenhar DER lógico (tabelas, colunas, FKs)
- [ ] **P1.3.3** — Verificar normalização (3FN)

### 1.4 Criar script SQL

- [ ] **P1.4.1** — Criar schema completo do banco
- [ ] **P1.4.2** — Verificar constraints (PK, FK, NOT NULL)
- [ ] **P1.4.3** — Criar seeds (dados de exemplo)

---

## PARTE 2 — PLANEJAMENTO ESTRATÉGICO

*Roadmap, Product Backlog, MVP, DoD. O mapa do tesouro.*

### 2.1 Definir Roadmap

- [ ] **P2.1.1** — Criar visão macro do projeto em 4 sprints
- [ ] **P2.1.2** — Definir marcos (milestones) de entrega
- [ ] **P2.1.3** — Definir papéis rotativos por sprint

### 2.2 Criar o Product Backlog

- [ ] **P2.2.1** — Listar todas as funcionalidades desejadas (brain dump)
- [ ] **P2.2.2** — Escrever User Stories (16 US)
- [ ] **P2.2.3** — Definir critérios de aceite para cada US
- [ ] **P2.2.4** — Estimar esforço relativo

### 2.3 Priorizar (Técnica MoSCoW)

- [ ] **P2.3.1** — Must have: cadastro, login, registro de denúncia, mapa público, dashboard gestor
- [ ] **P2.3.2** — Should have: notificações, histórico, relatórios
- [ ] **P2.3.3** — Could have: ranking de bairros, exportação de dados
- [ ] **P2.3.4** — Won't have: app nativo (MVP é WebApp)

### 2.4 Definir o MVP

- [ ] **P2.4.1** — Escopo mínimo para validação do professor
- [ ] **P2.4.2** — Funcionalidades obrigatórias: cadastro, login, registro de denúncia com foto/GPS, mapa público
- [ ] **P2.4.3** — Funcionalidades de suporte: dashboard gestor, atualização de status

### 2.5 Criar Casos de Uso

- [ ] **P2.5.1** — Escrever UC-01 a UC-08 (em `docs/qa-lead/use-cases.md`)
- [ ] **P2.5.2** — Validar fluxos principais e alternativos
- [ ] **P2.5.3** — Validar regras de negócio (RNG-01 a RNG-12)

### 2.6 Definir DoD

- [ ] **P2.6.1** — Funcionalidade: botões e fluxos clicáveis
- [ ] **P2.6.2** — Registro: documentação acompanha o desenvolvimento
- [ ] **P2.6.3** — Aprovação: revisado por 2+ membros

---

## PARTE 3 — PRODUCT BACKLOG (Estoque de Funcionalidades)

> 15 itens de backlog documentados em `docs/po/product-backlog.md`.

### 3.1 Épicos

| Código | Épico | Itens |
| :--- | :--- | :--- |
| EP-01 | Registro e Triagem | PB-01, PB-02, PB-10 |
| EP-02 | Acompanhamento | PB-03, PB-04, PB-11 |
| EP-03 | Transparência e Dados | PB-05, PB-06, PB-14 |
| EP-04 | Gestão Pública | PB-07, PB-08, PB-09 |
| EP-05 | Plataforma e Acesso | PB-12, PB-13, PB-15 |

### 3.2 User Stories

| Código | Épico | Descrição |
| :--- | :--- | :--- |
| US-01 | EP-05 | Como cidadão, desejo criar uma conta |
| US-02 | EP-05 | Como cidadão, desejo autenticar-me |
| US-03 | EP-01 | Como cidadão, desejo registrar denúncia com foto e GPS |
| US-04 | EP-01 | Como cidadão, desejo categorizar a denúncia |
| US-05 | EP-02 | Como cidadão, desejo acompanhar o status |
| US-06 | EP-02 | Como cidadão, desejo receber notificações |
| US-07 | EP-02 | Como cidadão, desejo consultar histórico |
| US-08 | EP-03 | Como cidadão, desejo visualizar mapa público |
| US-09 | EP-03 | Como cidadão, desejo ver ranking de bairros |
| US-10 | EP-05 | Como gestor, desejo autenticar-me |
| US-11 | EP-04 | Como gestor, desejo dashboard com mapa de calor |
| US-12 | EP-04 | Como gestor, desejo métricas por bairro |
| US-13 | EP-04 | Como gestor, desejo atualizar status |
| US-14 | EP-04 | Como gestor, desejo relatórios de tempo médio |
| US-15 | EP-05 | Como admin, desejo gerenciar perfis |
| US-16 | EP-03 | Como admin, desejo exportar dados |

---

## PARTE 4 — SPRINTS (A Execução Ágil)

*Cada sprint é um ciclo completo: planejar → executar → revisar.*

### SPRINT 1 — Concepção e Planejamento Inicial

**Coordenação Geral:** Felipe (PO)
**Papel-Líder:** PO — Felipe | **Duração:** ~3-4 dias

**Participação:** Felipe (PO, líder), Tainá (Stakeholder), Giulia (Stakeholder), Luiza (Stakeholder)

**Objetivo:** Definir o que será o app, para quem ele serve e mapear as funcionalidades essenciais.

**Backlog da Sprint:**
- [ ] **S1-01** — Conduzir reunião de alinhamento (Felipe)
- [ ] **S1-02** — Definir propósito e prioridades do Backlog (Felipe)
- [ ] **S1-03** — Configurar repositório/organização (Tainá)
- [ ] **S1-04** — Preparar quadro Kanban (Tainá)
- [ ] **S1-05** — Pesquisar ferramentas de IA e prototipagem (Giulia)
- [ ] **S1-06** — Revisar Canvas e pré-projeto (Luiza)
- [ ] **S1-07** — Gerar Documento de Visão do Produto (Equipe)

**DoD:** Documento de Visão publicado, Canvas preenchido, reunião gravada.

---

### SPRINT 2 — Estruturação e Wireframes

**Coordenação Geral:** Felipe (PO)
**Papel-Líder:** SM — Tainá | **Duração:** ~3-4 dias

**Participação:** Tainá (SM, líder), Felipe (Dev Sênior/Conselheiro), Giulia (Scrum Team), Luiza (Scrum Team)

**Objetivo:** Configurar ambiente, distribuir tarefas de prototipagem e evidenciar o rito ágil.

**Backlog da Sprint:**
- [ ] **S2-01** — Conduzir Sprint Planning (Tainá)
- [ ] **S2-02** — Detalhar histórias de usuário (Felipe)
- [ ] **S2-03** — Validar fluxo com stakeholders simulados (Felipe)
- [ ] **S2-04** — Definir padrões de nomenclatura (Giulia)
- [ ] **S2-05** — Preparar template de diagramas (Giulia)
- [ ] **S2-06** — Definir critérios de aceite por tela (Luiza)
- [ ] **S2-07** — Esboçar wireframes de baixa fidelidade (Equipe)

**DoD:** Quadro configurado, wireframes iniciais, critérios de aceite definidos.

---

### SPRINT 3 — Desenvolvimento do Protótipo (com IA)

**Coordenação Geral:** Felipe (PO)
**Papel-Líder:** Tech Lead — Giulia | **Duração:** ~3-4 dias

**Participação:** Giulia (Tech Lead/Dev/Designer, líder), Felipe (Dev Sênior/Analista/Conselheiro), Tainá (Dev/SM), Luiza (Dev)

**Objetivo:** Mapear diagramas técnicos e gerar as interfaces interativas utilizando IA.

**Backlog da Sprint:**
- [ ] **S3-01** — Escolher ferramenta de IA para protótipo (Giulia)
- [ ] **S3-02** — Gerar telas de alta fidelidade no Figma (Giulia)
- [ ] **S3-03** — Criar diagramas (casos de uso, sequência, classes) (Giulia)
- [ ] **S3-04** — Apoiar prototipação e desenvolvimento (Tainá, Luiza)
- [ ] **S3-05** — Validar se protótipo reflete o propósito (Felipe)
- [ ] **S3-06** — Garantir que o quadro reflita o progresso (Tainá)
- [ ] **S3-07** — Testar botões e fluxos do protótipo alfa (Luiza)
- [ ] **S3-08** — Reportar bugs e ajustar (Equipe)

**DoD:** Diagramas técnicos finalizados, versão alfa do protótipo clicável.

---

### SPRINT 4 — Testes, Ajustes e Fechamento

**Coordenação Geral:** Felipe (PO)
**Papel-Líder:** QA Lead — Luiza | **Duração:** ~3-4 dias

**Participação:** Luiza (QA Lead, líder), Felipe (QA Team/Dev Sênior/Conselheiro), Tainá (SM/Dev/QA Team), Giulia (Tech Lead/Dev/QA Team)

**Objetivo:** Validar conexões do protótipo, revisar material e compilar documento acadêmico final.

**Backlog da Sprint:**
- [ ] **S4-01** — Realizar auditoria final (Luiza)
- [ ] **S4-02** — Aplicar checklist DoD (Luiza)
- [ ] **S4-03** — Compilar entrega acadêmica (Luiza)
- [ ] **S4-04** — Aprovar versão final do protótipo (Felipe)
- [ ] **S4-05** — Organizar Sprint Review e Retrospective (Tainá)
- [ ] **S4-06** — Gravar evidências (Tainá)
- [ ] **S4-07** — Finalizar diagramas pendentes (Giulia)
- [ ] **S4-08** — Exportar protótipo navegável (Giulia)
- [ ] **S4-09** — Apoiar testes e auditoria (Felipe, Tainá, Giulia)

**DoD:** Protótipo finalizado, documentação completa, pitch gravado.

---

## PARTE 5 — ARQUITETURA TEÓRICA (Modelagem Técnica)

> **Nota para o MVP (10-15 dias):** O escopo é um protótipo de alta fidelidade funcional no Figma. Esta seção documenta a arquitetura planejada para uma futura implementação real — diagramas, DER, endpoints e models previstos. É material de apoio para a documentação acadêmica, não para execução no prazo da sprint.

### Fase 5.0 — Setup do Projeto

- [ ] **5.0.1** — Criar repositório Git
- [ ] **5.0.2** — Estruturar diretórios (frontend, backend, database)
- [ ] **5.0.3** — Configurar ambiente de desenvolvimento
- [ ] **5.0.4** — Definir stack final (Node.js/Python/Java)

### Fase 5.1 — Backend: Autenticação

- [ ] **5.1.1** — Model Usuario + PerfilAcesso
- [ ] **5.1.2** — Rota POST /api/auth/register
- [ ] **5.1.3** — Rota POST /api/auth/login
- [ ] **5.1.4** — Middleware de autenticação JWT
- [ ] **5.1.5** — Validação: e-mail único, senha 6-12 caracteres

### Fase 5.2 — Backend: Denúncias

- [ ] **5.2.1** — Model Denuncia + Categoria + HistoricoStatus
- [ ] **5.2.2** — Rota POST /api/denuncias (criar)
- [ ] **5.2.3** — Rota GET /api/denuncias (listar do usuário)
- [ ] **5.2.4** — Rota GET /api/denuncias/:id (detalhe)
- [ ] **5.2.5** — Rota PUT /api/denuncias/:id/status (atualizar)
- [ ] **5.2.6** — Rota GET /api/denuncias/mapa (público)
- [ ] **5.2.7** — Upload de foto (armazenamento local ou cloud)

### Fase 5.3 — Backend: Dashboard e Relatórios

- [ ] **5.3.1** — Rota GET /api/dashboard (métricas)
- [ ] **5.3.2** — Cálculo de tempo médio de resolução
- [ ] **5.3.3** — Relatórios mensais automáticos

### Fase 5.4 — Backend: Admin

- [ ] **5.4.1** — Rota GET /api/admin/usuarios
- [ ] **5.4.2** — Rota PUT /api/admin/usuarios/:id (ativar/desativar)
- [ ] **5.4.3** — Log de auditoria

### Fase 5.5 — Frontend: Autenticação

- [ ] **5.5.1** — Tela de Login
- [ ] **5.5.2** — Tela de Cadastro
- [ ] **5.5.3** — Persistência de token (localStorage)
- [ ] **5.5.4** — Proteção de rotas no frontend

### Fase 5.6 — Frontend: Denúncias

- [ ] **5.6.1** — Tela de Nova Denúncia (câmera + GPS + categoria)
- [ ] **5.6.2** — Tela de Acompanhamento (timeline)
- [ ] **5.6.3** — Tela de Histórico
- [ ] **5.6.4** — Integração com API de denúncias

### Fase 5.7 — Frontend: Mapa e Dashboard

- [ ] **5.7.1** — Mapa público (Leaflet/Google Maps API)
- [ ] **5.7.2** — Pins coloridos por categoria
- [ ] **5.7.3** — Dashboard do gestor (gráficos)
- [ ] **5.7.4** — Ranking de bairros

### Fase 5.8 — Frontend: Admin

- [ ] **5.8.1** — Tela de gerenciamento de usuários
- [ ] **5.8.2** — Exportação de dados

---

## PARTE 6 — TESTES E VALIDAÇÃO

*Verificar se tudo funciona. Caçar bugs.*

### 6.1 Teste de Funcionalidades

**Autenticação**
- [ ] Cadastrar usuário → aparece no banco
- [ ] Login com credenciais corretas → token gerado
- [ ] Login com senha errada → 401
- [ ] Cadastrar com e-mail duplicado → rejeita

**Denúncia**
- [ ] Registrar denúncia com foto → aparece no banco
- [ ] Registrar sem foto → rejeita (RNG-04)
- [ ] Registrar sem GPS → rejeita ou pede fallback
- [ ] Listar denúncias do usuário → apenas as dele
- [ ] Atualizar status → timeline é registrada

**Mapa Público**
- [ ] Mapa exibe pins corretos
- [ ] Filtro por categoria funciona
- [ ] Denúncias resolvidas não aparecem (RNG-08)

**Dashboard**
- [ ] Gestor vê apenas dados da sua região
- [ ] Gráficos refletem dados reais

**Admin**
- [ ] Admin pode desativar usuário
- [ ] Perfis respeitam permissões

---

## PARTE 7 — PRODUÇÃO ACADÊMICA

*O que a faculdade vai avaliar além do código.*

### 7.1 Diagrama de Casos de Uso

- [ ] Criar diagrama com atores: Cidadão, Gestor, Admin
- [ ] Incluir UC-01 a UC-08
- [ ] Ferramenta: draw.io → exportar PNG em `docs/images/`

### 7.2 Diagrama de Classes UML

- [ ] Incluir todas as entidades (Usuario, PerfilAcesso, Denuncia, Categoria, HistoricoStatus)
- [ ] Incluir serviços (AuthService, DenunciaService, RelatorioService)
- [ ] Mostrar atributos e métodos
- [ ] Mostrar relacionamentos (associação, dependência)
- [ ] Formatos: PNG + Mermaid + draw.io

### 7.3 Diagramas de Sequência

- [ ] UC-03 — Registrar Denúncia
- [ ] UC-04 — Acompanhar Denúncia
- [ ] UC-06 — Atualizar Status (Gestor)
- [ ] Mostrar: Ator → Frontend → API → Service → Banco → resposta

### 7.4 DER (Diagrama Entidade-Relacionamento)

- [ ] DER conceitual
- [ ] DER lógico (tabelas com colunas e FKs)

### 7.5 Relatório Técnico (Documento EDUAI)

- [ ] Capa (IBMR, disciplina, integrantes)
- [ ] Introdução (problema, objetivo, justificativa)
- [ ] Tópicos de Engenharia de Software (modelos, ágil, Scrum)
- [ ] Product Backlog
- [ ] Quadro Scrum e Sprints
- [ ] Requisitos (RF, RNF, RNG)
- [ ] User Stories
- [ ] Protótipos (baixa e alta fidelidade)
- [ ] Conclusão
- [ ] Apêndices (Termo de Abertura, Termo de Encerramento)

### 7.6 Slides de Apresentação

- [ ] Slide 1 — Capa
- [ ] Slide 2 — Problema e Motivação (ODS 11)
- [ ] Slide 3 — Tecnologias
- [ ] Slide 4 — Arquitetura
- [ ] Slide 5 — Casos de Uso
- [ ] Slide 6 — Classes UML
- [ ] Slide 7 — Demonstração (protótipo)
- [ ] Slide 8 — Dificuldades e Aprendizados
- [ ] Slide 9 — Conclusão

### 7.7 Vídeo do Pitch

- [ ] Roteiro (3-5 min)
- [ ] Gravação
- [ ] Edição/Legendas

---

## PARTE 8 — ENTREGA

*O checkout. O software existe, foi validado, está documentado.*

### 8.1 Verificação Final

- [ ] **Protótipo:** Todas as telas criadas e navegáveis
- [ ] **Docs:** po/vision.md, qa-lead/use-cases.md, po/product-backlog.md, sm/sprint-backlog.md, tech-lead/technical-design.md, tech-lead/class-diagram.md, GOD_BACKLOG.md
- [ ] **Diagramas:** casos de uso, classes, sequência, DER
- [ ] **Relatório:** documento técnico completo
- [ ] **Slides:** apresentação pronta
- [ ] **Pitch:** vídeo gravado

### 8.2 Artefatos para Entrega

- [ ] Link do protótipo Figma navegável
- [ ] Documento acadêmico formatado (EDUAI)
- [ ] Slides exportados (PDF)
- [ ] Vídeo do pitch (MP4 ou link)

### 8.3 Apresentação

- [ ] Projeto rodando (protótipo ao vivo ou por prints)
- [ ] Explicar arquitetura e metodologia
- [ ] Mostrar casos de uso e fluxos
- [ ] Responder perguntas

---

## APÊNDICE A — Matriz de Rotação de Papéis

Cada sprint um papel-foco diferente lidera as cerimônias ágeis. Todos os membros participam ativamente de todas as sprints com papeis específicos.

| Nome | Base | Sprint 1 (PO) | Sprint 2 (SM) | Sprint 3 (Tech Lead) | Sprint 4 (QA Lead) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Felipe** | PO / Analista Sênior | PO (líder) | Dev Sênior / Conselheiro | Dev Sênior / Analista / Conselheiro | QA Team / Dev Sênior / Conselheiro |
| **Tainá** | Scrum Master | Stakeholder | SM (líder) | Dev / SM | SM / Dev / QA Team |
| **Giulia** | Tech Lead | Stakeholder | Scrum Team | Tech Lead / Dev / Designer (líder) | Tech Lead / Dev / QA Team |
| **Luiza** | QA Lead | Stakeholder | Scrum Team | Dev | QA Lead (líder) |

---

## APÊNDICE B — Glossário

| Termo | Definição |
| :--- | :--- |
| **MVP** | Minimum Viable Product — versão validável |
| **ODS 11** | Objetivo de Desenvolvimento Sustentável: Cidades Sustentáveis |
| **WebApp** | Aplicação web responsiva acessada pelo navegador |
| **PWA** | Progressive Web App — experiência similar a app nativo |
| **GPS** | Global Positioning System — geolocalização |
| **JWT** | JSON Web Token — padrão de autenticação |
| **REST** | Representational State Transfer — estilo arquitetural de APIs |
| **DoD** | Definition of Done — critérios de conclusão |
| **MoSCoW** | Técnica de priorização: Must/Should/Could/Won't |
| **RF** | Requisito Funcional |
| **RNF** | Requisito Não Funcional |
| **RNG** | Regra de Negócio |
| **UC** | Use Case — caso de uso |
| **US** | User Story — história de usuário |
| **DER** | Diagrama Entidade-Relacionamento |
| **UML** | Unified Modeling Language |

---

*Este documento é vivo. Atualize as datas conforme avança.*
*Boa jornada, equipe Cidade Conectada.*
