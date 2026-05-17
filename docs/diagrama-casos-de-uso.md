# Diagrama de Casos de Uso — PrevIA

## 1. Objetivo

Este documento descreve o Diagrama de Casos de Uso do sistema **PrevIA**, identificando os principais atores, funcionalidades e relacionamentos do sistema.

O diagrama tem como objetivo representar como os usuários interagem com a solução de monitoramento inteligente de segurança industrial proativa.

---

## 2. Atores do Sistema

| Ator | Descrição |
|----|-----------|
| Operador de Chão de Fábrica | Colaborador monitorado pelo sistema durante suas atividades no ambiente industrial. |
| Supervisor de Segurança | Usuário responsável por acompanhar alertas, verificar ocorrências e agir preventivamente. |
| Gestor Industrial | Usuário responsável por consultar relatórios, analisar indicadores e apoiar decisões estratégicas. |
| Administrador do Sistema | Usuário responsável por configurar usuários, câmeras, áreas monitoradas e parâmetros do sistema. |
| Sistema de IA | Módulo responsável por processar imagens, identificar EPIs, detectar riscos e gerar alertas. |

---

## 3. Casos de Uso

| Código | Caso de Uso | Descrição |
|------|-------------|-----------|
| UC01 | Monitorar ambiente industrial | O sistema acompanha continuamente as áreas monitoradas por câmeras. |
| UC02 | Detectar colaborador | O sistema identifica a presença de colaboradores nas imagens capturadas. |
| UC03 | Verificar uso de EPIs | O sistema verifica se o colaborador está utilizando os EPIs obrigatórios. |
| UC04 | Identificar ausência de EPI | O sistema identifica quando um EPI obrigatório não está sendo utilizado. |
| UC05 | Detectar situação de risco | O sistema identifica comportamentos ou condições que podem representar perigo. |
| UC06 | Emitir alerta preventivo | O sistema emite um alerta quando uma irregularidade ou situação de risco é detectada. |
| UC07 | Registrar ocorrência | O sistema registra a ocorrência com informações como data, horário, tipo de risco e área monitorada. |
| UC08 | Consultar dashboard | O supervisor acompanha alertas, ocorrências e indicadores em tempo real. |
| UC09 | Consultar histórico de ocorrências | O supervisor ou gestor consulta registros anteriores de ocorrências. |
| UC10 | Gerar relatório de segurança | O gestor gera relatórios com dados de conformidade, ocorrências e indicadores. |
| UC11 | Cadastrar colaboradores | O administrador cadastra colaboradores no sistema. |
| UC12 | Cadastrar EPIs obrigatórios | O administrador define quais EPIs são obrigatórios por área ou função. |
| UC13 | Configurar câmeras | O administrador configura as câmeras e áreas monitoradas. |

---

## 4. Relacionamentos Include e Extend

### Relacionamentos do tipo include

O relacionamento `include` indica que um caso de uso obrigatoriamente utiliza outro para ser concluído.

| Caso de Uso Principal | Include | Justificativa |
|----------------------|---------|---------------|
| Monitorar ambiente industrial | Detectar colaborador | Para monitorar o ambiente, o sistema precisa identificar colaboradores. |
| Verificar uso de EPIs | Detectar colaborador | Para verificar EPIs, primeiro é necessário detectar o colaborador. |
| Emitir alerta preventivo | Registrar ocorrência | Todo alerta gerado deve ser registrado como ocorrência. |
| Gerar relatório de segurança | Consultar histórico de ocorrências | Relatórios dependem dos dados registrados no histórico. |

### Relacionamentos do tipo extend

O relacionamento `extend` indica uma situação opcional ou condicional.

| Caso de Uso Base | Extend | Condição |
|-----------------|--------|----------|
| Verificar uso de EPIs | Identificar ausência de EPI | Ocorre quando o sistema detecta que o colaborador está sem algum EPI obrigatório. |
| Monitorar ambiente industrial | Detectar situação de risco | Ocorre quando o sistema identifica comportamento ou condição perigosa. |
| Identificar ausência de EPI | Emitir alerta preventivo | Ocorre quando a ausência de EPI representa risco ou descumprimento de segurança. |
| Detectar situação de risco | Emitir alerta preventivo | Ocorre quando o risco identificado exige ação imediata. |

---

## 5. Representação em PlantUML

<img width="1184" height="791" alt="diagrama 2" src="https://github.com/user-attachments/assets/89aa2f84-bdce-4946-b91d-50e8ef2da3e7" />
