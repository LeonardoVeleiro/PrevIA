# Tecnologias Utilizadas

Este documento apresenta a stack tecnológica escolhida para o desenvolvimento do PrevIA.

## 1. Introdução

Este documento apresenta a stack tecnológica escolhida inicialmente para o desenvolvimento do projeto **PrevIA**, um sistema inteligente de monitoramento de segurança industrial proativa.

A escolha das tecnologias considera as necessidades do projeto, como processamento de imagens, inteligência artificial, detecção em tempo real, armazenamento de ocorrências, geração de relatórios e visualização de alertas em dashboard.

As tecnologias apresentadas neste documento representam a proposta inicial da equipe para a Sprint 1. Durante as próximas etapas do projeto, a stack poderá ser ajustada, substituída ou complementada conforme necessidades técnicas, limitações encontradas, desempenho dos testes e orientações recebidas ao longo do desenvolvimento.

---

## 2. Stack Tecnológica

| Tecnologia | Categoria | Finalidade |
|-----------|-----------|------------|
| Python | Linguagem de programação | Desenvolvimento da inteligência artificial, visão computacional e backend |
| OpenCV | Visão computacional | Captura, leitura e processamento de imagens e vídeos |
| YOLO | Inteligência artificial | Detecção de objetos em tempo real, como pessoas e EPIs |
| MediaPipe Pose ou YOLO Pose | Análise corporal | Identificação de postura e comportamentos de risco |
| FastAPI | Backend/API | Criação de APIs para comunicação entre IA, banco de dados e dashboard |
| PostgreSQL | Banco de dados | Armazenamento de colaboradores, alertas, ocorrências e relatórios |
| React.js | Frontend | Desenvolvimento do dashboard web |
| WebSocket | Comunicação em tempo real | Envio imediato de alertas ao dashboard |
| GitHub | Versionamento | Organização do repositório, documentação e controle de versões |
| Draw.io ou PlantUML | Modelagem UML | Criação dos diagramas de Casos de Uso, Atividades e Classes |

---

## 3. Justificativa Técnica

### 3.1 Python

Python foi escolhido como linguagem principal por ser amplamente utilizado em projetos de inteligência artificial, visão computacional, automação e análise de dados.

Além disso, possui grande quantidade de bibliotecas e frameworks que facilitam a implementação de modelos de IA, manipulação de imagens e desenvolvimento de APIs.

No PrevIA, Python será utilizado principalmente para:

- Processamento das imagens;
- Integração com modelos de inteligência artificial;
- Desenvolvimento do backend;
- Tratamento dos dados de monitoramento.

---

### 3.2 OpenCV

OpenCV será utilizado para captura e processamento de imagens e vídeos.

Essa tecnologia permite trabalhar com frames capturados por câmeras, aplicar pré-processamentos nas imagens e preparar os dados visuais para análise pelos modelos de inteligência artificial.

No PrevIA, OpenCV será utilizado para:

- Capturar imagens de câmeras;
- Ler vídeos em tempo real;
- Manipular frames;
- Apoiar a integração entre câmera e modelo de detecção.

---

### 3.3 YOLO

YOLO será utilizado para detecção de objetos em tempo real.

Essa tecnologia é adequada para identificar rapidamente elementos em imagens, como colaboradores e EPIs, incluindo capacetes, coletes, luvas e outros equipamentos de segurança.

No PrevIA, YOLO será utilizado para:

- Detectar pessoas no ambiente industrial;
- Identificar EPIs;
- Verificar ausência de equipamentos obrigatórios;
- Apoiar a geração de alertas preventivos.

---

### 3.4 MediaPipe Pose ou YOLO Pose

MediaPipe Pose ou YOLO Pose poderão ser utilizados para análise corporal e detecção de postura.

Essas tecnologias permitem identificar pontos do corpo humano e analisar movimentos ou posições que possam indicar comportamento de risco.

No PrevIA, essa tecnologia poderá ser utilizada para:

- Identificar postura inadequada;
- Detectar movimentos de risco;
- Apoiar a análise de proximidade com áreas perigosas;
- Complementar a verificação feita pelo modelo de detecção de EPIs.

---

### 3.5 FastAPI

FastAPI foi escolhido para o desenvolvimento do backend por ser um framework moderno, leve e rápido para criação de APIs em Python.

Ele permite criar rotas para comunicação entre o módulo de inteligência artificial, o banco de dados e o dashboard web.

No PrevIA, FastAPI será utilizado para:

- Receber dados gerados pelo módulo de IA;
- Enviar alertas ao dashboard;
- Registrar ocorrências;
- Disponibilizar dados para relatórios;
- Integrar os módulos do sistema.

---

### 3.6 PostgreSQL

PostgreSQL foi escolhido como banco de dados por ser robusto, confiável e adequado para armazenamento de dados estruturados.

Como o sistema precisa armazenar colaboradores, áreas, EPIs, ocorrências, alertas e relatórios, um banco relacional é adequado para manter consistência e organização das informações.

No PrevIA, PostgreSQL será utilizado para armazenar:

- Dados de colaboradores;
- EPIs obrigatórios;
- Áreas monitoradas;
- Alertas emitidos;
- Ocorrências registradas;
- Histórico de conformidade;
- Dados para relatórios.

---

### 3.7 React.js

React.js será utilizado para o desenvolvimento do dashboard web.

A escolha se justifica pela possibilidade de criar interfaces modernas, componentizadas e interativas, facilitando a visualização de alertas, indicadores e relatórios.

No PrevIA, React.js será utilizado para:

- Criar o dashboard do supervisor;
- Exibir alertas em tempo real;
- Apresentar gráficos e indicadores;
- Permitir consulta de ocorrências;
- Melhorar a experiência do usuário.

---

### 3.8 WebSocket

WebSocket será utilizado para comunicação em tempo real entre o backend e o dashboard.

Diferente de uma comunicação tradicional baseada apenas em requisições manuais, o WebSocket permite que o sistema envie alertas automaticamente assim que uma situação de risco for detectada.

No PrevIA, WebSocket será utilizado para:

- Enviar alertas imediatamente ao dashboard;
- Atualizar o painel sem necessidade de recarregar a página;
- Melhorar a resposta preventiva do supervisor;
- Apoiar o monitoramento contínuo.

---

### 3.9 GitHub

GitHub será utilizado para versionamento, organização do projeto e documentação.

O repositório conterá o README, documentos técnicos, diagramas UML e demais arquivos necessários para a entrega da Sprint 1.

No PrevIA, GitHub será utilizado para:

- Armazenar a documentação;
- Organizar arquivos do projeto;
- Controlar versões;
- Compartilhar o trabalho entre os integrantes;
- Disponibilizar o link final para entrega.

---

### 3.10 Draw.io ou PlantUML

Draw.io ou PlantUML serão utilizados para criação dos diagramas UML exigidos na Sprint 1.

Essas ferramentas permitem representar visualmente os casos de uso, fluxos de atividades e estrutura de classes do sistema.

No PrevIA, serão criados:

- Diagrama de Casos de Uso;
- Diagrama de Atividades;
- Diagrama de Classes.

---

## 4. Relação entre Tecnologias e Necessidades do Projeto

| Necessidade do Projeto | Tecnologia Relacionada |
|------------------------|-------------------------|
| Monitoramento por câmera | OpenCV |
| Detecção de colaboradores | YOLO |
| Verificação de EPIs | YOLO |
| Análise de postura | MediaPipe Pose ou YOLO Pose |
| Emissão de alertas | FastAPI e WebSocket |
| Registro de ocorrências | PostgreSQL |
| Dashboard de acompanhamento | React.js |
| Relatórios e histórico | PostgreSQL e React.js |
| Documentação e versionamento | GitHub |
| Modelagem UML | Draw.io ou PlantUML |

---

## 5. Possíveis Alterações Futuras

A stack apresentada neste documento não é definitiva. Ela representa uma proposta inicial coerente com os objetivos da Sprint 1 e com a ideia geral do projeto.

Durante o desenvolvimento, algumas tecnologias poderão ser alteradas caso a equipe identifique opções mais adequadas ou enfrente limitações técnicas.

Exemplos de possíveis mudanças:

- Substituir o banco PostgreSQL por outro banco de dados, caso o protótipo exija uma solução mais simples;
- Trocar React.js por outra tecnologia de interface, caso o grupo opte por um dashboard mais simples;
- Utilizar outra biblioteca ou modelo de visão computacional além do YOLO, caso os testes indiquem melhor desempenho;
- Adicionar novas tecnologias para relatórios, autenticação, integração com sensores ou deploy;
- Ajustar o uso de MediaPipe Pose ou YOLO Pose conforme a viabilidade da análise de postura.

Essas possíveis alterações não comprometem a proposta do projeto, pois a finalidade principal permanece a mesma: desenvolver uma solução inteligente para monitoramento proativo de segurança industrial.
