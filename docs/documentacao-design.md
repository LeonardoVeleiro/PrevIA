# Documentação de Design — Sprint 3
## Evolução do Protótipo e Refinamentos de UX/UI

---

## 1. Objetivo do Documento e da Evolução

Este documento apresenta a evolução do protótipo de alta fidelidade do **PrevIA** desenvolvido no Figma para a **Sprint 3**, detalhando as novas telas, fluxos secundários, refinamentos de usabilidade (UX) e o alinhamento com os requisitos consolidados nas Sprints anteriores.

Na Sprint 3, o foco foi transitar de um protótipo com regras estáticas e visão pontual para uma experiência operacional completa no contexto da Metaindústria. O protótipo passou a contemplar o fechamento do ciclo de segurança: **parametrização modular por área de risco**, **explicabilidade de inferência da IA (Explainable AI com bounding boxes)** e **auditoria e despacho formal de medidas corretivas/preventivas**.

---

## 2. Mapa de Telas (Atualizado - Sprint 3)

| Tela / Componente | Objetivo | Status na Sprint 3 |
|---|---|---|
| Login | Acesso simulado com autenticação por perfil (Supervisor, Gestor, Administrador). | Mantido da Sprint 2 |
| Dashboard de Monitoramento | Visão consolidada de indicadores de segurança, alertas ativos e conformidade em tempo real. | Refinado |
| Monitoramento em Tempo Real | Simulação de stream de vídeo com identificação de colaboradores e ausência de EPIs. | Mantido da Sprint 2 |
| Alertas e Notificações | Central de alertas disparados pela visão computacional. | Refinado |
| Histórico de Ocorrências | Consulta e filtragem avançada de eventos registrados. | Mantido da Sprint 2 |
| **Parametrização de EPIs por Área/Câmera** | **Configuração dinâmica da matriz de EPIs obrigatórios por setor fabril e vínculo com fluxos RTSP de câmeras.** | **Nova Tela (Sprint 3)** |
| **Auditoria e Triagem da Ocorrência** | **Visualização do frame de evidência estático com bounding boxes, scores de acurácia da IA e validação de incidentes.** | **Nova Tela (Sprint 3)** |
| **Despacho de Ação Preventiva** | **Formulário de encaminhamento operacional, orientações ao colaborador e contestação de falsos positivos.** | **Nova Tela (Sprint 3)** |
| Colaboradores & Detalhe | Gestão cadastral e consulta de dados funcionais. | Mantido da Sprint 2 |
| Relatórios de Conformidade | Dashboard analítico com taxas de adesão à NR-1 por período e setor. | Mantido da Sprint 2 |
| Relatório Detalhado | Laudo consolidado com gráficos e recomendações para exportação. | Mantido da Sprint 2 |

---

## 3. Novos Fluxos Navegáveis e Justificativas de UX (Sprint 3)

Em conformidade com as diretrizes da Sprint 3, foram implementados ao menos **dois novos fluxos secundários** para cobrir lacunas operacionais identificadas nos feedbacks da entrega anterior:

### 3.1 Novo Fluxo 1: Parametrização Dinâmica de Regras de EPI por Setor e Câmera (UC12 e UC13)
* **Caminho de Navegação:**  
  `Dashboard → Configurações → Câmeras e Áreas → Selecionar Área (ex.: Estamparia) → Parametrizar EPIs Obrigatórios → Salvar Regras`
* **Descrição da Interface:**  
  O Administrador do sistema visualiza as áreas da fábrica e as câmeras IP/RTSP associadas. Ao editar uma área, abre-se a matriz de seleção de EPIs (Capacete, Protetor Auricular, Óculos de Proteção, Luvas de Raspa, Botina com Biqueira e Máscara Respiratória). O sistema permite delimitar zonas de risco específicas dentro do enquadramento visual da câmera (*geofencing*).
* **Justificativa de UX e Negócio:**  
  > *Na Sprint anterior, as regras de segurança eram aplicadas de maneira homogênea por colaborador ou de forma global para a fábrica. Em ambientes reais da Metaindústria, cada setor possui riscos distintos (ex.: o setor de pintura exige proteção respiratória, enquanto a estamparia demanda protetor auricular e botina reforçada). Essa evolução de usabilidade elimina falsos positivos em áreas que não exigem certos EPIs, previne a fadiga de alertas por parte dos supervisores e confere flexibilidade operacional.*

---

### 3.2 Novo Fluxo 2: Auditoria de Imagem com Bounding Box e Despacho de Ação (UC07, UC09 e UC10)
* **Caminho de Navegação:**  
  `Dashboard → Alertas Recentes → Ver Detalhe da Ocorrência → Painel de Validação da IA → Registrar Conduta Preventiva → Concluir e Atualizar Status`
* **Descrição da Interface:**  
  Ao clicar em um alerta preventivo, o Supervisor visualiza o frame de evidência estático capturado no momento da infração. A interface desenha *bounding boxes* (caixas delimitadoras) coloridas sobre a imagem destacando a não conformidade (ex.: retângulo vermelho indicando *"Ausência de Capacete — Confiança 94%"*).  
  A tela oferece botões rápidos de validação (*Confirmar Risco*, *Falso Positivo* ou *Risco Mitigado*) e um modal para registro formal da ação preventiva adotada (ex.: substituição de EPI quebrado, diálogo de segurança ou interrupção de equipamento).
* **Justificativa de UX e Negócio:**  
  > *O protótipo da Sprint 2 encerrava a interação na mera exibição do alerta na tela, gerando um vácuo no fluxo operacional. Esse novo fluxo atende às exigências normativas da NR-1 (Gerenciamento de Riscos Ocupacionais), permitindo que a detecção do modelo de Visão Computacional se converta em ação prática, rastreável e auditável. Além disso, a explicabilidade visual (XAI) do bounding box aumenta a confiança do supervisor no sistema.*

---

## 4. Refinamentos de UX/UI Adotados na Sprint 3

### 4.1 Explicabilidade da Inteligência Artificial (Explainable AI - XAI)
* **Feedback Incorporado:** O usuário necessita compreender o motivo exato pelo qual a inteligência artificial acionou uma notificação crítica.
* **Solução de Interface:** Exibição da métrica de acurácia da inferência (ex.: *Acurácia: 94%*) e caixas delimitadoras coloridas em volta das áreas corporais do trabalhador na foto da ocorrência.

### 4.2 Prevenção de Fadiga de Alertas e Redução de Atrito
* Adoção de triagem visual categorizada por cores de criticidade (Crítico, Alto, Médio e Atenção) e disponibilização de botão de descarte rápido caso o supervisor identifique uma oclusão ou falso positivo, alimentando a base para re-treinamento do modelo.

### 4.3 Design System e Consistência
* Criação de novos componentes reutilizáveis no Figma:
  * Componente de *Bounding Box* visual;
  * Modal padronizado de *Despacho de Ordem/Ação Preventiva*;
  * Seletor em formato de *Chips* / *Tags* para inclusão/exclusão dinâmica de EPIs obrigatórios.

---

## 5. Mapeamento Atualizado entre Telas e Casos de Uso (Sprint 3)

| Caso de Uso | Tela Relacionada no Protótipo | Status de Cobertura |
|---|---|---|
| UC01 — Monitorar ambiente industrial | Monitoramento em Tempo Real | Coberto na Sprint 2 |
| UC02 — Detectar colaborador | Monitoramento em Tempo Real | Coberto na Sprint 2 |
| UC03 — Verificar uso de EPIs | Monitoramento / Detalhe do Colaborador | Coberto na Sprint 2 |
| UC04 — Identificar ausência de EPI | Monitoramento / Auditoria da Ocorrência | Refinado na Sprint 3 |
| UC05 — Detectar situação de risco | Alertas / Ocorrências | Refinado na Sprint 3 |
| UC06 — Emitir alerta preventivo | Alertas e Notificações | Coberto na Sprint 2 |
| UC07 — Registrar ocorrência | Auditoria da Ocorrência / Histórico | Refinado na Sprint 3 |
| UC08 — Consultar dashboard | Dashboard de Monitoramento | Refinado na Sprint 3 |
| UC09 — Consultar histórico de ocorrências | Histórico de Ocorrências | Refinado na Sprint 3 |
| UC10 — Gerar relatório de segurança | Relatórios / Relatório Detalhado | Coberto na Sprint 2 |
| UC11 — Cadastrar colaboradores | Colaboradores | Coberto na Sprint 2 |
| **UC12 — Cadastrar EPIs obrigatórios** | **Parametrização de EPIs por Área/Câmera** | **Evoluído na Sprint 3** |
| **UC13 — Configurar câmeras** | **Parametrização de EPIs por Área/Câmera** | **Evoluído na Sprint 3** |

---

## 6. Relação com o Modelo Lógico (Diagrama de Classes Refinado)

As telas e fluxos adicionados na Sprint 3 possuem correspondência direta com as entidades atualizadas no Diagrama de Classes:

* **`AreaMonitorada` e `Camera`:** A tela de parametrização implementa visualmente os métodos `definirEPIsObrigatorios()` e a associação direta entre a área e a lista de câmeras RTSP.
* **`Ocorrencia`:** A tela de auditoria reflete os novos atributos de banco de dados modelados:
  * `statusValidacao` (Pendente, Confirmado, Falso Positivo, Mitigado);
  * `urlFrameEvidencia` (imagem capturada pela IA com marcações);
  * `acaoTomada` (medida preventiva digitada e arquivada pelo supervisor).

---

## 7. Conclusão

A evolução do protótipo na Sprint 3 permitiu validar cenários operacionais complexos, eliminando limitações da versão anterior. A integração de fluxos de configuração modular e auditoria detalhada de evidências consolidou o PrevIA como uma solução madura, intuitiva e plenamente alinhada às necessidades da indústria 4.0.
