# Atividade 2: Organização da Qualidade no LocalEats

## 1. Identificação

**Turma:** Análise e Desenvolvimento de Sistemas - 5º Semestre - 2026/2

**Equipe:** Rafaela Boldt

**Data:** 22/09/2026

### Integrantes

| Nome          | Usuário no GitHub |
| ------------- | ----------------- |
| Rafaela Boldt | @rafaelaboldt     |

**Elemento de Competência:** Identificar papéis, responsabilidades e competências relacionadas às atividades de qualidade e testes.

**Aplicação:** https://local-eats-unisenac.vercel.app/

---

## 2. Tarefa 1: Diagnóstico da situação

| Problema identificado                                                       | Possível consequência para o produto ou para a equipe                                                                                                                                          |
| --------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Os critérios para considerar uma funcionalidade pronta não estão claros.    | Uma funcionalidade pode ser considerada concluída mesmo sem atender completamente aos requisitos ou às necessidades dos usuários.                                                              |
| Testes QA                  | Problemas que poderiam ser encontrados durante o desenvolvimento podem chegar até a etapa final, aumentando o retrabalho e concentrando a responsabilidade pela qualidade em uma única pessoa. |
| Defeitos são identificados, mas nem sempre são registrados ou acompanhados. | Os defeitos podem ser esquecidos, voltar a aparecer em versões futuras ou não ter um responsável definido para sua correção.                                                                   |

### A qualidade do LocalEats deve ser responsabilidade exclusiva do profissional de QA?

Não. A qualidade deve ser construída durante todo o desenvolvimento e envolver diferentes papéis da equipe. O QA possui responsabilidades relacionadas ao planejamento e execução dos testes, mas os desenvolvedores também devem verificar o código e realizar testes, enquanto o responsável pelo produto deve ajudar a definir os critérios de aceitação. Dessa forma, a equipe compartilha a responsabilidade pela qualidade.

---

## 3. Tarefa 2: Papéis e competências

| Integrante    | Papel analisado            | Responsabilidades relacionadas à qualidade                                                                                                                                          | Competências técnicas                                                                                                          | Competências comportamentais                                                                |
| ------------- | -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------- |
| Rafaela Boldt | Responsável pelo Produto   | Definir e priorizar requisitos, esclarecer as necessidades dos usuários, definir critérios de aceitação e verificar se as funcionalidades entregues atendem ao objetivo do produto. | Conhecimento de requisitos, critérios de aceitação, priorização e entendimento das necessidades do usuário.                    | Comunicação, organização, capacidade de decisão, negociação e visão do usuário.             |
| Rafaela Boldt | Desenvolvedor              | Implementar as funcionalidades, realizar testes unitários, corrigir defeitos e participar de revisões de código.                                                                    | Conhecimento das tecnologias utilizadas, testes unitários, controle de versão, debugging e boas práticas de desenvolvimento.   | Organização, atenção aos detalhes, colaboração, pensamento lógico e abertura para feedback. |
| Rafaela Boldt | QA / Analista de Qualidade | Planejar e executar testes, verificar os critérios de aceitação, realizar testes exploratórios, registrar defeitos e acompanhar suas correções.                                     | Técnicas de teste, elaboração de casos de teste, testes funcionais e exploratórios e ferramentas de gerenciamento de defeitos. | Pensamento crítico, atenção aos detalhes, organização, comunicação e colaboração.           |
| Rafaela Boldt | DevOps                     | Apoiar a integração e disponibilização das versões, manter os ambientes e contribuir para processos de entrega controlados e automatizados.                                         | CI/CD, automação, controle de ambientes, versionamento, monitoramento e infraestrutura.                                        | Organização, responsabilidade, colaboração, comunicação e resolução de problemas.           |

### Relação dos papéis com a Atividade 1

Na Atividade 1 foi explorada a funcionalidade de login, considerando uma tentativa de acesso válida e outra com senha incorreta. A análise mostrou a importância de que o sistema tenha um comportamento compreensível para o usuário em diferentes situações. Para garantir esse tipo de qualidade, é necessário que diferentes papéis participem do processo: o responsável pelo produto ajuda a definir o comportamento esperado, o desenvolvedor implementa a funcionalidade e realiza testes durante o desenvolvimento, o QA verifica o comportamento do sistema e o DevOps contribui para uma entrega controlada das versões.

---

## 4. Tarefa 3: Matriz de responsabilidades

### Legenda

* **R — Responsável:** executa a atividade.
* **A — Aprovador:** responde pelo resultado final ou toma a decisão.
* **C — Consultado:** contribui antes da execução ou decisão.
* **I — Informado:** precisa conhecer o resultado.

| Atividade de qualidade                | Produto | Desenvolvedor | QA  | DevOps |
| ------------------------------------- | ------- | ------------- | --- | ------ |
| Definir critérios de aceitação        | A/R     | C             | C   | I      |
| Revisar requisitos                    | A       | C             | C   | I      |
| Implementar a funcionalidade          | C       | A/R           | C   | I      |
| Revisar o código                      | I       | A/R           | C   | I      |
| Criar testes unitários                | I       | A/R           | C   | I      |
| Planejar e executar testes do sistema | C       | C             | A/R | I      |
| Registrar e acompanhar defeitos       | I       | C             | A/R | I      |
| Priorizar a correção dos defeitos     | A/R     | C             | C   | I      |
| Aprovar a disponibilização da versão  | A/R     | C             | C   | C      |

### Relação da matriz com os problemas identificados

A matriz distribui as responsabilidades para evitar que a qualidade fique concentrada somente no QA. Os critérios de aceitação são definidos pelo responsável pelo produto com participação do desenvolvedor e do QA. Os testes unitários ficam sob responsabilidade do desenvolvedor, enquanto os testes do sistema ficam sob responsabilidade do QA. Dessa forma, diferentes etapas do desenvolvimento possuem pessoas responsáveis pela qualidade.

---

## Lacuna ou conflito encontrado

Uma possível lacuna está na aprovação da disponibilização da versão. O responsável pelo produto possui a responsabilidade final pela decisão, mas essa decisão deve considerar as informações fornecidas pelo QA, desenvolvedores e DevOps. Sem essa comunicação, uma versão pode ser aprovada sem que todos os problemas conhecidos tenham sido considerados.

Também é importante evitar que o QA seja considerado o único responsável por encontrar defeitos. O desenvolvedor deve identificar problemas durante a implementação e os testes unitários, enquanto o QA complementa essa verificação com testes do sistema.

---

## Práticas recomendadas

| Prática recomendada                                              | Problema que ajuda a resolver                                                                                                                          | Papéis envolvidos           |
| ---------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------- |
| Definir critérios de aceitação antes da implementação            | Evita que existam dúvidas sobre quando uma funcionalidade pode ser considerada pronta e ajuda a garantir que ela atenda às necessidades identificadas. | Produto, Desenvolvedor e QA |
| Registrar e acompanhar os defeitos em uma ferramenta de controle | Evita que problemas identificados sejam esquecidos ou deixem de ser acompanhados até sua correção.                                                     | QA, Desenvolvedor e Produto |

### Justificativa das práticas

A definição dos critérios de aceitação antes do desenvolvimento cria uma referência comum para a equipe. Isso está relacionado à Atividade 1, pois permite definir previamente o comportamento esperado de funcionalidades como o login, incluindo situações de acesso válido e inválido.

O registro e acompanhamento dos defeitos permite que os problemas encontrados tenham um histórico e um responsável pela correção. A equipe também consegue acompanhar se uma correção foi realizada e verificar novamente o comportamento da funcionalidade.

---

## 5. Uso de inteligência artificial

**Ferramenta utilizada:**

ChatGPT.

**Como foi utilizada:**

A ferramenta foi utilizada como apoio para compreender o enunciado, organizar os papéis e responsabilidades relacionados à qualidade e estruturar a matriz RACI do LocalEats.

**Como as respostas foram verificadas:**

As sugestões foram comparadas com o enunciado da atividade e com a análise realizada na Atividade 1. As responsabilidades foram revisadas para garantir que a qualidade não ficasse concentrada somente no QA. A matriz também foi conferida para verificar se cada atividade possui pelo menos um responsável (R) e um único aprovador (A).
