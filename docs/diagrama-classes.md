# Diagrama de Classes — PrevIA

## 1. Objetivo

Este documento descreve o Diagrama de Classes do sistema **PrevIA**, apresentando as principais entidades, atributos, métodos e relacionamentos da solução.

O diagrama tem como objetivo representar a estrutura lógica do sistema, servindo como base para o desenvolvimento futuro da aplicação.

---

## 2. Principais Classes

O sistema PrevIA possui classes relacionadas ao monitoramento industrial, controle de colaboradores, verificação de EPIs, emissão de alertas, registro de ocorrências e geração de relatórios.

As principais classes são:

- Usuario
- Supervisor
- Gestor
- Administrador
- Colaborador
- AreaMonitorada
- Camera
- EPI
- RegistroMonitoramento
- Ocorrencia
- Alerta
- Relatorio
- Dashboard
- SistemaIA

---

## 3. Descrição das Classes

| Classe | Descrição |
|------|-----------|
| Usuario | Representa um usuário do sistema com acesso ao dashboard ou funções administrativas. |
| Supervisor | Usuário responsável por acompanhar alertas e ocorrências. |
| Gestor | Usuário responsável por consultar relatórios e indicadores. |
| Administrador | Usuário responsável por cadastrar dados e configurar o sistema. |
| Colaborador | Representa o trabalhador monitorado no ambiente industrial. |
| AreaMonitorada | Representa uma área industrial acompanhada por câmeras. |
| Camera | Representa o dispositivo responsável por capturar imagens. |
| EPI | Representa os equipamentos de proteção individual exigidos. |
| RegistroMonitoramento | Representa um registro de análise feita pelo sistema. |
| Ocorrencia | Representa uma irregularidade ou situação de risco identificada. |
| Alerta | Representa o alerta gerado a partir de uma ocorrência. |
| Relatorio | Representa relatórios de segurança e conformidade. |
| Dashboard | Representa a interface de acompanhamento dos dados. |
| SistemaIA | Representa o módulo responsável por processar imagens e detectar riscos. |

---

## 4. Representação em PlantUML

<img width="1203" height="1406" alt="classes 2" src="https://github.com/user-attachments/assets/9be265e5-fd7e-4614-adad-efbc0af45ea1" />
