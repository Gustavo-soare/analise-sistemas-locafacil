<sub>[🏠 Início](../README.md) › Diagramas › Máquina de estados</sub>

# 5. Diagrama de Máquina de Estados: Equipamento

## 1. Descrição

Este diagrama apresenta o ciclo de vida de um equipamento, com seus estados e as transições entre eles.

## 2. Diagrama

<p align="center">

![Diagrama de máquina de estados](../imagens/Diagrama%20de%20maquina%20de%20estado.drawio.png)

</p>

## 3. Estados

| Estado | Significado |
|---|---|
| **Disponível** | Pode ser reservado ou locado |
| **Reservado** | Está preso a uma reserva ativa |
| **Locado** | Está com o cliente |
| **Em vistoria** | Foi devolvido e está sendo avaliado |
| **Em manutenção** | Teve avaria e está em reparo |
| **Baixado** | Reparo inviável; saiu do estoque (estado final) |

## 4. Transições

| De | Para | Evento [guarda] / ação |
|---|---|---|
| Estado inicial | Disponível | cadastrar equipamento |
| Disponível | Reservado | registrar reserva |
| Reservado | Disponível | cancelar reserva |
| Reservado | Disponível | expirar reserva |
| Reservado | Locado | registrar retirada [pagamento registrado] |
| Disponível | Locado | registrar retirada sem reserva [pagamento registrado] |
| Locado | Em vistoria | registrar devolução |
| Em vistoria | Disponível | registrar laudo [sem avaria] |
| Em vistoria | Em manutenção | registrar laudo [com avaria] / cobrar avaria |
| Em manutenção | Disponível | concluir reparo |
| Em manutenção | Baixado | dar baixa [reparo inviável] |
| Baixado | Estado final | — |

---

<div align="center">

[⬅️ Atividades](atividades.md) · [🏠 Voltar ao início](../README.md)

</div>
