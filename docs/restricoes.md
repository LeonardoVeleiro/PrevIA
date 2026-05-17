# Restrições do Sistema

Este documento apresenta as limitações e restrições técnicas do projeto PrevIA.

## 1. Introdução

Este documento apresenta as principais restrições, limitações e condições técnicas relacionadas ao desenvolvimento e funcionamento do sistema **PrevIA**.

As restrições são importantes para delimitar o escopo da solução, evitar interpretações incorretas sobre o projeto e demonstrar quais fatores podem impactar o desempenho do sistema em um ambiente industrial real.

---

## 2. Restrições Técnicas

| Código | Restrição | Descrição |
|------|-----------|-----------|
| RT01 | Dependência da qualidade da câmera | A precisão da detecção depende da resolução, posicionamento e qualidade das câmeras utilizadas no ambiente industrial. |
| RT02 | Dependência da iluminação | Ambientes com baixa iluminação, sombras intensas ou reflexos podem prejudicar a identificação de colaboradores e EPIs. |
| RT03 | Capacidade de processamento | O desempenho em tempo real depende do hardware disponível, principalmente CPU, GPU e memória. |
| RT04 | Qualidade do dataset | A precisão da IA depende da qualidade e diversidade das imagens utilizadas para treinamento ou validação do modelo. |
| RT05 | Conexão de rede | Para envio de alertas ao dashboard, o sistema depende de uma rede local ou conexão estável entre os módulos. |
| RT06 | Limitação de ambiente simulado | Nesta etapa do projeto, o sistema será pensado e prototipado em ambiente simulado, não contemplando todas as variáveis de uma fábrica real. |
| RT07 | Integração limitada | O projeto não terá integração direta com sistemas industriais reais, como ERP, MES, sensores industriais ou sistemas corporativos externos. |
| RT08 | Compatibilidade com câmeras | O sistema será pensado para câmeras comuns ou webcams, não dependendo de hardware industrial avançado nesta sprint. |

---

## 3. Restrições de Escopo

O PrevIA não pretende, nesta primeira etapa, substituir completamente equipes de segurança do trabalho ou processos internos de fiscalização.

O sistema tem como objetivo **apoiar a segurança proativa**, fornecendo dados, alertas e registros para auxiliar supervisores e gestores.

Nesta sprint, o projeto não incluirá:

- Implantação em ambiente industrial real;
- Integração com sensores industriais físicos;
- Integração com sistemas ERP ou RH;
- Uso de hardware embarcado avançado;
- Validação com todas as normas regulatórias aplicáveis;
- Treinamento completo de modelo próprio em larga escala;
- Reconhecimento facial obrigatório dos colaboradores;
- Decisões automatizadas de punição ou advertência.

---

## 4. Restrições Legais e de Privacidade

Como o sistema utiliza imagens de colaboradores, é necessário considerar boas práticas relacionadas à privacidade e proteção de dados.

Entre os principais cuidados estão:

- Informar os colaboradores sobre o uso de câmeras;
- Utilizar as imagens apenas para finalidade de segurança;
- Evitar exposição indevida de dados pessoais;
- Controlar o acesso aos registros e relatórios;
- Armazenar apenas os dados necessários;
- Considerar princípios da LGPD no tratamento de imagens e informações dos colaboradores.

O sistema deve ser utilizado com foco em prevenção e segurança, não como ferramenta de vigilância punitiva ou exposição individual.

---

## 5. Restrições Operacionais

| Código | Restrição | Descrição |
|------|-----------|-----------|
| RO01 | Necessidade de configuração por área | Cada área industrial pode exigir EPIs diferentes, sendo necessário configurar corretamente os equipamentos obrigatórios. |
| RO02 | Dependência da posição dos colaboradores | Se o colaborador estiver parcialmente oculto ou fora do ângulo da câmera, a detecção pode ser prejudicada. |
| RO03 | Ambientes com oclusão | Máquinas, estruturas, outros colaboradores ou objetos podem bloquear a visualização dos EPIs. |
| RO04 | Falsos positivos | O sistema pode gerar alertas incorretos em algumas situações, exigindo validação ou ajuste do modelo. |
| RO05 | Falsos negativos | O sistema pode deixar de identificar algumas irregularidades, especialmente em condições inadequadas de imagem. |
| RO06 | Necessidade de supervisão humana | As decisões finais devem continuar sob responsabilidade dos profissionais de segurança e gestores. |

---

## 6. Premissas do Projeto

Para o funcionamento esperado do PrevIA, considera-se que:

- Haverá câmeras posicionadas nas áreas monitoradas;
- O ambiente terá iluminação mínima adequada;
- Os EPIs terão características visuais identificáveis;
- O sistema terá acesso a um servidor ou computador capaz de processar as imagens;
- Supervisores terão acesso ao dashboard;
- Os alertas serão utilizados para prevenção de acidentes;
- O projeto será inicialmente validado como protótipo acadêmico.

---

## 7. Limitações Atuais

Nesta etapa do projeto, algumas funcionalidades serão planejadas, mas podem não ser implementadas completamente no protótipo inicial.

Entre essas limitações estão:

- Detecção de todos os tipos possíveis de EPIs;
- Análise avançada de comportamento em ambiente real;
- Integração com múltiplas câmeras industriais;
- Geração de relatórios completos com dados reais;
- Treinamento de modelo próprio com grande volume de dados;
- Operação contínua em ambiente fabril real.
