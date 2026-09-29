# Atividade 3: Estratégia e Projeto de Testes do LocalEats

## 1. Identificação

**Turma:** Análise e Desenvolvimento de Sistemas - 5º Semestre - 2026/2

**Equipe:** Rafaela Boldt

**Data:** 22/09/2026

### Integrantes

| Nome          | Usuário no GitHub |
| ------------- | ----------------- |
| Rafaela Boldt | @rafaelaboldt     |

**Unidade Curricular:** Qualidade de Software

**Metodologia:** Problem-Based Learning (PBL)

**Elemento de Competência:** EC4: Planejar e projetar testes selecionando técnicas adequadas.

**Projeto:** LocalEats

**Aplicação:** https://local-eats-unisenac.vercel.app/

---

# 2. Tarefa 1: Planejamento dos testes

## 2.1 Objetivo dos testes

O objetivo dos testes é verificar se a funcionalidade de login do LocalEats permite o acesso de usuários com credenciais válidas e impede o acesso quando as credenciais informadas são inválidas. Também será verificado se o sistema apresenta um comportamento compreensível para o usuário nas diferentes situações de acesso.

---

## 2.2 Escopo

Como o trabalho é individual, a funcionalidade analisada nesta atividade é o **login**.

### Funcionalidade incluída

| Integrante    | Funcionalidade incluída | O que será verificado                                                                                     |
| ------------- | ----------------------- | --------------------------------------------------------------------------------------------------------- |
| Rafaela Boldt | Login                   | Comportamento do sistema ao utilizar credenciais válidas e diferentes situações de credenciais inválidas. |

### Funcionalidade não incluída

| Funcionalidade não incluída | Justificativa                                                                                                                                  |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| Fazer pedido                | Não faz parte da funcionalidade escolhida para análise nesta atividade e possui regras próprias que não serão abordadas no planejamento atual. |

---

## 2.3 Abordagem

| Item            | Decisão da equipe               | Justificativa                                                                                                                                                      |
| --------------- | ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Níveis de teste | Sistema                         | O login será analisado pelo comportamento da aplicação, considerando a interação do usuário com a interface e o resultado apresentado pelo sistema.                |
| Tipos de teste  | Funcional                       | O objetivo é verificar se o login funciona de acordo com o comportamento esperado para diferentes entradas.                                                        |
| Perspectiva     | Caixa-preta                     | Os testes serão planejados considerando as entradas fornecidas pelo usuário e os resultados observáveis, sem analisar o código interno da aplicação.               |
| Técnica         | Particionamento de equivalência | As possíveis entradas do login podem ser divididas em classes válidas e inválidas, permitindo selecionar casos representativos sem testar todas as possibilidades. |

---

## 2.4 Ambiente e responsabilidades

| Item                                     | Definição                                                                                                                                      |
| ---------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| Ambiente necessário                      | Aplicação LocalEats disponível em ambiente web, navegador atualizado, conexão com a internet e uma conta de usuário cadastrada para os testes. |
| Responsável pelo planejamento            | Rafaela Boldt                                                                                                                                  |
| Responsável pela especificação dos casos | Rafaela Boldt                                                                                                                                  |
| Responsável pela futura execução         | Rafaela Boldt                                                                                                                                  |

---

## 2.5 Critérios

| Critério  | Definição da equipe                                                                                                                                      |
| --------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Entrada   | Aplicação disponível, acesso à tela de login e dados necessários para realizar as tentativas de acesso.                                                  |
| Saída     | Os três casos de teste planejados foram executados posteriormente e seus resultados registrados, permitindo verificar o comportamento esperado do login. |
| Suspensão | A aplicação estiver indisponível, a tela de login não puder ser acessada ou não houver dados suficientes para realizar os casos planejados.              |

---

# 3. Tarefa 2: Riscos e técnicas de teste

## 3.1 Análise dos riscos

A funcionalidade escolhida foi o **login**. Foram identificados dois riscos principais relacionados ao acesso do usuário.

| ID  | Integrante    | Funcionalidade | Risco                                                                               | Consequência                                                                                                                | Probabilidade | Impacto | Prioridade | Justificativa                                                                                                        |
| --- | ------------- | -------------- | ----------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- | ------------- | ------- | ---------- | -------------------------------------------------------------------------------------------------------------------- |
| R01 | Rafaela Boldt | Login          | O sistema permitir o acesso mesmo quando as credenciais informadas forem inválidas. | Uma pessoa poderia acessar uma conta sem possuir as credenciais corretas, comprometendo a segurança e os dados do usuário.  | Média         | Alto    | Alta       | O problema pode afetar diretamente a segurança das contas e permitir acesso indevido ao sistema.                     |
| R02 | Rafaela Boldt | Login          | O sistema não permitir o acesso de um usuário que informou credenciais válidas.     | O usuário não conseguirá acessar sua conta e poderá ficar impedido de utilizar as funcionalidades disponíveis após o login. | Média         | Alto    | Alta       | O login é uma etapa de entrada no sistema. Um erro nesse processo impede o usuário de continuar o fluxo normalmente. |

---

## 3.2 Aplicação da técnica

### Integrante responsável

**Nome:** Rafaela Boldt

**Funcionalidade:** Login

**Riscos relacionados:** R01 e R02

**Técnica escolhida:** Particionamento de equivalência

### Por que a técnica foi escolhida?

O particionamento de equivalência foi escolhido porque as entradas utilizadas no login podem ser agrupadas em classes que apresentam comportamentos esperados semelhantes.

Neste caso, não é necessário testar todas as combinações possíveis de e-mail e senha. É possível selecionar valores representativos de classes válidas e inválidas e verificar se o sistema apresenta o comportamento esperado para cada uma delas.

### Aplicação da técnica

Foram consideradas as seguintes classes de equivalência:

| Classe | Situação               | Exemplo de entrada                             |
| ------ | ---------------------- | ---------------------------------------------- |
| CE01   | Credenciais válidas    | E-mail de usuário cadastrado + senha correta   |
| CE02   | Senha inválida         | E-mail de usuário cadastrado + senha incorreta |
| CE03   | Usuário não cadastrado | E-mail não cadastrado + senha informada        |

As classes CE01, CE02 e CE03 representam situações diferentes que podem ocorrer durante uma tentativa de login.

### Casos derivados

* **CT01:** Acessar o sistema com credenciais válidas.
* **CT02:** Tentar acessar o sistema com senha inválida.
* **CT03:** Tentar acessar o sistema com usuário não cadastrado.

---

# 4. Tarefa 3: Casos de teste e rastreabilidade

## 4.1 Especificação dos casos de teste

### CT01: Realizar login com credenciais válidas

**Integrante responsável:** Rafaela Boldt

**Funcionalidade:** Login

**Risco relacionado:** R02 — O sistema não permitir o acesso de um usuário que informou credenciais válidas.

**Técnica utilizada:** Particionamento de equivalência — CE01

**Pré-condição:**

O usuário possui uma conta cadastrada no LocalEats e conhece as credenciais corretas para realizar o acesso.

**Dados de entrada:**

* E-mail de uma conta cadastrada.
* Senha correta correspondente à conta.

**Passos:**

1. Acessar a tela de login do LocalEats.
2. Informar o e-mail de uma conta cadastrada.
3. Informar a senha correta da conta.
4. Acionar a opção de entrar.

**Resultado esperado:**

O sistema deve aceitar as credenciais e permitir o acesso do usuário à área correspondente após o login.

---

### CT02: Impedir login com senha inválida

**Integrante responsável:** Rafaela Boldt

**Funcionalidade:** Login

**Risco relacionado:** R01 — O sistema permitir o acesso mesmo quando as credenciais informadas forem inválidas.

**Técnica utilizada:** Particionamento de equivalência — CE02

**Pré-condição:**

Existe uma conta cadastrada no LocalEats e o e-mail utilizado no teste pertence a essa conta.

**Dados de entrada:**

* E-mail de uma conta cadastrada.
* Senha diferente da senha correta da conta.

**Passos:**

1. Acessar a tela de login do LocalEats.
2. Informar o e-mail de uma conta cadastrada.
3. Informar uma senha incorreta.
4. Acionar a opção de entrar.

**Resultado esperado:**

O sistema deve impedir o acesso e informar ao usuário que as credenciais utilizadas não são válidas, sem permitir a entrada na conta.

---

### CT03: Impedir login com usuário não cadastrado

**Integrante responsável:** Rafaela Boldt

**Funcionalidade:** Login

**Risco relacionado:** R01 — O sistema permitir o acesso mesmo quando as credenciais informadas forem inválidas.

**Técnica utilizada:** Particionamento de equivalência — CE03

**Pré-condição:**

O e-mail utilizado no teste não está associado a uma conta cadastrada no LocalEats.

**Dados de entrada:**

* E-mail que não possui cadastro no sistema.
* Uma senha qualquer.

**Passos:**

1. Acessar a tela de login do LocalEats.
2. Informar um e-mail que não esteja cadastrado.
3. Informar uma senha.
4. Acionar a opção de entrar.

**Resultado esperado:**

O sistema deve impedir o acesso e informar ao usuário que as credenciais não são válidas, sem permitir a entrada no sistema.

---

## 4.2 Matriz de rastreabilidade

| Integrante    | Funcionalidade | Risco ou requisito                                         | Técnica utilizada               | Casos de teste |
| ------------- | -------------- | ---------------------------------------------------------- | ------------------------------- | -------------- |
| Rafaela Boldt | Login          | R01: O sistema permitir acesso com credenciais inválidas   | Particionamento de equivalência | CT02 e CT03    |
| Rafaela Boldt | Login          | R02: O sistema não permitir acesso com credenciais válidas | Particionamento de equivalência | CT01           |

A matriz demonstra a relação entre a funcionalidade analisada, os riscos identificados, a técnica utilizada e os casos de teste planejados.

Dessa forma, os dois riscos identificados possuem pelo menos um caso de teste relacionado.

---

# 5. Relação entre funcionalidade, risco, técnica e casos

A partir do planejamento realizado, a relação definida para a funcionalidade de login foi:

**Login → Riscos R01 e R02 → Particionamento de equivalência → CT01, CT02 e CT03**

O risco R01 está relacionado às situações em que o sistema poderia permitir o acesso com credenciais inválidas. Por isso, foram criados os casos CT02 e CT03, utilizando duas classes inválidas diferentes.

O risco R02 está relacionado à possibilidade de um usuário com credenciais válidas não conseguir acessar sua conta. Por isso, foi criado o CT01 para representar a classe de credenciais válidas.

Os casos foram planejados para representar situações diferentes do login, sem a necessidade de testar todas as possíveis combinações de e-mail e senha.

---

# 6. Uso de inteligência artificial

**Ferramenta utilizada:**

ChatGPT.

**Como foi utilizada:**

A ferramenta foi utilizada como apoio para compreender o enunciado, identificar possíveis riscos relacionados à funcionalidade de login, comparar técnicas de teste e organizar os casos de teste e a matriz de rastreabilidade.

**Uma sugestão que precisou ser alterada ou rejeitada:**

Durante a elaboração, as sugestões foram analisadas para evitar a criação de casos de teste que não estivessem relacionados aos riscos identificados. Também foi mantida somente a funcionalidade de login, de acordo com a proposta individual da atividade.

**Como as respostas foram verificadas:**

As sugestões foram comparadas com o enunciado da atividade e com a funcionalidade de login analisada nas atividades anteriores. Os riscos, a técnica escolhida e os casos de teste foram revisados para verificar se estavam relacionados entre si e se os resultados esperados eram observáveis. A matriz de rastreabilidade também foi conferida para garantir que os riscos identificados possuíssem casos de teste correspondentes.
