<sub>[🏠 Início](../README.md) › Diagramas › Sequência</sub>

# 3. Diagrama de Sequência: Registrar Devolução

## 1. Descrição

Este diagrama apresenta a interação entre os objetos durante o caso de uso Registrar Devolução, utilizando os estereótipos de análise boundary, control e entity.

## 2. Diagrama

<p align="center">

![Diagrama de sequência](../imagens/Diagrama de Sequencia.drawio)

</p>

## 3. Lifelines

| Lifeline | Estereótipo | Papel |
|---|---|---|
| Atendente | Ator | Inicia o cenário e recebe o comprovante |
| :TelaDeDevolucao | «boundary» | Conversa com o atendente |
| :ControleDeDevolucao | «control» | Coordena o cenário |
| loc:Locacao | «entity» | A locação que está sendo devolvida |
| item:ItemLocacao | «entity» | Cada item devolvido |
| eq:Equipamento | «entity» | O equipamento do item |
| v:Vistoria | «entity» | Criada em cada vistoria |
| cm:Cobranca / ca:Cobranca | «entity» | Cobranças de multa e de avaria, criadas durante o cenário |

## 4. Fragmentos combinados

| Fragmento | Guarda | O que acontece |
|---|---|---|
| opt | [dataDevolucao > dataDevolucaoPrevista] | Calcula os dias excedentes e cria a cobrança de multa |
| loop | [para cada item de locação devolvido] | Envia o equipamento para vistoria e registra o laudo |
| alt | [houveAvaria = true] | Cobra a avaria e envia o equipamento para manutenção |
| alt | [houveAvaria = false] | Libera o equipamento |

## 5. Notação

- Quadro externo **sd Registrar Devolução**.
- Mensagens síncronas em linha cheia, e retornos tracejados só quando o valor importa.
- Criação de objetos com mensagem tracejada «create».
- Quem fala com quem: ator ↔ boundary ↔ control ↔ entity.
- Toda mensagem às entidades corresponde a uma operação do diagrama de classes.

---

<div align="center">

[⬅️ Classes](classes.md) · [🏠 Voltar ao início](../README.md) · [Atividades ➡️](atividades.md)

</div>
