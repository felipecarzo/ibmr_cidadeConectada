# Product Backlog — Cidade Conectada

| Documento | Product Backlog |
| :--- | :--- |
| **Versão** | 1.0 |
| **Priorização** | MoSCoW (Must / Should / Could / Won't) |

---

## 1. Épicos

### EP-01 — Registro e Triagem
Captura, categorização e encaminhamento automático de denúncias urbanas.

### EP-02 — Acompanhamento
Status em tempo real, notificações e histórico para o cidadão.

### EP-03 — Transparência e Dados
Mapa público interativo, ranking de bairros e exportação de dados.

### EP-04 — Gestão Pública
Dashboard analítico, mapa de calor, relatórios e métricas para a prefeitura.

### EP-05 — Plataforma e Acesso
Cadastro, autenticação, perfis de acesso e segurança.

---

## 2. Product Backlog (Itens)

> **Escopo MVP (10-15 dias):** Protótipo de alta fidelidade funcional no Figma — telas clicáveis que demonstram o fluxo completo. Itens marcados como **Must** são obrigatórios para a validação do professor; **Should** agregam valor à demonstração; **Could** são diferenciais.

| ID | Épico | Item do Backlog | MVP | Descrição (para o protótipo) |
| :--- | :--- | :--- | :---: | :--- |
| PB-12 | EP-05 | Cadastro de usuário | **Must** | Tela de cadastro (nome, e-mail, senha) com validação |
| PB-13 | EP-05 | Autenticação de gestor | **Must** | Tela de login com campos e-mail/senha e botão "Entrar" |
| PB-01 | EP-01 | Registro de denúncia com foto | **Must** | Tela com botão de câmera, pré-visualização da foto e confirmação |
| PB-02 | EP-01 | Categorização da denúncia | **Must** | Dropdown ou cards de seleção (buraco, lixo, esgoto, iluminação, outros) |
| PB-03 | EP-02 | Acompanhamento em tempo real | **Must** | Tela com timeline visual do status (4 etapas) |
| PB-05 | EP-03 | Mapa público de denúncias | **Must** | Mapa interativo com pins coloridos por categoria |
| PB-07 | EP-04 | Dashboard do gestor | **Must** | Painel com mapa de calor, métricas por bairro e categoria |
| PB-04 | EP-02 | Notificação de atualização | Should | Popup/notificação simulando alerta de mudança de status |
| PB-11 | EP-02 | Histórico de denúncias do usuário | Should | Lista de denúncias do usuário com filtro por status |
| PB-06 | EP-03 | Ranking de bairros ativos | Should | Tabela ou gráfico de barras com ranking por bairro |
| PB-08 | EP-04 | Relatório de tempo médio de resolução | Should | Gráfico no dashboard com tempo médio por categoria |
| PB-09 | EP-04 | Feedback antes/depois | Should | Tela de detalhe mostrando foto do antes e depois |
| PB-15 | EP-05 | Perfis de acesso | Could | Tela de seleção de perfil (cidadão/gestor) no cadastro |
| PB-10 | EP-01 | Encaminhamento automático | — | Lógica de backend — não prototipável; documentar como requisito |
| PB-14 | EP-03 | Exportação de dados | — | Não faz parte do escopo do protótipo |

---

## 3. User Stories

### EP-05 — Plataforma e Acesso

| ID | Como um... | Eu quero... | Para que... | Prioridade |
| :--- | :--- | :--- | :--- | :--- |
| US-01 | Cidadão | criar uma conta no sistema | registrar denúncias | Must |
| US-02 | Cidadão | autenticar-me no sistema | acessar as funcionalidades | Must |
| US-10 | Gestor público | autenticar-me no sistema | acessar o painel administrativo | Must |
| US-15 | Administrador | gerenciar perfis de acesso | garantir a segurança do sistema | Should |

### EP-01 — Registro e Triagem

| ID | Como um... | Eu quero... | Para que... | Prioridade |
| :--- | :--- | :--- | :--- | :--- |
| US-03 | Cidadão | registrar uma denúncia com foto e GPS | reportar problemas urbanos | Must |
| US-04 | Cidadão | categorizar a denúncia | ela chegue ao órgão correto | Must |

### EP-02 — Acompanhamento

| ID | Como um... | Eu quero... | Para que... | Prioridade |
| :--- | :--- | :--- | :--- | :--- |
| US-05 | Cidadão | acompanhar o status da minha denúncia | saber se está sendo resolvida | Must |
| US-06 | Cidadão | receber notificações sobre atualizações | ficar informado | Should |
| US-07 | Cidadão | consultar meu histórico de denúncias | acompanhar meu engajamento | Should |

### EP-03 — Transparência e Dados

| ID | Como um... | Eu quero... | Para que... | Prioridade |
| :--- | :--- | :--- | :--- | :--- |
| US-08 | Cidadão | visualizar o mapa público de denúncias | ver os problemas da minha região | Must |
| US-09 | Cidadão | ver o ranking de bairros | incentivar a participação comunitária | Could |
| US-16 | Administrador | exportar dados anonimizados | pesquisa e urbanismo | Could |

### EP-04 — Gestão Pública

| ID | Como um... | Eu quero... | Para que... | Prioridade |
| :--- | :--- | :--- | :--- | :--- |
| US-11 | Gestor público | visualizar o dashboard com mapa de calor | identificar áreas críticas | Must |
| US-12 | Gestor público | visualizar métricas por bairro | priorizar ações | Must |
| US-13 | Gestor público | atualizar o status das denúncias | informar o cidadão | Must |
| US-14 | Gestor público | ver relatórios de tempo médio de resolução | avaliar a eficiência | Should |

---

## 4. Mapeamento UC × US

| Caso de Uso | User Stories |
| :--- | :--- |
| UC-01 — Cadastrar Usuário | US-01 |
| UC-02 — Autenticar Usuário | US-02, US-10 |
| UC-03 — Registrar Denúncia | US-03, US-04 |
| UC-04 — Acompanhar Denúncia | US-05, US-06, US-07 |
| UC-05 — Visualizar Mapa Público | US-08, US-09 |
| UC-06 — Gerenciar Denúncias (Gestor) | US-11, US-12, US-13 |
| UC-07 — Gerar Relatórios | US-14 |
| UC-08 — Gerenciar Perfis de Acesso | US-15, US-16 |

---

## 5. Regras de Negócio (Consolidadas)

| ID | Categoria | Descrição | UC |
| :--- | :--- | :--- | :--- |
| RNG-01 | Identificação | Todo usuário deve se autenticar com e-mail e senha | UC-01, UC-02 |
| RNG-02 | Identificação | A senha deve conter de 6 a 12 caracteres alfanuméricos | UC-01 |
| RNG-03 | Identificação | Cada perfil tem acesso individual conforme seu nível de permissão | UC-02, UC-08 |
| RNG-04 | Denúncia | A denúncia deve conter obrigatoriamente: foto, localização GPS e categoria | UC-03 |
| RNG-05 | Denúncia | Uma denúncia só pode ser resolvida pelo órgão público competente | UC-03 |
| RNG-06 | Denúncia | O status da denúncia segue o fluxo: registrada → em análise → em execução → resolvida | UC-03, UC-04, UC-06 |
| RNG-07 | Denúncia | O cidadão pode registrar no máximo 10 denúncias por dia | UC-03 |
| RNG-08 | Transparência | O mapa público exibe apenas denúncias com status "registrada" ou "em andamento" | UC-05 |
| RNG-09 | Gestão | O dashboard do gestor só exibe dados da sua região/município | UC-06 |
| RNG-10 | Gestão | Relatórios mensais devem ser gerados automaticamente no dia 1 de cada mês | UC-07 |
| RNG-11 | Integridade | Denúncias resolvidas são arquivadas após 90 dias | UC-07 |
| RNG-12 | Segurança | Dados anonimizados para exportação não podem conter informação pessoal identificável | UC-07 |
