# Atividade 1: Fundamentos e Características da Qualidade no LocalEats

## 1. Identificação

**Turma:** Análise e Desenvolvimento de Sistemas - 5º Semestre - 2026/2

**Equipe:** Rafaela Boldt

**Data:** 22/09/2026

### Integrantes

| Nome          | Usuário no GitHub |
| ------------- | ----------------- |
| Rafaela Boldt | @rafaelaboldt     |

**Elemento de Competência:** Compreender os fundamentos de qualidade de software e sua aplicação no desenvolvimento de sistemas.

**Aplicação:** https://local-eats-unisenac.vercel.app/

---

## 2. Tarefa 1: Fundamentos da qualidade

### 2.1 Necessidades explícitas e implícitas

| Tipo      | Necessidade                                                                                                   | Interessado | Consequência se não for atendida                                                                     |
| --------- | ------------------------------------------------------------------------------------------------------------- | ----------- | ---------------------------------------------------------------------------------------------------- |
| Explícita | O usuário deve conseguir criar uma conta no LocalEats.                                                        | Usuário     | O usuário não conseguirá utilizar o sistema com uma conta própria.                                   |
| Explícita | O usuário deve conseguir pesquisar restaurantes por especialidade ou localização.                             | Usuário     | O usuário terá dificuldade para encontrar restaurantes de acordo com o que procura.                  |
| Implícita | Os pedidos realizados pelo usuário devem ser registrados corretamente e permanecer disponíveis para consulta. | Usuário     | O usuário pode perder informações sobre seus pedidos ou não conseguir acompanhar o que realizou.     |
| Implícita | As funcionalidades do sistema devem ser compreensíveis e fáceis de utilizar.                                  | Usuário     | O usuário pode ter dificuldade para realizar tarefas, mesmo que elas estejam disponíveis no sistema. |

### 2.2 Questão sobre os fundamentos da qualidade

**Um sistema que implementa todas as funcionalidades explicitamente solicitadas pode, ainda assim, apresentar baixa qualidade? Justifiquem utilizando pelo menos uma necessidade implícita identificada pela equipe.**

Sim. Um sistema pode possuir todas as funcionalidades solicitadas e ainda apresentar problemas de qualidade. Por exemplo, o LocalEats pode permitir que o usuário faça um pedido, mas se o pedido não for registrado corretamente ou se for difícil de consultar depois, a necessidade do usuário não será atendida. Por isso, a qualidade também depende do atendimento às necessidades implícitas.

---

## 3. Tarefa 2: Exploração da aplicação

A funcionalidade escolhida para exploração foi o **login**.

Foi realizada uma utilização esperada, utilizando credenciais válidas, e uma utilização alternativa, utilizando uma senha incorreta.

| Integrante    | Funcionalidade | O que foi realizado                                                                                          | O que foi observado                                                                                                                                                          | Evidência                                                                                                                             |
| ------------- | -------------- | ------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| Rafaela Boldt | Login          | Foi realizado um acesso com credenciais válidas e, em seguida, uma tentativa utilizando uma senha incorreta. | No primeiro caso, o sistema apresentou o resultado correspondente ao acesso. No segundo caso, foi observado o comportamento apresentado pelo sistema para a senha incorreta. | [Credenciais válidas](evidencias/login-credenciais-validas.png) e [Credenciais inválidas](evidencias/login-credenciais-invalidas.png) |

---

## 4. Tarefa 3: Requisitos e características de qualidade

| Integrante    | Requisito de Qualidade                                                                                       | Característica ou subcaracterística                     | Justificativa                                                                                                                                                                                                                                           | Como avaliar                                                                                                                                               |
| ------------- | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Rafaela Boldt | O sistema deve informar de forma clara ao usuário quando as credenciais utilizadas no login forem inválidas. | Usabilidade - capacidade de reconhecimento da adequação | Durante o login, o usuário precisa entender quando não conseguiu acessar o sistema devido às credenciais informadas. Uma mensagem clara ajuda a identificar o problema e evita que o usuário fique sem saber o motivo do acesso não ter sido realizado. | Realizar tentativas de login com credenciais válidas e inválidas e verificar se o sistema apresenta uma mensagem clara e compreensível para cada situação. |

---

## 5. Uso de inteligência artificial

**Ferramenta utilizada:**

ChatGPT.

**Como foi utilizada:**

A ferramenta foi utilizada como apoio para compreender o enunciado, discutir possíveis necessidades de qualidade e organizar as respostas das tarefas.

**Como as respostas foram verificadas:**

As sugestões foram comparadas com o enunciado da atividade e com o comportamento observado durante a exploração do LocalEats. As respostas foram revisadas antes de serem incluídas no documento.
