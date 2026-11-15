<div align="center">

# 🏗️ Modelagem UML — Sistema LocaFácil

**Especificação de um sistema de locação de equipamentos para obras, da reserva à devolução**

![UML](https://img.shields.io/badge/UML-2.5-1f6feb?style=for-the-badge)
![draw.io](https://img.shields.io/badge/draw.io-Diagramas-f08705?style=for-the-badge&logo=diagramsdotnet&logoColor=white)
![Markdown](https://img.shields.io/badge/Markdown-Documentação-000000?style=for-the-badge&logo=markdown&logoColor=white)

| 👤 Aluno | 📚 Disciplina | 👨‍🏫 Professor |
|:---:|:---:|:---:|
| Seu Nome | Análise de Sistemas | Lacordaire Kemel |

</div>

---

## 📑 Sumário

1. [Apresentação](#1-apresentação)
2. [Sistema modelado](#2-sistema-modelado)
3. [Objetivo](#3-objetivo)
4. [Escopo do projeto](#4-escopo-do-projeto)
5. [Documentação do projeto](#5-documentação-do-projeto)
6. [Ferramentas utilizadas](#6-ferramentas-utilizadas)
7. [Diagramas elaborados](#7-diagramas-elaborados)
8. [Galeria dos diagramas](#8-galeria-dos-diagramas)
9. [Estrutura do repositório](#9-estrutura-do-repositório)
10. [Considerações finais](#10-considerações-finais)

---

## 1. Apresentação

Este projeto aplica os conceitos de **Análise de Sistemas** e da linguagem **UML** na especificação de um sistema de locação de equipamentos para obras de pequeno porte.

O processo da empresa foi modelado da reserva até a devolução: cadastro de clientes e equipamentos, controle de disponibilidade, emissão do contrato de locação, registro de pagamentos, vistoria dos equipamentos devolvidos e cobrança de avarias e multas por atraso.

## 2. Sistema modelado

A **LocaFácil** aluga equipamentos como **betoneiras, andaimes, compactadores, martelos rompedores e geradores**.

> ⚠️ **Situação atual:** o controle é feito em planilhas e num caderno de retiradas, o que causa **reservas duplicadas**, **equipamentos entregues sem conferência** e **cobranças de atraso esquecidas**.

## 3. Objetivo

Especificar, por meio de diagramas UML, um sistema que informatize o processo de locação da LocaFácil, da reserva à devolução. Os diagramas representam os atores, a estrutura do sistema, as interações entre os objetos, o fluxo do processo e o ciclo de vida dos equipamentos.

## 4. Escopo do projeto

| Etapa | Funcionalidades modeladas |
|---|---|
| 📇 **Cadastro** | Cadastro de clientes e equipamentos |
| 📅 **Reserva** | Consulta de disponibilidade, registro, cálculo do valor previsto, cancelamento e expiração |
| 📦 **Retirada** | Conferência de documentos, registro da retirada, emissão do contrato e registro do pagamento por sistema externo |
| 🔁 **Devolução** | Vistoria dos itens, cobrança de avaria, multa por atraso, encerramento da locação e emissão do comprovante |
| 🔧 **Manutenção** | Conclusão do reparo e baixa do equipamento |

## 5. Documentação do projeto

| Documento | Descrição |
|---|---|
| 📄 [Escopo do projeto](documentacao/escopo.md) | A empresa, o problema, o objetivo e os atores do sistema |
| 📄 [Requisitos](documentacao/requisitos.md) | Cadastros, requisitos funcionais e regras de negócio |
| 📄 [Critérios de avaliação](documentacao/criterios-avaliacao.md) | Diagramas solicitados, exigências e orientações da atividade |

## 6. Ferramentas utilizadas

| Ferramenta | Uso |
|---|---|
| **UML 2.5** | Linguagem de modelagem |
| **draw.io** | Elaboração dos diagramas |
| **Markdown** | Documentação |
| **GitHub** | Hospedagem e versionamento |

## 7. Diagramas elaborados

Foram elaborados **cinco diagramas**, que cobrem as visões funcional, estrutural, de interação e comportamental do sistema.

| Nº | Diagrama | O que representa |
|:---:|---|---|
| 1 | [Casos de uso](diagramas/casos-de-uso.md) | Atores Cliente, Atendente e Sistema de Pagamento, com «include» e «extend» |
| 2 | [Classes](diagramas/classes.md) | Classes em nível de especificação, com atributos tipados, operações, multiplicidades e composições |
| 3 | [Sequência — Registrar Devolução](diagramas/sequencia-registrar-devolucao.md) | Interação com boundary, control e entity, com loop, alt e opt |
| 4 | [Atividades](diagramas/atividades.md) | Processo da reserva à devolução, com raias para Cliente, Atendente e Sistema |
| 5 | [Máquina de estados](diagramas/maquina-de-estados.md) | Ciclo de vida do equipamento |

## 8. Galeria dos diagramas

<details open>
<summary><b>1. Diagrama de casos de uso</b></summary>
<br>
<p align="center"><img src="imagens/Diagrama%20Caso%20de%20uso.drawio.png" alt="Diagrama de casos de uso" width="90%"></p>
</details>

<details>
<summary><b>2. Diagrama de classes</b></summary>
<br>
<p align="center"><img src="imagens/Diagrama%20de%20Classes.drawio.png" alt="Diagrama de classes" width="90%"></p>
</details>

<details>
<summary><b>3. Diagrama de sequência — Registrar Devolução</b></summary>
<br>
<p align="center"><img src="imagens/Diagrama%20de%20Sequencia.drawio.png" alt="Diagrama de sequência" width="90%"></p>
</details>

<details>
<summary><b>4. Diagrama de atividades</b></summary>
<br>
<p align="center"><img src="imagens/Diagrama%20de%20atividades.drawio.png" alt="Diagrama de atividades" width="70%"></p>
</details>

<details>
<summary><b>5. Diagrama de máquina de estados</b></summary>
<br>
<p align="center"><img src="imagens/Diagrama%20de%20maquina%20de%20estado.drawio.png" alt="Diagrama de máquina de estados" width="80%"></p>
</details>

> 💡 Clique no nome de cada diagrama para abrir ou fechar a imagem.

## 9. Estrutura do repositório

```text
analise-sistemas-locafacil/
│
├── README.md
│
├── documentacao/
│   ├── escopo.md
│   ├── requisitos.md
│   └── criterios-avaliacao.md
│
├── diagramas/
│   ├── casos-de-uso.md
│   ├── classes.md
│   ├── sequencia-registrar-devolucao.md
│   ├── atividades.md
│   └── maquina-de-estados.md
│
└── imagens/
    ├── Diagrama Caso de uso.drawio.png
    ├── Diagrama de Classes.drawio.png
    ├── Diagrama de Sequencia.drawio.png
    ├── Diagrama de atividades.drawio.png
    └── Diagrama de maquina de estado.drawio.png
```

## 10. Considerações finais

Este projeto permitiu aplicar os principais diagramas da UML na especificação de um sistema real, partindo da análise do enunciado para identificar atores, classes, interações, fluxos e estados.

A modelagem da LocaFácil mantém a coerência entre os diagramas:

- os **casos de uso** orientam o **diagrama de sequência**;
- as mensagens da **sequência** correspondem às operações do **diagrama de classes**;
- os estados do **equipamento** acompanham o fluxo do **diagrama de atividades**.

O projeto mostra a importância da modelagem para compreender, documentar e comunicar os requisitos de um sistema antes da sua implementação.

---

<div align="center">
<sub>Instituto Federal Goiano · Análise de Sistemas · 2026</sub>
</div>
