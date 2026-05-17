# Requisitos do Sistema

Este documento apresenta os requisitos funcionais e não funcionais do projeto PrevIA.

## 1. Introdução

Este documento apresenta o levantamento de requisitos do sistema **PrevIA**, uma solução inteligente para monitoramento de segurança industrial proativa em tempo real.

O objetivo do sistema é auxiliar empresas no controle do uso correto de Equipamentos de Proteção Individual (EPIs), na identificação de situações de risco e na emissão de alertas preventivos antes que acidentes ocorram.

A proposta está alinhada ao contexto do Challenge 2026, com foco na mudança de uma segurança reativa e punitiva para uma abordagem proativa, preventiva e baseada em dados.

---

## 2. Escopo do Sistema

O PrevIA será desenvolvido para atuar em ambientes industriais, utilizando câmeras, visão computacional e inteligência artificial para monitorar colaboradores em campo.

O sistema deverá:

- Capturar imagens ou vídeos do ambiente industrial;
- Detectar colaboradores presentes na área monitorada;
- Verificar o uso correto de EPIs obrigatórios;
- Identificar situações de risco;
- Emitir alertas em tempo real;
- Registrar ocorrências;
- Disponibilizar informações em um dashboard;
- Gerar dados para relatórios de segurança.

---

## 3. Fontes para Levantamento dos Requisitos

Os requisitos foram levantados com base em:

- Análise do problema apresentado no Challenge 2026;
- Estudo do contexto de segurança industrial proativa;
- Discussões internas do grupo;
- Personas fictícias representando usuários do sistema;
- Necessidades de operadores, supervisores de segurança e gestores industriais.

---

## 4. Requisitos Funcionais

| Código | Requisito Funcional | Descrição |
|------|----------------------|-----------|
| RF01 | Detectar colaboradores | O sistema deve identificar a presença de colaboradores nas imagens captadas pelas câmeras. |
| RF02 | Verificar uso de EPIs | O sistema deve verificar se o colaborador está utilizando os EPIs obrigatórios, como capacete, colete e luvas. |
| RF03 | Identificar ausência de EPI | O sistema deve identificar quando um colaborador estiver sem um ou mais EPIs obrigatórios. |
| RF04 | Detectar situações de risco | O sistema deve identificar situações de risco, como permanência em áreas restritas ou postura inadequada. |
| RF05 | Emitir alertas em tempo real | O sistema deve emitir alertas imediatos quando identificar uma irregularidade ou risco. |
| RF06 | Registrar ocorrências | O sistema deve registrar automaticamente as ocorrências detectadas, armazenando data, horário, tipo de risco e colaborador envolvido, quando possível. |
| RF07 | Exibir dashboard de monitoramento | O sistema deve disponibilizar um painel para supervisores acompanharem alertas, ocorrências e indicadores. |
| RF08 | Gerar relatórios de segurança | O sistema deve permitir a geração de relatórios com histórico de ocorrências e indicadores de conformidade. |
| RF09 | Cadastrar colaboradores | O sistema deve permitir o cadastro de colaboradores monitorados. |
| RF10 | Cadastrar EPIs obrigatórios | O sistema deve permitir o cadastro dos EPIs exigidos para cada área ou função. |
| RF11 | Consultar histórico de ocorrências | O sistema deve permitir que supervisores e gestores consultem ocorrências registradas anteriormente. |
| RF12 | Classificar nível de risco | O sistema deve classificar as ocorrências por nível de criticidade, como baixo, médio ou alto. |

---

## 5. Requisitos Não Funcionais

| Código | Requisito Não Funcional | Descrição |
|------|--------------------------|-----------|
| RNF01 | Desempenho | O sistema deve processar as imagens em tempo próximo ao real, permitindo a emissão rápida de alertas. |
| RNF02 | Usabilidade | O dashboard deve apresentar informações de forma clara, objetiva e fácil de interpretar. |
| RNF03 | Confiabilidade | O sistema deve manter registros consistentes das ocorrências detectadas. |
| RNF04 | Escalabilidade | A solução deve permitir futura expansão para novas câmeras, áreas industriais e tipos de EPIs. |
| RNF05 | Segurança da informação | O sistema deve proteger os dados dos colaboradores e registros de ocorrências. |
| RNF06 | Disponibilidade | O sistema deve permanecer disponível durante o período de operação industrial monitorado. |
| RNF07 | Manutenibilidade | O código e a documentação devem ser organizados para facilitar futuras melhorias e correções. |
| RNF08 | Compatibilidade | O sistema deve ser compatível com câmeras comuns e infraestrutura computacional acessível para prototipação. |
| RNF09 | Privacidade | O uso de imagens de colaboradores deve considerar boas práticas de privacidade e adequação à LGPD. |
| RNF10 | Precisão | O sistema deve buscar reduzir falsos positivos e falsos negativos na detecção de EPIs e riscos. |

---

## 6. Regras de Negócio

| Código | Regra de Negócio | Descrição |
|------|------------------|-----------|
| RN01 | Uso obrigatório de EPI | Cada área ou função deve possuir uma lista de EPIs obrigatórios. |
| RN02 | Geração de alerta | Um alerta deve ser gerado sempre que for detectada ausência de EPI obrigatório ou situação de risco. |
| RN03 | Registro de ocorrência | Toda ocorrência identificada pelo sistema deve ser registrada para consulta posterior. |
| RN04 | Classificação de risco | Ocorrências devem ser classificadas conforme seu nível de criticidade. |
| RN05 | Acesso por perfil | Supervisores devem visualizar alertas e ocorrências, enquanto gestores devem acessar relatórios e indicadores consolidados. |
| RN06 | Monitoramento contínuo | O sistema deve manter o monitoramento ativo enquanto a área industrial estiver em operação. |

---

## 7. Atores do Sistema

| Ator | Descrição |
|----|-----------|
| Operador de Chão de Fábrica | Colaborador monitorado pelo sistema durante suas atividades no ambiente industrial. |
| Supervisor de Segurança | Usuário responsável por acompanhar alertas, verificar ocorrências e agir preventivamente. |
| Gestor Industrial | Usuário responsável por analisar relatórios, indicadores e apoiar decisões estratégicas de segurança. |
| Sistema de IA | Módulo responsável por processar imagens, detectar EPIs, identificar riscos e gerar alertas. |

---

## 8. Priorização dos Requisitos

| Prioridade | Requisitos |
|-----------|------------|
| Alta | RF01, RF02, RF03, RF05, RF06, RF07 |
| Média | RF04, RF08, RF11, RF12 |
| Baixa | RF09, RF10 |

