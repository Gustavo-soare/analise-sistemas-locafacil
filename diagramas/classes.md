<sub>[🏠 Início](../README.md) › Diagramas › Classes</sub>

# 2. Diagrama de Classes (Nível de Especificação)

## 1. Descrição

Este diagrama apresenta a estrutura do sistema em nível de especificação, com as classes, seus atributos tipados, operações públicas, multiplicidades, enumerações e restrições.

## 2. Diagrama

<p align="center">

![Diagrama de classes](../imagens/Diagrama%20de%20Classes.drawio.png)

</p>

## 3. Classes

| Classe | Atributos | Operações |
|---|---|---|
| **Categoria** | nome | — |
| **Equipamento** | codigo, descricao, valorDiaria, situacao | consultarDisponibilidade, reservar, locar, liberar, enviarParaVistoria, enviarParaManutencao, concluirReparo, darBaixa |
| **Cliente** | cpf, nome, telefone | — |
| **Atendente** | matricula, nome | — |
| **Reserva** | numero, dataSolicitacao, dataInicioPrevista, dataFimPrevista, situacao | calcularValorPrevisto, cancelar, expirar |
| **ItemReserva** | valorDiariaPrevisto | calcularSubtotal |
| **Locacao** | numero, dataRetirada, dataDevolucaoPrevista, dataDevolucao, situacao | emitirContrato, calcularValor, registrarDevolucao, cobrarAvaria, aplicarMultaAtraso, calcularDiasExcedentes, encerrar, emitirComprovanteDevolucao |
| **ItemLocacao** | valorDiariaPraticado | calcularSubtotal, registrarVistoria |
| **Vistoria** | houveAvaria, valorEstimadoReparo | — |
| **Cobranca** | tipo, valor, situacao | registrarPagamento |
| «interface» **SistemaPagamento** | — | processarPagamento |

## 4. Enumerações

| Enumeração | Valores |
|---|---|
| SituacaoEquipamento | DISPONIVEL, RESERVADO, LOCADO, EM_VISTORIA, EM_MANUTENCAO, BAIXADO |
| SituacaoReserva | ATIVA, CANCELADA, EXPIRADA |
| SituacaoLocacao | EM_ANDAMENTO, ENCERRADA |
| TipoCobranca | LOCACAO, AVARIA, MULTA_ATRASO |
| SituacaoCobranca | EM_ABERTO, PAGA |

## 5. Relacionamentos

| Tipo | Ligação | Multiplicidade |
|---|---|---|
| Composição | Reserva — ItemReserva | 1 — 1..* |
| Composição | Locacao — ItemLocacao | 1 — 1..* |
| Associação | Categoria — Equipamento | 1 — 0..* |
| Associação | Cliente — Reserva | 1 — 0..* |
| Associação | Cliente — Locacao | 1 — 0..* |
| Associação | Atendente — Locacao | 1 — 0..* |
| Associação | Atendente — Vistoria | 1 — 0..* |
| Associação | Reserva — Locacao | 0..1 — 0..1 |
| Associação | ItemReserva → Equipamento | 0..* — 1 |
| Associação | ItemLocacao → Equipamento | 0..* — 1 |
| Associação | ItemLocacao — Vistoria | 1 — 0..1 |
| Associação | Locacao — Cobranca | 1 — 1..* |
| Dependência «use» | Cobranca → SistemaPagamento | — |

## 6. Restrições

- `{toda Locacao tem exatamente uma Cobranca do tipo LOCACAO}`
- `{valorEstimadoReparo só é informado quando houveAvaria = true}`

---

<div align="center">

[⬅️ Casos de uso](casos-de-uso.md) · [🏠 Voltar ao início](../README.md) · [Sequência ➡️](sequencia-registrar-devolucao.md)

</div>
