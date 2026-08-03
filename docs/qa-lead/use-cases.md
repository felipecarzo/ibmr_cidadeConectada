# Especificação de Casos de Uso

| Documento | Use Case Specification |
| :--- | :--- |
| **Versão** | 1.0 |
| **Atores** | Cidadão, Gestor Público, Administrador |

---

![Diagrama de Casos de Uso](../images/casos-de-uso.png)

---

## Atores do Sistema

| Ator | Descrição |
| :--- | :--- |
| **Cidadão** | Usuário comum — registra denúncias, acompanha status, consulta mapa público |
| **Gestor Público** | Funcionário da prefeitura — gerencia denúncias, acessa dashboard e relatórios |
| **Administrador** | Superusuário — gerencia perfis de acesso e auditoria |

---

## UC-01 — Cadastrar Usuário

**Ator Principal:** Cidadão
**Objetivo:** Criar conta no sistema para registrar e acompanhar denúncias.
**Pré-condições:** Nenhuma.
**Pós-condições:** Usuário cadastrado com sucesso; sistema redireciona para tela de login.

**Fluxo Principal:**
1. Cidadão acessa a tela de cadastro
2. Sistema solicita nome, e-mail e senha
3. Cidadão informa os dados e confirma
4. Sistema valida e-mail único (RNG-01), senha 6-12 caracteres alfanuméricos (RNG-02)
5. Sistema armazena dados e exibe confirmação
6. Sistema redireciona para tela de login

**Regras de Negócio:** RNG-01, RNG-02

---

## UC-02 — Autenticar Usuário

**Ator Principal:** Cidadão / Gestor Público
**Objetivo:** Acessar o sistema com credenciais cadastradas.
**Pré-condições:** Usuário deve estar cadastrado.
**Pós-condições:** Usuário autenticado com token JWT; redirecionado para home conforme perfil.

**Fluxo Principal:**
1. Usuário acessa tela de login
2. Sistema solicita e-mail e senha
3. Usuário informa credenciais
4. Sistema valida e autentica
5. Sistema redireciona para a home conforme perfil

**Fluxo Alternativo (Credenciais Inválidas):**
1. Sistema exibe mensagem de erro
2. Usuário tenta novamente ou recupera senha

**Regras de Negócio:** RNG-01, RNG-03

---

## UC-03 — Registrar Denúncia

**Ator Principal:** Cidadão
**Objetivo:** Reportar um problema urbano com foto e geolocalização.
**Pré-condições:** Cidadão deve estar autenticado.
**Pós-condições:** Denúncia registrada com status "registrada"; encaminhada ao órgão competente; cidadão recebe código de acompanhamento.

**Fluxo Principal:**
1. Cidadão acessa "Nova Denúncia"
2. Sistema ativa câmera e captura geolocalização
3. Cidadão tira foto do problema
4. Sistema exibe pré-visualização com localização
5. Cidadão seleciona a categoria (buraco, lixo, esgoto, iluminação, outros)
6. Cidadão confirma o envio
7. Sistema registra denúncia com status "registrada"
8. Sistema encaminha automaticamente ao órgão competente
9. Sistema exibe confirmação com código de acompanhamento

**Fluxo Alternativo (Limite Diário):**
1. Sistema verifica que cidadão já atingiu 10 denúncias no dia (RNG-07)
2. Sistema bloqueia novo registro e informa o limite

**Regras de Negócio:** RNG-04, RNG-05, RNG-06, RNG-07

---

## UC-04 — Acompanhar Denúncia

**Ator Principal:** Cidadão
**Objetivo:** Visualizar o status e timeline de uma denúncia.
**Pré-condições:** Denúncia deve estar registrada.
**Pós-condições:** Timeline do status da denúncia exibida ao cidadão.

**Fluxo Principal:**
1. Cidadão acessa "Minhas Denúncias"
2. Sistema exibe lista de denúncias do usuário
3. Cidadão seleciona uma denúncia
4. Sistema exibe timeline visual: registrada → em análise → em execução → resolvida
5. Sistema exibe foto, localização, data e status atual

**Regras de Negócio:** RNG-06

---

## UC-05 — Visualizar Mapa Público

**Ator Principal:** Cidadão (autenticado ou não)
**Objetivo:** Ver problemas reportados na região em mapa interativo.
**Pré-condições:** Nenhuma.
**Pós-condições:** Mapa interativo com pins de denúncias ativas exibido ao usuário.

**Fluxo Principal:**
1. Usuário acessa "Mapa Público"
2. Sistema carrega mapa com pins coloridos por categoria
3. Usuário navega, dá zoom e clica nos pins
4. Sistema exibe detalhes da denúncia (foto, descrição, status)

**Regras de Negócio:** RNG-08

---

## UC-06 — Gerenciar Denúncias (Gestor)

**Ator Principal:** Gestor Público
**Objetivo:** Visualizar, atualizar status e gerenciar denúncias da sua região.
**Pré-condições:** Gestor deve estar autenticado.
**Pós-condições:** Status da denúncia atualizado; cidadão notificado sobre a alteração.

**Fluxo Principal:**
1. Gestor acessa o dashboard
2. Sistema exibe mapa de calor, métricas por bairro e categoria
3. Gestor seleciona uma denúncia para detalhar
4. Sistema exibe foto, localização, histórico
5. Gestor atualiza o status (análise, execução, resolvida)
6. Sistema notifica o cidadão sobre a atualização

**Regras de Negócio:** RNG-06, RNG-09

---

## UC-07 — Gerar Relatórios

**Ator Principal:** Gestor Público
**Objetivo:** Visualizar estatísticas e tempo médio de resolução.
**Pré-condições:** Gestor autenticado.
**Pós-condições:** Gráficos e relatórios exibidos; dados anonimizados exportados se solicitado.

**Fluxo Principal:**
1. Gestor acessa "Relatórios"
2. Sistema exibe gráficos de pizza/barras por categoria e bairro
3. Sistema exibe tempo médio de resolução
4. Gestor pode exportar dados anonimizados (se autorizado)

**Regras de Negócio:** RNG-10, RNG-11, RNG-12

---

## UC-08 — Gerenciar Perfis de Acesso

**Ator Principal:** Administrador
**Objetivo:** Gerenciar contas e permissões de usuários.
**Pré-condições:** Administrador autenticado.
**Pós-condições:** Contas ativadas/desativadas; permissões alteradas; log de auditoria registrado.

**Fluxo Principal:**
1. Administrador acessa "Gerenciar Usuários"
2. Sistema exibe lista de usuários cadastrados
3. Administrador pode ativar/desativar contas
4. Administrador pode alterar permissões de perfil
5. Sistema registra alterações em log de auditoria

**Regras de Negócio:** RNG-03
