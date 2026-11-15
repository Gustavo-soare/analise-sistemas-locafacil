<sub>[🏠 Início](../README.md) › Documentação › Critérios de avaliação</sub>

# Critérios de Avaliação

## 1. Diagramas solicitados

| Nº | Diagrama | Exigências |
|---|---|---|
| 1 | Casos de uso | Identificar os atores e os relacionamentos «include» e «extend». |
| 2 | Classes | Nível de especificação, com atributos tipados, assinaturas completas das operações, multiplicidades e relacionamentos adequados. |
| 3 | Sequência | Caso de uso Registrar Devolução, cobrindo o laço sobre os itens, a alternativa de avaria e a condição de atraso. |
| 4 | Atividades | Processo completo, da reserva à devolução, com raias para Cliente, Atendente e Sistema. |
| 5 | Máquina de estados | Ciclo de vida de um equipamento. |

## 2. Orientações da atividade

- Modelar apenas o que o enunciado sustenta.
- Não inventar atributos nem operações sem verbo correspondente no texto.
- Não utilizar getters e setters como operações.
- Utilizar composição somente quando a parte não existe fora do todo.

## 3. Verificações realizadas

| Verificação | Situação |
|---|---|
| Associações entre atores e casos de uso representadas sem seta. | Atendido |
| «include» do caso base para o incluído e «extend» do estendente para o base, com condição e ponto de extensão. | Atendido |
| Atributos privados e tipados e operações públicas com assinatura completa. | Atendido |
| Multiplicidade informada nas duas extremidades das associações. | Atendido |
| Composição apenas em Reserva/ItemReserva e Locacao/ItemLocacao. | Atendido |
| Mensagens do diagrama de sequência correspondentes às operações do diagrama de classes. | Atendido |
| Fragmentos loop, alt e opt no diagrama de sequência. | Atendido |
| Raias para Cliente, Atendente e Sistema no diagrama de atividades. | Atendido |
| Transições no formato evento [guarda] / ação na máquina de estados. | Atendido |

## 4. Informações da atividade

- **Valor:** 1,0 ponto.
- **Carga horária:** 3 horas.

---

<div align="center">

[⬅️ Requisitos](requisitos.md) · [🏠 Voltar ao início](../README.md)

</div>
