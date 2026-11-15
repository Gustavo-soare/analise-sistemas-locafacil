# Modelagem UML — Sistema LocaFácil

**Aluno:** Seu Nome  
**Disciplina:** Análise de Sistemas  
**Professor:** Lacordaire Kemel

## 1. Apresentação

Este projeto aplica os conceitos de Análise de Sistemas e da linguagem UML na especificação de um sistema de locação de equipamentos para obras de pequeno porte.

A proposta consiste em modelar o processo da empresa desde a reserva até a devolução, considerando o cadastro de clientes e equipamentos, o controle de disponibilidade, a emissão do contrato de locação, o registro de pagamentos, a vistoria dos equipamentos devolvidos e a cobrança de avarias e multas por atraso.

## 2. Sistema modelado

A **LocaFácil** é uma empresa que aluga equipamentos como betoneiras, andaimes, compactadores, martelos rompedores e geradores.

Atualmente, o controle é feito em planilhas e em um caderno de retiradas, o que provoca reservas duplicadas, entrega de equipamentos sem conferência e esquecimento de cobranças de atraso.

## 3. Objetivo

Especificar, por meio de diagramas UML, um sistema que informatize o processo de locação da LocaFácil, da reserva à devolução, representando seus atores, sua estrutura, as interações entre os objetos, o fluxo do processo e o ciclo de vida dos equipamentos.

## 4. Escopo do projeto

O projeto contempla a modelagem das seguintes funcionalidades:

- Cadastro de clientes e equipamentos;
- Consulta de disponibilidade dos equipamentos;
- Registro, cancelamento e expiração de reservas;
- Cálculo do valor previsto da reserva;
- Conferência de documentos e registro da retirada;
- Emissão do contrato de locação;
- Registro do pagamento por sistema externo;
- Registro da devolução e da vistoria dos itens;
- Cobrança de avarias e aplicação de multa por atraso;
- Encerramento da locação e emissão do comprovante;
- Controle da manutenção e da baixa de equipamentos.

## 5. Documentação do projeto

A documentação foi organizada em arquivos específicos, com o objetivo de facilitar a compreensão do caso e o acompanhamento da modelagem.

| Documento | Descrição |
|---|---|
| Escopo do projeto | Define a empresa, o problema, o objetivo e os atores do sistema. |
| Requisitos | Apresenta os cadastros, os requisitos funcionais e as regras de negócio. |
| Critérios de avaliação | Relaciona os diagramas solicitados, as exigências e as orientações da atividade. |
| Diagrama de casos de uso | Apresenta os atores, os casos de uso e os relacionamentos «include» e «extend». |
| Diagrama de classes | Apresenta as classes em nível de especificação, com atributos, operações e relacionamentos. |
| Diagrama de sequência | Apresenta as interações do caso de uso Registrar Devolução. |
| Diagrama de atividades | Apresenta o fluxo do processo da reserva à devolução, com raias. |
| Diagrama de máquina de estados | Apresenta o ciclo de vida de um equipamento. |

## 6. Ferramentas utilizadas

- **Linguagem de modelagem:** UML 2.5.
- **Ferramenta de diagramação:** draw.io.
- **Documentação:** Markdown.
- **Hospedagem:** GitHub.

## 7. Diagramas elaborados

Foram elaborados cinco diagramas, abrangendo as visões funcional, estrutural, de interação e comportamental do sistema.

- **Casos de uso:** identifica os atores Cliente, Atendente e Sistema de Pagamento, com «include» para os passos obrigatórios e «extend» para avaria e atraso.
- **Classes:** representa as classes em nível de especificação, com atributos tipados, operações públicas, multiplicidades, composições, enumerações e restrições.
- **Sequência:** detalha o caso de uso Registrar Devolução com os estereótipos boundary, control e entity, cobrindo o laço sobre os itens, a alternativa de avaria e a condição de atraso.
- **Atividades:** representa o processo completo, da reserva à devolução, com raias para Cliente, Atendente e Sistema.
- **Máquina de estados:** representa os estados do equipamento: disponível, reservado, locado, em vistoria, em manutenção e baixado.

A descrição detalhada de cada diagrama está na pasta `diagramas`.

## 8. Imagens

As imagens dos diagramas estão organizadas na pasta `imagens`. Elas permitem visualizar os elementos modelados, os relacionamentos e os fluxos representados em cada diagrama.

## 9. Estrutura do repositório

A organização dos arquivos do projeto está distribuída da seguinte maneira:

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

A realização deste projeto possibilitou aplicar os principais diagramas da UML na especificação de um sistema real, partindo da análise do enunciado para a identificação de atores, classes, interações, fluxos e estados.

A modelagem da LocaFácil permitiu representar de forma integrada o processo de locação, garantindo coerência entre os diagramas: os casos de uso orientam o diagrama de sequência, as mensagens da sequência correspondem às operações do diagrama de classes, e os estados do equipamento acompanham o fluxo descrito no diagrama de atividades.

Dessa forma, o projeto demonstra a importância da modelagem para compreender, documentar e comunicar os requisitos de um sistema antes de sua implementação.
