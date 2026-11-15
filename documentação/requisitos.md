<sub>[🏠 Início](../README.md) › Documentação › Requisitos</sub>

# Requisitos

## 1. Cadastros

| Cadastro | Dados | Observação |
|---|---|---|
| Equipamento | Código, descrição, valor da diária, categoria e situação. | Cada equipamento é uma unidade física individual. |
| Categoria | Nome. | Exemplos: Concretagem, Acesso e elevação. |
| Cliente | CPF, nome e telefone. | Identificado pelo CPF. |
| Atendente | Matrícula e nome. | Funcionário que opera o balcão. |

As situações possíveis de um equipamento são: disponível, reservado, locado, em vistoria, em manutenção e baixado.

## 2. Requisitos funcionais

| ID | Requisito |
|---|---|
| RF01 | O sistema deve consultar a disponibilidade de cada equipamento no período informado. |
| RF02 | O sistema deve registrar a reserva com número, data da solicitação, datas previstas de início e fim e situação ativa. |
| RF03 | O sistema deve registrar os itens da reserva com o valor da diária previsto. |
| RF04 | O sistema deve calcular o valor previsto da reserva somando os subtotais dos itens. |
| RF05 | O sistema deve permitir o cancelamento da reserva antes da retirada. |
| RF06 | O sistema deve expirar a reserva quando o cliente não comparecer até o fim do dia de início previsto. |
| RF07 | O sistema deve registrar a retirada após a conferência dos documentos do cliente. |
| RF08 | O sistema deve emitir o contrato de locação com os itens entregues e o valor da diária praticado. |
| RF09 | O sistema deve registrar o pagamento da locação por meio do sistema de pagamento externo. |
| RF10 | O sistema deve permitir locações com reserva prévia ou realizadas diretamente no balcão. |
| RF11 | O sistema deve registrar a vistoria de cada item devolvido, informando se houve avaria e o valor estimado do reparo. |
| RF12 | O sistema deve cobrar a avaria e enviar o equipamento para manutenção quando a vistoria constatar avaria. |
| RF13 | O sistema deve aplicar multa por atraso calculada sobre os dias excedentes. |
| RF14 | O sistema deve encerrar a locação e emitir o comprovante de devolução. |
| RF15 | O sistema deve registrar a conclusão do reparo ou a baixa do equipamento. |

## 3. Regras de negócio

| ID | Regra |
|---|---|
| RN01 | A reserva somente é registrada se todos os equipamentos estiverem disponíveis no período. |
| RN02 | Os itens de reserva e de locação não existem fora da reserva ou da locação a que pertencem. |
| RN03 | A retirada somente se conclui com o registro do pagamento. |
| RN04 | Cada item de locação é avaliado por no máximo uma vistoria. |
| RN05 | Cancelada ou expirada a reserva, os equipamentos voltam a ficar disponíveis. |
| RN06 | Não havendo avaria, o equipamento volta a ficar disponível imediatamente. |
| RN07 | Toda locação gera ao menos uma cobrança da própria locação e pode gerar cobranças de avaria e de multa por atraso. |
| RN08 | Cada cobrança permanece em aberto até que o pagamento seja registrado. |

---

<div align="center">

[⬅️ Escopo](escopo.md) · [🏠 Voltar ao início](../README.md) · [Critérios de avaliação ➡️](criterios-avaliacao.md)

</div>
