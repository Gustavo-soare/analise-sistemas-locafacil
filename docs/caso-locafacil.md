<h1 align="center">📘 Caso LocaFácil</h1> <p align="center"> Resumo do estudo de caso e das entregas pedidas na atividade de <b>Análise de Sistemas</b>. </p>
🏢 A empresa

A LocaFácil aluga equipamentos para obras de pequeno porte, como betoneiras, andaimes, compactadores, martelos rompedores e geradores.

O problema

Hoje tudo é controlado em planilhas e num caderno de retiradas, e isso causa:

❌ Problema	Consequência
Reservas duplicadas	O mesmo equipamento é prometido para dois clientes
Entrega sem conferência	Não se sabe em que estado o equipamento saiu
Cobranças esquecidas	Multas de atraso deixam de ser cobradas
O objetivo

Especificar um sistema que informatize o processo da reserva à devolução.

📇 Cadastros
Cadastro	Dados	Observação
Equipamento	código, descrição, valor da diária, categoria e situação	Cada unidade física é um equipamento: dois andaimes iguais têm códigos diferentes
Categoria	nome	Exemplos: "Concretagem", "Acesso e elevação"
Cliente	CPF, nome e telefone	É identificado pelo CPF
Atendente	matrícula e nome	É o funcionário que opera o balcão

Situações possíveis de um equipamento: disponível · reservado · locado · em vistoria · em manutenção · baixado

🔄 O processo
1️⃣ Reserva
O cliente informa o período e os equipamentos que quer alugar.
O sistema consulta a disponibilidade de cada equipamento no período.
Se todos estiverem disponíveis, a reserva é registrada com número, data da solicitação e datas previstas de início e fim, na situação ativa.
A reserva tem itens, um por equipamento, e cada item guarda o valor da diária no momento da reserva. Os itens não existem sem a reserva.
O sistema calcula o valor previsto somando os subtotais dos itens.
Antes da retirada, o cliente pode cancelar. Se ele não comparecer até o fim do dia de início, a reserva expira. Nos dois casos, os equipamentos voltam a ficar disponíveis.
2️⃣ Retirada
O atendente confere os documentos do cliente e registra a retirada.
O sistema emite o contrato de locação, com número, data de retirada, data de devolução prevista e os itens entregues, cada um com o valor da diária praticado.
A retirada só se conclui com o pagamento registrado, processado por um sistema de pagamento externo.
A locação fica em andamento e os equipamentos ficam locados.
A locação pode vir de uma reserva ou ser feita direto no balcão.
3️⃣ Devolução
O atendente faz a vistoria de cada item e registra o laudo: se houve avaria e, havendo, o valor estimado do reparo.
Cada item é avaliado por no máximo uma vistoria.
Sem avaria, o equipamento volta a ficar disponível na hora.
Concluídas as vistorias, o sistema encerra a locação e o cliente recebe o comprovante de devolução.
⚠️ Situações excepcionais
Situação	O que acontece
Avaria	O sistema cobra a avaria e o equipamento vai para manutenção. Depois do reparo, volta ao estoque; se o reparo for inviável, recebe baixa.
Atraso	Se a devolução passar da data prevista, o sistema aplica multa pelos dias excedentes.
💰 Cobranças
Toda locação gera pelo menos uma cobrança, a da própria locação.
Ela pode gerar outras, dos tipos avaria e multa por atraso.
Cada cobrança fica em aberto até o pagamento ser registrado.
📝 O que o professor pediu
Nº	Diagrama	Exigências
1	Casos de uso	Atores e relacionamentos «include» e «extend»
2	Classes	Nível de especificação, com atributos tipados, assinaturas completas das operações, multiplicidades e os relacionamentos adequados
3	Sequência	Caso de uso Registrar Devolução, cobrindo o laço sobre os itens, a alternativa de avaria e a condição de atraso
4	Atividades	Processo completo, da reserva à devolução, com raias para Cliente, Atendente e Sistema
5	Máquina de estados	Ciclo de vida de um equipamento
📌 Orientações
✅ Modelar apenas o que o enunciado sustenta.
✅ Não inventar atributos nem operações sem um verbo correspondente no texto.
✅ Não usar getters e setters como operações.
✅ Usar composição só onde a parte não existe sem o todo.
