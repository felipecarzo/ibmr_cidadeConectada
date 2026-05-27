# 06_PROTOTIPOS

# 06 — Protótipos das Interfaces

Baseado em: `refs/Documento - A3 Engenharia de Software.pdf` (seção de protótipos do EDUAI), `olddocs/fluxograma escrito.docx`

## Diretrizes de Design

- **Fonte:** Inter ou similar, mínimo 16 pt para mobile
- **Cores:** Contraste elevado, botões vibrantes com rótulos autoexplicativos
- **Ícones:** Intuitivos (câmera para foto, marcador para GPS, engrenagem para configurações)
- **Navegação:** Linear e simples, com feedback visual imediato
- **Acessibilidade:** WCAG 2.1 nível AA

## Protótipos de Baixa Fidelidade

### Ferramentas Sugeridas

- Papel e caneta (esboço inicial)
- Balsamiq
- Figma (modo wireframe)

### Telas para Esboçar

1. **Tela de Cadastro/Login** — campos de e-mail e senha, botão “Entrar” e “Criar conta”
2. **Tela Principal (Feed)** — botão grande “Nova Denúncia”, lista das últimas denúncias do usuário
3. **Tela de Registro** — visualizador de câmera, campo de categoria (seleção), botão “Enviar”
4. **Tela de Acompanhamento** — timeline do status (registrada → análise → execução → resolvida)
5. **Mapa Público** — mapa com pins coloridos por categoria
6. **Dashboard do Gestor** — mapa de calor, gráficos por bairro e categoria

## Protótipos de Alta Fidelidade

### Ferramenta Sugerida

- **Figma** (com IA ou plugins para acelerar)

### Telas a Desenvolver

| # | Tela | Descrição | Funcionalidades |
| --- | --- | --- | --- |
| 1 | **Login / Cadastro** | Tela inicial com formulário de login e opção de cadastro | Campos e-mail/senha, botão “Criar conta”, “Recuperar senha” |
| 2 | **Home (Cidadão)** | Tela principal do cidadão com resumo e atalhos | Botão “Nova Denúncia”, últimas denúncias, notificações |
| 3 | **Registro de Denúncia** | Captura de foto + seleção de categoria + confirmação de localização | Câmera integrada, dropdown de categorias, mapa de pré-visualização GPS |
| 4 | **Acompanhamento** | Timeline visual do status da denúncia | 4 etapas com ícones, data/hora de cada atualização |
| 5 | **Mapa Público** | Mapa interativo com pins de denúncias | Filtros por categoria, legenda por cor, zoom, clique no pin para detalhes |
| 6 | **Histórico** | Lista de denúncias do usuário | Busca, filtro por status/data, acesso ao detalhe de cada uma |
| 7 | **Dashboard (Gestor)** | Painel administrativo | Mapa de calor, gráficos por bairro, tempo médio de resolução, filtros |
| 8 | **Detalhe da Denúncia (Gestor)** | Visualização completa da denúncia | Foto, localização, status, botão “Atualizar Status” |
| 9 | **Relatórios** | Estatísticas mensais | Gráficos de pizza/barras, exportação de dados |
| 10 | **Perfil** | Configurações do usuário | Editar dados, alterar senha, preferências de notificação |

## Fluxo de Navegação

```
Login/Cadastro
       │
       ▼
  Home (Cidadão) ────────────────────┐
       │                              │
       ├── Nova Denúncia              │
       │       │                      │
       │       ▼                      │
       │  Registro → Confirmação      │
       │                              │
       ├── Minhas Denúncias           │
       │       │                      │
       │       ▼                      │
       │  Acompanhamento (timeline)   │
       │                              │
       ├── Mapa Público               │
       │                              │
       └── Perfil                     │
                                      │
  Login Gestor                        │
       │                              │
       ▼                              │
  Dashboard (Gestor)                  │
       │                              │
       ├── Mapa de Calor              │
       ├── Denúncias (detalhe)        │
       ├── Relatórios                 │
       └── Perfil                     │
                                      │
  Admin (mesmo fluxo do gestor        │
  + gerenciamento de usuários) ───────┘
```

## Relação com os Épicos

| Tela | Épico Relacionado |
| --- | --- |
| Login / Cadastro | EP-05 (Plataforma e Acesso) |
| Home (Cidadão) | EP-02 (Acompanhamento) |
| Registro de Denúncia | EP-01 (Registro e Triagem) |
| Acompanhamento | EP-02 (Acompanhamento) |
| Mapa Público | EP-03 (Transparência e Dados) |
| Histórico | EP-02 (Acompanhamento) |
| Dashboard (Gestor) | EP-04 (Gestão Pública) |
| Detalhe da Denúncia (Gestor) | EP-04 (Gestão Pública) |
| Relatórios | EP-04 (Gestão Pública) |
| Perfil | EP-05 (Plataforma e Acesso) |

## Critérios de Aceite do Protótipo

- [ ]  Todas as telas acima foram criadas no Figma
- [ ]  Botões e links estão clicáveis e direcionam para a tela correta
- [ ]  O fluxo de “Nova Denúncia → Confirmação” está funcional
- [ ]  O Mapa Público exibe pins simulados
- [ ]  O Dashboard do gestor contém gráficos e mapa de calor simulados
- [ ]  A navegação de volta (voltar) funciona em todas as telas
- [ ]  O protótipo pode ser exportado como link navegável