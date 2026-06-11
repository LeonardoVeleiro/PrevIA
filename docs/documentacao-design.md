# Documentação de Design — Sprint 2

## 1. Objetivo do Protótipo

O objetivo desta documentação é apresentar as decisões de design, o mapa de telas e o relacionamento entre o protótipo navegável da Sprint 2 e a modelagem desenvolvida na Sprint 1 do projeto PrevIA.

O PrevIA é uma solução de segurança industrial proativa que utiliza câmeras, visão computacional e inteligência artificial para detectar colaboradores, verificar o uso correto de EPIs, identificar situações de risco, emitir alertas preventivos, registrar ocorrências e gerar relatórios de conformidade.

Na Sprint 2, o foco foi transformar os requisitos, personas, casos de uso, diagrama de atividades e diagrama de classes da Sprint 1 em uma interface navegável no Figma. O protótipo não possui implementação em código, mas simula a experiência principal do usuário dentro do sistema.

---

## 2. Mapa de Telas

O protótipo foi estruturado com as seguintes telas principais:

| Tela                        | Objetivo                                                                       |
| --------------------------- | ------------------------------------------------------------------------------ |
| Login                       | Permitir o acesso simulado ao sistema por diferentes perfis de usuário.        |
| Dashboard de Monitoramento  | Exibir visão geral dos alertas, ocorrências, conformidade e áreas monitoradas. |
| Monitoramento em Tempo Real | Simular a análise de câmera, detecção de colaborador e verificação de EPIs.    |
| Alertas e Notificações      | Listar alertas identificados pelo sistema e destacar o fluxo principal.        |
| Histórico de Ocorrências    | Permitir a consulta de ocorrências registradas anteriormente.                  |
| Detalhe da Ocorrência       | Exibir informações completas de uma ocorrência específica.                     |
| Registrar Ação Preventiva   | Simular o registro de uma ação tomada pela supervisora de segurança.           |
| Colaboradores               | Listar colaboradores monitorados pelo sistema.                                 |
| Detalhe do Colaborador      | Consultar dados do colaborador, EPIs obrigatórios e histórico recente.         |
| Editar EPIs do Colaborador  | Simular a alteração dos EPIs vinculados a um colaborador.                      |
| Gestão de EPIs              | Listar e gerenciar EPIs obrigatórios por área ou função.                       |
| Relatórios de Conformidade  | Exibir indicadores, gráficos e filtros por setor e período.                    |
| Relatório Detalhado         | Simular o relatório gerado para um setor específico.                           |
| Câmeras e Áreas Monitoradas | Exibir câmeras, setores monitorados, status e EPIs obrigatórios por área.      |

---

## 3. Fluxos Navegáveis Principais

A Sprint 2 solicitou que o protótipo cobrisse três fluxos principais. Esses fluxos foram representados no Figma da seguinte forma:

### 3.1 Cadastro e Consulta de EPI por Colaborador

Fluxo:

1. Login
2. Dashboard
3. Colaboradores
4. Detalhe do Colaborador — Carlos Henrique
5. Editar EPIs
6. Salvar alterações
7. Retorno ao detalhe do colaborador com mensagem de sucesso

Esse fluxo representa a consulta dos EPIs obrigatórios associados ao colaborador e a simulação da edição desses vínculos. No protótipo, o colaborador Carlos Henrique foi utilizado como exemplo principal, pois também está relacionado ao alerta de ausência de capacete.

A tela de detalhe mostra os EPIs obrigatórios, o status de conformidade e o histórico recente de ocorrências. A tela/modal de edição permite visualizar os EPIs vinculados ao colaborador e simular uma atualização.

### 3.2 Emissão e Visualização de Alerta de Risco

Fluxo:

1. Dashboard
2. Monitoramento em Tempo Real
3. Ver Alerta Preventivo
4. Detalhe da Ocorrência
5. Registrar Ação Preventiva
6. Salvar ação
7. Ocorrência resolvida com sucesso

Esse fluxo foi baseado diretamente no Diagrama de Atividades da Sprint 1. A tela de monitoramento simula a captura de imagem por câmera, a detecção do colaborador Carlos Henrique e a identificação da ausência do capacete de segurança.

Como a Sprint 2 exige apenas um protótipo navegável, a área da câmera foi representada por um frame simulado. O objetivo é demonstrar a experiência de uso e a lógica do fluxo, sem implementar o processamento real de visão computacional.

A ocorrência gerada exibe data, horário, setor, tipo de irregularidade, criticidade, EPIs obrigatórios e EPIs detectados. Em seguida, a supervisora Mariana Oliveira registra uma ação preventiva, encerrando a ocorrência.

### 3.3 Geração de Relatório de Conformidade por Setor

Fluxo:

1. Dashboard
2. Relatórios de Conformidade
3. Gerar Relatório
4. Relatório Detalhado — Produção
5. Visualização de indicadores e recomendações preventivas

Esse fluxo representa a necessidade do gestor industrial de consultar indicadores consolidados sobre segurança e conformidade. A tela de relatórios apresenta filtros por setor e período, além de gráficos, indicadores e resumo por setor.

O relatório detalhado mostra dados do setor de Produção, como taxa de conformidade, total de alertas, total de ocorrências, colaboradores monitorados, análise por EPI, ocorrências do período e recomendações preventivas.

O botão de exportação em PDF foi representado visualmente como uma ação prevista para uma versão funcional do sistema. Nesta Sprint, a ação é simulada no protótipo, pois o foco está na navegação e validação da experiência.

---

## 4. Decisões de UX/UI

### 4.1 Hierarquia de Informação

A interface foi organizada para priorizar informações críticas de segurança. Por isso, o Dashboard apresenta logo no início os principais indicadores:

* alertas ativos;
* ocorrências do dia;
* taxa de conformidade;
* áreas monitoradas.

Essa organização facilita a leitura rápida por parte da supervisora de segurança, que precisa tomar decisões preventivas em pouco tempo.

### 4.2 Uso de Cores

A paleta visual foi pensada para o contexto de segurança industrial:

* azul escuro: identidade principal do sistema e sensação de confiança;
* branco e cinza claro: fundos neutros para facilitar a leitura;
* verde: conformidade, câmera online e ocorrência resolvida;
* amarelo/laranja: atenção ou risco médio;
* vermelho: alerta crítico, EPI ausente e risco alto.

Essa escolha permite que o usuário identifique rapidamente a gravidade de cada situação.

### 4.3 Componentes Reutilizáveis

O protótipo utiliza componentes semelhantes entre as telas para manter consistência visual:

* menu lateral;
* cabeçalho;
* cards de indicadores;
* tabelas;
* filtros;
* botões;
* badges de status;
* modais;
* listas de EPIs;
* cards de câmeras e setores.

Essa padronização melhora a navegação e facilita a compreensão do sistema.

### 4.4 Navegação

A navegação foi estruturada com menu lateral fixo, permitindo acesso rápido às principais áreas do sistema:

* Dashboard;
* Monitoramento;
* Alertas;
* Ocorrências;
* Colaboradores;
* EPIs;
* Relatórios;
* Câmeras e Áreas;
* Configurações.

Além disso, foram utilizados breadcrumbs para indicar o caminho da tela atual, como “PrevIA > Colaboradores > Detalhe do Colaborador” e “PrevIA > Ocorrências > Detalhe da Ocorrência”.

---

## 5. Relação com as Personas

### Carlos Henrique — Operador de Chão de Fábrica

Carlos aparece como colaborador monitorado pelo sistema. Seu perfil foi usado no fluxo de alerta de risco, em que o sistema detecta ausência de capacete no setor de Produção.

### Mariana Oliveira — Supervisora de Segurança

Mariana é a principal usuária operacional do sistema. Ela acompanha o dashboard, visualiza alertas, consulta ocorrências e registra ações preventivas.

### Roberto Almeida — Gestor Industrial

Roberto está relacionado principalmente ao fluxo de relatórios. O painel de conformidade e o relatório detalhado ajudam na análise de indicadores e apoio à tomada de decisão.

### Fernanda Lima — Administradora do Sistema

Fernanda está relacionada às telas de gestão, como cadastro de EPIs, colaboradores, câmeras e áreas monitoradas. Essas telas representam as funções administrativas previstas na Sprint 1.

---

## 6. Mapeamento entre Telas e Casos de Uso da Sprint 1

| Caso de Uso                               | Tela relacionada no protótipo                        |
| ----------------------------------------- | ---------------------------------------------------- |
| UC01 — Monitorar ambiente industrial      | Monitoramento em Tempo Real                          |
| UC02 — Detectar colaborador               | Monitoramento em Tempo Real                          |
| UC03 — Verificar uso de EPIs              | Monitoramento em Tempo Real / Detalhe do Colaborador |
| UC04 — Identificar ausência de EPI        | Monitoramento / Detalhe da Ocorrência                |
| UC05 — Detectar situação de risco         | Alertas / Ocorrências                                |
| UC06 — Emitir alerta preventivo           | Alertas e Notificações / Detalhe da Ocorrência       |
| UC07 — Registrar ocorrência               | Detalhe da Ocorrência / Histórico de Ocorrências     |
| UC08 — Consultar dashboard                | Dashboard de Monitoramento                           |
| UC09 — Consultar histórico de ocorrências | Histórico de Ocorrências                             |
| UC10 — Gerar relatório de segurança       | Relatórios / Relatório Detalhado                     |
| UC11 — Cadastrar colaboradores            | Colaboradores                                        |
| UC12 — Cadastrar EPIs obrigatórios        | Gestão de EPIs / Editar EPIs do Colaborador          |
| UC13 — Configurar câmeras                 | Câmeras e Áreas Monitoradas                          |

---

## 7. Relação com o Diagrama de Atividades

O fluxo de emissão de alerta preventivo foi representado no protótipo seguindo a lógica do Diagrama de Atividades da Sprint 1:

1. câmera captura imagem ou vídeo;
2. sistema processa a imagem;
3. colaborador é identificado;
4. EPIs obrigatórios são verificados;
5. ausência de EPI é detectada;
6. alerta preventivo é gerado;
7. ocorrência é registrada;
8. alerta aparece para a supervisora;
9. supervisora analisa a ocorrência;
10. ação preventiva é registrada;
11. ocorrência é encerrada.

No protótipo, esse fluxo é representado com o caso do colaborador Carlos Henrique, identificado sem capacete no setor de Produção.

---

## 8. Relação com o Diagrama de Classes

As telas do protótipo também refletem as principais classes definidas na Sprint 1:

| Classe                | Representação no protótipo                                |
| --------------------- | --------------------------------------------------------- |
| Usuario               | Perfis de acesso no login                                 |
| Supervisor            | Mariana Oliveira, responsável pela análise de alertas     |
| Gestor                | Perfil relacionado à consulta de relatórios               |
| Administrador         | Perfil relacionado à gestão de cadastros e configurações  |
| Colaborador           | Tela de colaboradores e detalhe do Carlos Henrique        |
| AreaMonitorada        | Setores como Produção, Soldagem, Almoxarifado e Expedição |
| Camera                | Tela de Câmeras e Áreas Monitoradas                       |
| EPI                   | Gestão de EPIs e EPIs obrigatórios por colaborador        |
| RegistroMonitoramento | Registro do monitoramento em tempo real                   |
| Ocorrencia            | Histórico e detalhe da ocorrência                         |
| Alerta                | Tela de alertas e notificações                            |
| Relatorio             | Relatórios de conformidade e relatório detalhado          |
| Dashboard             | Dashboard de monitoramento                                |
| SistemaIA             | Representado pela detecção simulada no monitoramento      |

---

## 9. Limitações do Protótipo

O protótipo desenvolvido na Sprint 2 não possui implementação em código, banco de dados ou processamento real de imagens. As interações são simuladas para representar a experiência esperada do usuário.

Algumas ações, como exportar PDF ou atualizar dados após edição, foram representadas visualmente por telas, botões e mensagens de sucesso. Essas ações demonstram o comportamento previsto para uma versão funcional futura do sistema.

Essa abordagem está alinhada à proposta da Sprint 2, que solicita um protótipo navegável e fiel o suficiente para simular a experiência real do usuário.

---

## 10. Conclusão

O protótipo do PrevIA foi desenvolvido para representar uma solução de segurança industrial proativa, mantendo coerência com a modelagem da Sprint 1.

As telas e fluxos criados permitem demonstrar os principais objetivos do sistema: monitorar colaboradores, verificar EPIs, identificar riscos, emitir alertas preventivos, registrar ocorrências, apoiar ações da supervisão e gerar relatórios de conformidade por setor.

Dessa forma, o protótipo atende aos requisitos da Sprint 2 e funciona como artefato de comunicação técnica e de negócio para apresentação da solução a stakeholders industriais.
