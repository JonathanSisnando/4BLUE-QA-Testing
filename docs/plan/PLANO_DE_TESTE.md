# PLANO DE TESTE - 4BLUE

## INFORMAÇÕES DO PROJETO DE TESTE

| PROJETO | VERSÃO | PLATAFORMA | DATA DO TESTE |
| :--- | :--- | :--- | :--- |
| 4BLUE | 1.0.0 | WEB CMS | 06/03/2026 |

**Comentários:** Este documento Plano de Teste é referente ao ciclo de teste realizado na versão e plataforma supracitadas na tabela. Tem como também seu complemento de resultado do teste o documento Relatório de Teste da mesma versão e plataforma.

| ELABORADOR | REVISORES | APROVADOR |
| :--- | :--- | :--- |
| Jonathan Gabriel | REVISOR |  APROVADOR |

---

## 1. INTRODUÇÃO
Este documento descreve o Plano de Teste do projeto de acordo com os requisitos que foram levantados, com base nas diretrizes e recursos especificados na reunião de planejamento do projeto.

## 2. OBJETIVO DOS TESTES
* Verificar e validar as funcionalidades desenvolvidas de acordo o Processo de Teste de Software, conforme os requisitos e histórias de usuário disponíveis, revelando falhas que deverão ser corrigidas até que o produto final atinja a qualidade estabelecida e desejada para o usuário final, acordada entre os times de Desenvolvimento e Teste de Software.
* Apresentar os Ambientes de Teste e da Aplicação utilizados neste ciclo de verificação e validação.

## 3. ESCOPO DOS TESTES
* Criar o planejamento de testes;
* Avaliar as especificações dos requisitos;
* Criar os cenários e/ou casos de testes para cada funcionalidade planejada;
* Executar os testes: manual e automatizados quando disponíveis em cada grupo;
* Reportar as issues encontradas durante a execução dos testes;
* Aplicar o processo de Teste de Confirmação para as issues resolvidas;
* Gerar Relatório final da execução dos testes com base nos status das issues no final de cada entrega e o parecer final da Equipe de Qualidade.

## 4. ITENS A TESTAR NA REGRESSÃO
Todos mencionados no item 5 deste Plano. Será realizado os testes funcionais manuais quando disponíveis, com o objetivo de validar situações de sucesso e exceções.
Os testes devem ser realizados nas seguintes situações:
* Alterações na arquitetura e framework do projeto que possam impactar no correto funcionamento dos casos de uso entregues.
* Alterações no caso de uso, requisitos ou histórias de usuário após a validação do mesmo (correção de issue, alteração de regra de negócio, alteração de layout).
* Primeira release para teste ou fora do escopo: é retirado do escopo de teste se for o primeiro ciclo de teste.
* Não for critério para esse tipo de teste (fora do escopo) definido junto ao Time de Desenvolvimento, para esta release e plataforma.

## 5. ITENS A TESTAR
### 5.1 FUNCIONALIDADES
Os itens abaixo são as funcionalidades disponibilizadas para o Time de Teste nesta versão.

| PLATAFORMA | FUNCIONALIDADES |
| :--- | :--- |
| WEB SITE | CRIAR CONTA |
| | LOGIN |

### 5.2 HISTÓRIA DO USUÁRIO NO JIRA
Para esta versão e plataforma disponibilizada para teste, não haverá verificação e validação de histórias de usuário do Jira.

### 5.3 ITENS DE TESTES DE CONFIRMAÇÃO
Para esta versão e plataforma disponibilizada para teste, não haverá verificação e validação de bugs corrigidos.

## 6. FERRAMENTAS
As ferramentas de testes utilizadas serão:
* MantisBT: issue tracker do projeto
* Explorer Charter (Planilha Office 360)
* GitHub – Link

## 7. AMBIENTES DE TESTE
### 7.1 AMBIENTE TESTE: APLICAÇÃO
Abaixo está a descrição detalhada do Ambiente onde encontra-se a Aplicação que será realizado o ciclo de Teste de Software:

| SERVIDOR | ENDEREÇO | HARDWARE | SOFTWARE |
| :--- | :--- | :--- | :--- |
| 999.999.99.99 | https://qa-play-sim.lovable.app/ | Hardware:10 núcleos, 12 ram 500 gb | Software: Windows 11 |

### 7.2 AMBIENTE DE TESTE: DISPOSITIVOS
Abaixo está a descrição detalhada dos dispositivos que serão utilizados para realizar o ciclo de Teste de Software.

| PLATAFORMA DE TRABALHO | HARDWARE | SOFTWARE |
| :--- | :--- | :--- |
| Web Site | Processador: Intel(R) Core(TM) i7-9700 CPU @ 3.00GHz 3.00 GHz, Ram: 16,0 GB | S.O.: Windows 11, Browser: Google Chrome |

## 8. ESTRATÉGIAS DE TESTE

| MÉTODO | NÍVEL | TIPO | EXECUÇÃO | OBJETIVO |
| :--- | :--- | :--- | :--- | :--- |
| Caixa Preta | [x] Teste de Integração | [x] Funcional <br> [ ] Regressão | [x] Exploratório <br> [x] Manual <br> [ ] Automatizado | Testar as interfaces entre os componentes, arquivos, hardware ou interfaces entre sistemas. |
| | [x] Teste de Sistema | [x] Funcional <br> [ ] Estático <br> [ ] Regressão <br> [ ] Segurança <br> [x] Usabilidade <br> [ ] Desempenho <br> [x] Carga | [x] Exploratório <br> [x] Manual <br> [ ] Automatizado | Refere-se ao comportamento de todo o sistema; Ambiente de teste deve corresponder, o máximo possível, ao ambiente de produção; Testar requisitos funcionais e não funcionais do sistema. |
| | [ ] Teste de Aceitação | [ ] Requisitos <br> [ ] Funcional <br> [ ] Não Funcional | [ ] Manual <br> [ ] Automatizado | Responsabilidade do cliente ou do usuário do sistema; Estabelecer a confiança no sistema, parte do sistema ou uma característica não específica do sistema; Avaliar a disponibilidade do sistema para entrar em produção. |
| Caixa Branca | [ ] Teste Unitário | [ ] Funcional <br> [ ] Estático | [ ] Automatizado | Reduzir o risco; verificar os comportamentos funcional e não funcional do componente ao projetado e especificado; construir a confiança na qualidade do componente; encontrar defeitos no componente; evitar que os defeitos espalhem para níveis mais altos de teste. |

## 9. CRITÉRIOS DE APROVAÇÃO, REPROVAÇÃO, SUSPENSÃO E RETOMADA DOS TESTES

### 9.1 APROVAÇÃO E REPROVAÇÃO
| CRITÉRIOS DE APROVAÇÃO E REPROVAÇÃO | DESCRIÇÃO |
| :--- | :--- |
| Percentual de cobertura dos Requisitos Funcionais e Não Funcionais | - O percentual de casos de teste e condições de testes executados e planejados na estratégia (mencionados no item 8) terão execução de 100% do planejado, conforme ambiente disponibilizado para o Time de Teste. |
| Índice de Qualidade | Índice da qualidade percebida dos resultados da execução dos casos e condições de teste, onde: <br> - Existindo somente defeitos de gravidade normal ou baixa, será feito análise pelo QA responsável, em relação aos casos de teste executados e a quantidade de defeitos, onde será analisado o impacto causado na aplicação. <br> - No uso das ferramentas de testes automatizados, cabe a análise do QA responsável diante das métricas apresentadas no relatório gerado pela ferramenta utilizada. <br> - Todos os defeitos cadastrados nesta release, independentemente de prioridade e gravidade, será realizado análise pelo QA responsável analisando se existe impacto no fluxo principal, alternativo e de exceção, conforme requisitos estabelecidos e boas práticas do Time de Teste de Software. <br> - Existindo 0% de issues de qualquer natureza que causem impacto nos seguintes itens: Fluxo Principal do Sistema estabelecido através dos Requisitos Funcionais; Fluxo Alternativo estabelecido ou não através dos Requisitos Funcionais; Fluxo Exceção estabelecido ou não através dos Requisitos Funcionais. |

### 9.2 SUSPENSÃO
| CRITÉRIOS DE SUSPENSÃO | DESCRIÇÃO |
| :--- | :--- |
| Existência de erros impeditivos | - Existência de erros que impeçam a execução dos testes de determinada funcionalidade, registradas através de defeitos de gravidade impeditiva. <br> - Existência de falhas de seguranças, hotspot security ou code smell’s com valores superiores a um dia (nove horas) de trabalho para correção. <br> - Percentual de cobertura de testes unitários inferior ao acordado com o Time de Desenvolvimento conforme descrito no critério de aprovação e reprovação. |
| Ausência de massa de teste | - Ausência de massa de testes que seja de responsabilidade do cliente fornecer ou Time de Desenvolvimento. |
| Indisponibilidade do ambiente | - Ambiente de testes indisponível em decorrência de problemas relacionados ao cliente, servidores locais, indisponibilidade de rede ou infraestrutura. |
| Mudança de Requisitos. | - Em caso de mudanças que não forem formalizadas a equipe de teste, será suspenso a execução do teste até que os novos requisitos sejam apresentados, havendo posteriormente análise do Time de Teste junto ao Time de Desenvolvimento para que haja a decisão de continuar de onde parou ou recomeçar, desde o início, o ciclo de teste. |

### 9.3 RETOMADA DOS TESTES
| CRITÉRIOS DE RETOMADA DOS TESTES | DESCRIÇÃO |
| :--- | :--- |
| Correção de erros impeditivos | - Correção de erros que impediam a execução dos testes de determinada funcionalidade, registradas através de defeitos de gravidade impeditiva. <br> - Correção de falhas de segurança, hotspot security ou code smell’s com valores superiores a um dia de trabalho para correção. <br> - Estar dentro do percentual mínimo da cobertura de testes unitários acordados entre o QA responsável e o Time de Desenvolvimento conforme descrito no critério de aprovação e reprovação. |
| Existência de massa de teste | - Disponibilização de massa de testes que seja de responsabilidade do cliente fornecer ou Time de Desenvolvimento. |
| Disponibilidade do ambiente | - Disponibilização do ambiente de testes. |
