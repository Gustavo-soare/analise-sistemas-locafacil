<h1 align="center">🏗️ LocaFácil — Modelagem UML</h1> <p align="center"> Especificação UML de um sistema de <b>locação de equipamentos para obras</b>, da reserva à devolução. </p> <p align="center"> <img src="https://img.shields.io/badge/UML-2.5-blue" alt="UML 2.5"> <img src="https://img.shields.io/badge/draw.io-diagramas-orange" alt="draw.io"> <img src="https://img.shields.io/badge/Disciplina-An%C3%A1lise%20de%20Sistemas-orange" alt="Análise de Sistemas"> <img src="https://img.shields.io/badge/IF%20Goiano-2026-darkgreen" alt="IF Goiano"> </p>
📋 Sumário
Sobre o projeto
Diagramas
1. Casos de uso
2. Classes
3. Sequência — Registrar Devolução
4. Atividades
5. Máquina de estados
Estrutura do repositório
Como editar os diagramas
Autor
📌 Sobre o projeto

A LocaFácil aluga equipamentos para obras de pequeno porte: betoneiras, andaimes, compactadores, martelos rompedores e geradores. O controle era feito em planilhas e num caderno de retiradas, o que causava:

❌ reservas duplicadas
❌ equipamentos entregues sem conferência
❌ multas de atraso esquecidas

Este projeto especifica, em UML, o sistema que informatiza o processo completo:

Etapa	O que o sistema faz
Cadastro	Guarda clientes (CPF, nome e telefone) e equipamentos (código, descrição, diária, categoria e situação).
Reserva	Consulta a disponibilidade, registra a reserva e calcula o valor previsto. Permite cancelar e expira a reserva quando o cliente não comparece.
Retirada	Confere os documentos, emite o contrato de locação e registra o pagamento no sistema externo.
Devolução	Faz a vistoria de cada item, cobra avaria, aplica multa por atraso, encerra a locação e emite o comprovante.
📊 Diagramas
1. Diagrama de casos de uso

Atores primários Cliente e Atendente, e o ator de apoio Sistema de Pagamento. Os passos que sempre acontecem usam «include», e as situações excepcionais (avaria e atraso) usam «extend», com condição e ponto de extensão.

<p align="center"> <img src="diagramas/01-casos-de-uso.png" alt="Diagrama de casos de uso" width="100%"> </p>
2. Diagrama de classes

Feito em nível de especificação:

atributos privados e tipados, e operações públicas com assinatura completa;
multiplicidade nas duas pontas de todas as associações;
composição só onde a parte não existe sem o todo (itens da reserva e da locação);
enumerações para as situações e tipos;
restrições entre chaves para as regras que a multiplicidade não mostra.
<p align="center"> <img src="diagramas/02-classes.png" alt="Diagrama de classes" width="100%"> </p>
3. Diagrama de sequência — Registrar Devolução

Usa os estereótipos de análise boundary, control e entity, com três fragmentos combinados:

Fragmento	Situação
opt	devolução depois da data prevista: aplica a multa por atraso
loop	para cada item devolvido: registra a vistoria
alt	com avaria: cobra e envia para manutenção. Sem avaria: libera o equipamento
<p align="center"> <img src="diagramas/03-sequencia-registrar-devolucao.png" alt="Diagrama de sequência" width="100%"> </p>
4. Diagrama de atividades

O processo completo, da reserva à devolução, com raias para Cliente, Atendente e Sistema. Cobre o cadastro, a reserva (com cancelamento e expiração), a locação direta no balcão, a retirada, o pagamento, a devolução, a multa, as vistorias e o encerramento.

<p align="center"> <img src="diagramas/04-atividades.png" alt="Diagrama de atividades" width="70%"> </p>
5. Diagrama de máquina de estados

O ciclo de vida de um equipamento:

Disponível → Reservado → Locado → Em vistoria → Em manutenção → Baixado

<p align="center"> <img src="diagramas/05-estados-equipamento.png" alt="Diagrama de máquina de estados" width="80%"> </p>
📁 Estrutura do repositório

locafacil-uml/
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
    ├── D01-casos-de-uso.png
    ├── D02-classes.png
    ├── D03-sequencia-registrar-devolucao.png
    ├── D04-atividades.png
    └── D05-maquina-de-estados.png

🛠️ Como editar os diagramas

Os diagramas foram feitos no draw.io (diagrams.net). Para editar:

Acesse app.diagrams.net ou abra o draw.io instalado no computador.
Clique em Abrir diagrama existente e escolha o arquivo .drawio da pasta fontes/.
Depois de editar, exporte em Arquivo → Exportar como → PNG e substitua a imagem na pasta diagramas/, com o mesmo nome.
👤 Autor

Seu Nome Curso — Instituto Federal Goiano Disciplina: Análise de Sistemas · Prof. Lacordaire Kemel
