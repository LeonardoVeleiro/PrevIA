# PrevIA  
## Inteligência que antecipa riscos e protege vidas

---

## Integrantes

- Agatha Cassari Benedicto — RM 556251  
- Gustavo Shinn Shyong Cheng — RM 559084  
- Leonardo Fernandes Veleiro — RM 557773  
- Sara Barbosa da Silva — RM 559042  

---

## Desafio

Desenvolver um sistema inteligente para o monitoramento de segurança proativa do trabalho em ambientes industriais.

O projeto está alinhado ao contexto do Challenge 2026, com foco na transição de uma segurança reativa e punitiva para uma abordagem proativa, preventiva e baseada em dados.

---

## Problema Abordado

No ambiente industrial, a segurança do trabalho ainda é frequentemente tratada de forma reativa. Muitas empresas dependem de inspeções periódicas, checklists manuais e ações corretivas somente após a ocorrência de acidentes ou infrações.

Esse modelo apresenta diversos problemas, como:

- Identificação tardia de riscos;
- Falta de monitoramento contínuo;
- Dependência excessiva da observação humana;
- Maior chance de falhas operacionais;
- Custos elevados com acidentes, paralisações, multas e afastamentos;
- Cultura punitiva, que pode desestimular o relato de incidentes.

Dessa forma, existe a necessidade de uma solução capaz de identificar riscos em tempo real, apoiar a prevenção de acidentes e fortalecer uma cultura de segurança proativa.

---

## Proposta de Solução

O **PrevIA** é um sistema inteligente de monitoramento industrial em tempo real que utiliza visão computacional e inteligência artificial para identificar situações de risco e verificar o uso correto de Equipamentos de Proteção Individual, os EPIs.

A solução propõe o uso de câmeras posicionadas no ambiente industrial para capturar imagens dos colaboradores em campo. Essas imagens são processadas por algoritmos de visão computacional capazes de detectar pessoas, identificar EPIs obrigatórios e reconhecer possíveis comportamentos de risco.

Quando uma situação irregular é identificada, o sistema emite alertas imediatos para supervisores e registra a ocorrência para consulta posterior, geração de relatórios e acompanhamento de indicadores de segurança.

---

## Objetivo Geral

Desenvolver um sistema inteligente capaz de apoiar a segurança industrial proativa por meio do monitoramento em tempo real, identificação automática de riscos e emissão de alertas preventivos.

---

## Objetivos Específicos

- Detectar colaboradores em ambiente industrial por meio de câmeras;
- Verificar automaticamente o uso correto de EPIs;
- Identificar situações de risco, como ausência de equipamentos obrigatórios ou comportamento inadequado em áreas perigosas;
- Emitir alertas em tempo real para supervisores;
- Registrar ocorrências para análise posterior;
- Gerar dados para relatórios e indicadores de segurança;
- Apoiar a tomada de decisão dos gestores industriais;
- Reduzir a dependência de inspeções manuais e ações apenas corretivas.

---

## Público-Alvo

O sistema PrevIA é voltado para ambientes industriais que necessitam de monitoramento contínuo de segurança.

Os principais usuários da solução são:

- Operadores de chão de fábrica;
- Supervisores de segurança do trabalho;
- Gestores industriais;
- Administradores do sistema.

---

## Funcionamento Geral do Sistema

O funcionamento do PrevIA segue o seguinte fluxo:

1. A câmera captura imagens do ambiente industrial;
2. O sistema identifica a presença de colaboradores;
3. O algoritmo de visão computacional verifica o uso correto dos EPIs;
4. O sistema analisa possíveis situações de risco;
5. Caso uma irregularidade seja detectada, um alerta é gerado;
6. A ocorrência é registrada no banco de dados;
7. Supervisores acompanham os alertas e indicadores por meio de um dashboard;
8. Gestores podem consultar relatórios e históricos de conformidade.

---

## Tecnologias Utilizadas

| Tecnologia | Finalidade |
|-----------|------------|
| Python | Linguagem principal para desenvolvimento da inteligência artificial, visão computacional e backend |
| OpenCV | Captura, leitura e processamento de imagens e vídeos |
| YOLO | Detecção de objetos em tempo real, como pessoas e EPIs |
| MediaPipe Pose ou YOLO Pose | Análise de postura e comportamento de risco |
| FastAPI | Criação da API backend do sistema |
| PostgreSQL | Armazenamento de colaboradores, alertas, ocorrências e relatórios |
| React.js | Desenvolvimento do dashboard web |
| WebSocket | Comunicação em tempo real entre backend e dashboard |
| GitHub | Versionamento, organização e documentação do projeto |
| Draw.io ou PlantUML | Criação dos diagramas UML |

A stack tecnológica apresentada representa uma proposta inicial da equipe e poderá ser ajustada ao longo do desenvolvimento, conforme testes, limitações técnicas e decisões futuras do projeto.

Mais detalhes estão disponíveis em:

[docs/tecnologias.md](docs/tecnologias.md)

---

## Documentação do Projeto

A documentação completa da Sprint 1 está organizada na pasta `docs`.

| Documento | Descrição |
|----------|-----------|
| [Requisitos](docs/requisitos.md) | Requisitos funcionais, não funcionais, regras de negócio e atores do sistema |
| [Tecnologias](docs/tecnologias.md) | Stack tecnológica e justificativa técnica |
| [Personas](docs/personas.md) | Perfis dos usuários envolvidos no sistema |
| [Restrições](docs/restricoes.md) | Limitações, premissas e restrições do projeto |
| [Diagrama de Casos de Uso](docs/diagrama-casos-de-uso.md) | Descrição dos atores, casos de uso e relacionamentos include/extend |
| [Diagrama de Atividades](docs/diagrama-atividades.md) | Fluxo de emissão de alerta preventivo |
| [Diagrama de Classes](docs/diagrama-classes.md) | Estrutura de classes, atributos, métodos e relacionamentos |

---

## Diagramas UML

Os diagramas UML foram desenvolvidos para representar o funcionamento e a estrutura do sistema PrevIA.

### Diagrama de Casos de Uso

Representa os principais atores do sistema, suas interações e os relacionamentos entre os casos de uso.

![Diagrama de Casos de Uso](diagramas/caso-de-uso.png)

---

### Diagrama de Atividades

Representa o fluxo principal de monitoramento, análise de risco e emissão de alerta preventivo.

![Diagrama de Atividades](diagramas/atividades.png)

---

### Diagrama de Classes

Representa as principais entidades do sistema, seus atributos, métodos e relacionamentos.

![Diagrama de Classes](diagramas/classes.png)

---

---

## Sprint 2 — Protótipo Navegável

Na Sprint 2, o projeto PrevIA evoluiu da modelagem inicial para um protótipo navegável desenvolvido no Figma.

O objetivo desta etapa foi representar visualmente os principais fluxos do sistema, mantendo coerência com os requisitos, personas, casos de uso, diagrama de atividades e diagrama de classes definidos na Sprint 1.

---

## Objetivo do Protótipo

O protótipo tem como objetivo simular a experiência de uso do sistema PrevIA, permitindo visualizar como supervisores, gestores e administradores interagem com a solução de segurança industrial proativa.

O foco principal está na validação da navegação, organização das informações e clareza dos fluxos relacionados ao monitoramento de EPIs, emissão de alertas e geração de relatórios.

---

## Fluxos Representados

O protótipo cobre os três fluxos principais solicitados na Sprint 2:

1. Cadastro e consulta de EPI por colaborador;
2. Emissão e visualização de alerta de risco;
3. Geração de relatório de conformidade por setor.

---

## Telas Principais

As principais telas desenvolvidas no protótipo são:

* Login;
* Dashboard de Monitoramento;
* Monitoramento em Tempo Real;
* Alertas e Notificações;
* Histórico de Ocorrências;
* Detalhe da Ocorrência;
* Registro de Ação Preventiva;
* Colaboradores;
* Detalhe do Colaborador;
* Edição de EPIs do Colaborador;
* Gestão de EPIs;
* Relatórios de Conformidade;
* Relatório Detalhado;
* Câmeras e Áreas Monitoradas.

---

## Instruções de Navegação do Protótipo

Para testar o protótipo, recomenda-se seguir os fluxos abaixo.

### Fluxo 1 — Cadastro e Consulta de EPI por Colaborador

Login → Dashboard → Colaboradores → Carlos Henrique → Editar EPIs → Salvar alterações → Detalhe do Colaborador

Esse fluxo demonstra a consulta dos EPIs obrigatórios de um colaborador e a simulação da edição dos EPIs vinculados.

### Fluxo 2 — Emissão e Visualização de Alerta de Risco

Dashboard → Monitoramento → Ver Alerta Preventivo → Detalhe da Ocorrência → Registrar Ação Preventiva → Salvar ação → Ocorrência Resolvida

Esse fluxo representa a detecção de ausência de capacete, geração de alerta preventivo, registro de ocorrência e tomada de ação pela supervisora de segurança.

### Fluxo 3 — Relatório de Conformidade por Setor

Dashboard → Relatórios → Gerar Relatório → Relatório Detalhado

Esse fluxo representa a geração de um relatório de conformidade por setor, com indicadores, ocorrências e recomendações preventivas.

---

## Link do Protótipo

Link do protótipo no Figma:

https://www.figma.com/make/WKn2i6gkAbUXN4ECFAkarC/Review-idea-from-text-file?code-node-id=0-9&p=f&t=5ivuy0KCbHPFA5Uy-0&fullscreen=1

---

## Documentação de Design

A documentação de design da Sprint 2 está disponível em:

`docs/documentacao-design.md`

Esse documento apresenta o mapa de telas, decisões de UX/UI e o mapeamento entre as telas do protótipo e os casos de uso da Sprint 1.

---

## Observação sobre o Protótipo

O protótipo desenvolvido na Sprint 2 não possui implementação em código, banco de dados ou processamento real de imagens. As interações representam a experiência esperada do usuário em uma versão funcional futura do sistema.

A área de câmera e os botões de exportação ou salvamento são simulações visuais, utilizadas para demonstrar o fluxo navegável exigido nesta etapa.

---

## Estrutura do Repositório

```text
PrevIA/
├── README.md
├── entrega.txt
├── docs/
│   ├── requisitos.md
│   ├── tecnologias.md
│   ├── personas.md
│   ├── restricoes.md
│   ├── diagrama-casos-de-uso.md
│   ├── diagrama-atividades.md
│   ├── diagrama-classes.md
│   └── documentacao-design.md
└── diagramas/
    ├── caso-de-uso.png
    ├── atividades.png
    └── classes.png
```

---

## Status do Projeto

Projeto em desenvolvimento acadêmico.

A Sprint 1 contemplou a documentação, modelagem e definição inicial da solução.
A Sprint 2 contemplou a criação do protótipo navegável e a documentação de design.
