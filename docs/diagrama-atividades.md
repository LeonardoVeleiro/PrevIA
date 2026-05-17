# Diagrama de Atividades — PrevIA

## 1. Objetivo

Este documento descreve o Diagrama de Atividades do sistema **PrevIA**, representando o fluxo principal de monitoramento, análise de risco e emissão de alerta preventivo.

O objetivo é demonstrar como o sistema atua desde a captura da imagem até o registro da ocorrência e visualização do alerta pelo supervisor.

---

## 2. Funcionalidade Representada

A funcionalidade escolhida para o Diagrama de Atividades é:

**Emissão de alerta preventivo**

Essa funcionalidade foi escolhida por ser uma das mais importantes do PrevIA, pois representa a proposta central do projeto: antecipar riscos e apoiar a prevenção de acidentes em ambientes industriais.

---

## 3. Fluxo Principal

O fluxo principal do sistema ocorre da seguinte forma:

1. A câmera captura a imagem ou vídeo do ambiente industrial;
2. O sistema processa a imagem capturada;
3. O sistema identifica se há colaborador na área monitorada;
4. Caso não haja colaborador, o sistema continua monitorando;
5. Caso haja colaborador, o sistema verifica o uso de EPIs obrigatórios;
6. O sistema analisa se existe ausência de EPI;
7. O sistema também verifica possíveis situações de risco;
8. Caso não haja irregularidade, o monitoramento continua;
9. Caso exista ausência de EPI ou situação de risco, o sistema gera um alerta preventivo;
10. A ocorrência é registrada no banco de dados;
11. O alerta é exibido no dashboard do supervisor;
12. O supervisor analisa o alerta e toma uma ação preventiva.

---

## 4. Regras do Fluxo

- O monitoramento deve ocorrer de forma contínua;
- A verificação de EPIs só ocorre se um colaborador for identificado;
- O alerta só será gerado se houver ausência de EPI ou situação de risco;
- Toda ocorrência associada a um alerta deve ser registrada;
- O supervisor deve visualizar o alerta para apoiar a tomada de decisão.

---

## 5. Representação em PlantUML

<img width="785" height="800" alt="atividades" src="https://github.com/user-attachments/assets/734e36b8-f1dd-4f28-87c3-37accd1e1afa" />
