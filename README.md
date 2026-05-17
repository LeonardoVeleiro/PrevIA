# PrevIA  
## Inteligência que antecipa riscos e protege vidas

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

O PrevIA é um sistema inteligente de monitoramento industrial em tempo real que utiliza visão computacional e inteligência artificial para identificar situações de risco e verificar o uso correto de Equipamentos de Proteção Individual, os EPIs.

A solução propõe o uso de câmeras posicionadas no ambiente industrial para capturar imagens dos colaboradores em campo. Essas imagens são processadas por algoritmos de visão computacional capazes de detectar pessoas, identificar EPIs obrigatórios e reconhecer possíveis comportamentos de risco.

Quando uma situação irregular é identificada, o sistema emite alertas imediatos para supervisores e registra a ocorrência para consulta posterior, geração de relatórios e acompanhamento de indicadores de segurança.

---

## Objetivos do Projeto

### Objetivo Geral

Desenvolver um sistema inteligente capaz de apoiar a segurança industrial proativa por meio do monitoramento em tempo real, identificação automática de riscos e emissão de alertas preventivos.

### Objetivos Específicos

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

O sistema PrevIA é voltado para ambientes industriais que necessitam de monitoramento contínuo de segurança. Os principais usuários da solução são:

- Operadores de chão de fábrica;
- Supervisores de segurança do trabalho;
- Gestores industriais;
- Equipes responsáveis por prevenção de acidentes e conformidade operacional.

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
| Python | Linguagem principal para desenvolvimento da inteligência artificial e processamento de imagens |
| OpenCV | Captura, leitura e processamento de imagens e vídeos |
| YOLO | Detecção de objetos em tempo real, como pessoas e EPIs |
| MediaPipe Pose ou YOLO Pose | Análise de postura e comportamento de risco |
| FastAPI | Criação da API backend do sistema |
| PostgreSQL | Armazenamento de colaboradores, alertas, ocorrências e relatórios |
| React.js | Desenvolvimento do dashboard web |
| WebSocket | Comunicação em tempo real entre backend e dashboard |
| GitHub | Versionamento, organização e documentação do projeto |
| Draw.io ou PlantUML | Criação dos diagramas UML |

---

## Justificativa Técnica das Tecnologias

Python foi escolhido por ser uma linguagem amplamente utilizada em projetos de inteligência artificial, visão computacional e análise de dados. Sua grande quantidade de bibliotecas facilita o desenvolvimento de soluções inteligentes e permite uma prototipação mais rápida.

OpenCV será utilizado para captura e processamento de imagens em tempo real, permitindo a integração com câmeras e o tratamento dos frames antes da análise pela inteligência artificial.

YOLO foi selecionado por ser um modelo eficiente para detecção de objetos em tempo real. Ele é adequado para identificar colaboradores e EPIs, como capacetes, coletes, luvas e outros equipamentos de segurança.

MediaPipe Pose ou YOLO Pose poderão ser utilizados para análise corporal e identificação de comportamentos de risco, como postura inadequada ou movimentação perigosa próxima a áreas restritas.

FastAPI será utilizado no backend por ser um framework leve, rápido e compatível com Python, facilitando a comunicação entre o módulo de inteligência artificial, o banco de dados e o dashboard.

PostgreSQL foi escolhido por ser um banco de dados relacional robusto, confiável e adequado para armazenar informações estruturadas, como usuários, ocorrências, alertas e relatórios.

React.js será utilizado no desenvolvimento do dashboard, permitindo a criação de uma interface moderna e interativa para acompanhamento dos alertas e indicadores de segurança.

WebSocket será utilizado para permitir comunicação em tempo real, garantindo que os alertas sejam enviados imediatamente ao painel do supervisor.

---

## Requisitos do Sistema

A documentação completa dos requisitos funcionais e não funcionais está disponível no arquivo:

[docs/requisitos.md](docs/requisitos.md)

---

## Personas

As personas do projeto representam os principais usuários do sistema, como operador de chão de fábrica, supervisor de segurança e gestor industrial.

A documentação completa está disponível em:

[docs/personas.md](docs/personas.md)

---

## Restrições do Sistema

As limitações e restrições técnicas do projeto estão documentadas em:

[docs/restricoes.md](docs/restricoes.md)

---

## Diagramas UML

Os diagramas UML do projeto serão armazenados na pasta `diagramas`.

### Diagramas previstos

- Diagrama de Casos de Uso;
- Diagrama de Atividades;
- Diagrama de Classes.

Pasta dos diagramas:

[diagramas](diagramas)

---

## Estrutura do Repositório

```txt
PrevIA/
│
├── README.md
├── entrega.txt
│
├── docs/
│   ├── requisitos.md
│   ├── tecnologias.md
│   ├── personas.md
│   └── restricoes.md
│
└── diagramas/
    ├── caso-de-uso.png
    ├── atividades.png
    └── classes.png
