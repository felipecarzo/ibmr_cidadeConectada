# Product Vision — Cidade Conectada

| Documento | Product Vision |
| :--- | :--- |
| **Versão** | 1.0 |
| **Contexto** | A3 Engenharia de Software — Faculdade IBMR |
| **Stack** | WebApp (HTML/CSS/JS ou framework moderno) + API REST + Banco relacional |

---

## 1. Propósito do Produto

**Para** cidadãos e gestores públicos que precisam resolver problemas urbanos de forma eficiente,
**o** Cidade Conectada **é um** WebApp de denúncias urbanas geolocalizadas
**que** permite registrar, acompanhar e visualizar ocorrências como buracos, lixo acumulado, esgoto aberto e iluminação quebrada,
**diferente de** canais tradicionais como 156 ou formulários genéricos,
**o nosso produto** oferece geolocalização automática, mapa público interativo e dashboard analítico para a gestão pública.

---

## 2. Contexto Acadêmico

Projeto desenvolvido no âmbito da disciplina **Engenharia de Software** do Centro Universitário IBMR. A equipe de 4 integrantes adota **Scrum com papéis fixos** (PO, SM, Tech Lead, QA Lead) em 4 micro-sprints de ~3-4 dias cada, totalizando 14 dias corridos.

### 2.1 Stack Tecnológica

| Camada | Tecnologia |
| :--- | :--- |
| Frontend | WebApp responsivo (HTML/CSS/JS ou framework SPA) |
| Backend | API REST (Node.js / Python / Java — a definir) |
| Banco | PostgreSQL ou MySQL/MariaDB |
| Prototipação | Figma |
| IA Auxiliar | ChatGPT, Claude (código, diagramas, textos) |
| Versionamento | Git + GitHub |

### 2.2 Ambiente Alvo

- Navegadores modernos (Chrome, Firefox, Edge, Safari)
- Dispositivos mobile e desktop (design responsivo)
- Hospedagem cloud com suporte a HTTPS

---

## 3. Jornada do Cidadão

O fluxo completo de uso do sistema, do problema à resolução:

| Etapa | Descrição |
| :--- | :--- |
| **1. Acesso Facilitado** | Cidadão abre o WebApp no navegador do celular, sem download |
| **2. Evidência Georreferenciada** | Foto do problema com geolocalização automática via GPS |
| **3. Triagem Automática** | Denúncia categorizada e direcionada ao órgão competente |
| **4. Acompanhamento** | Status em tempo real: registrada → em análise → em execução → resolvida |
| **5. Feedback Transparente** | Notificação com foto do antes/depois da resolução |
| **6. Mapeamento** | Mapa de calor atualizado com estatísticas do bairro |

---

## 4. Definição de Pronto (Definition of Done)

Nenhuma funcionalidade é considerada concluída sem cumprir **todos** os critérios abaixo:

- [ ] **Funcionalidade:** Botões e fluxos estão clicáveis e direcionam ao destino correto
- [ ] **Registro:** Decisões e artefatos documentados no repositório
- [ ] **Aprovação:** Revisado por pelo menos 2 outros membros da equipe
- [ ] **Qualidade:** Protótipo sem quebras de navegação

---

## 5. Stakeholders

| Papel | Descrição |
| :--- | :--- |
| **Professor Fábio Gomes** | Cliente / Avaliador — valida o projeto A3 |
| **Equipe (4 integrantes)** | Felipe (PO/Coord.), Tainá (SM), Giulia (Tech Lead), Luiza (QA Lead) |
| **Cidadãos** | Usuários finais que reportam problemas urbanos |
| **Gestores Públicos** | Usuários que analisam dados e gerenciam denúncias |
