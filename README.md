# 🔧 Sistema de Gestão de Ordens de Serviço - Oficina Mecânica

## 📘 Descrição do Projeto

Este projeto apresenta um modelo conceitual e lógico de banco de dados para um sistema de **controle e gerenciamento de ordens de serviço** em uma **oficina mecânica**. O objetivo é registrar todas as informações relacionadas aos serviços realizados, equipes envolvidas, veículos atendidos e peças utilizadas.

## 🎯 Objetivo

Modelar um banco de dados relacional para representar de forma eficiente o fluxo de trabalho da oficina, desde a entrada do cliente e seu veículo, até a execução e finalização dos serviços.

## 🧱 Entidades Principais

- **Cliente:** Dados do cliente que leva o veículo à oficina.
- **Veículo:** Informações do carro pertencente ao cliente.
- **Equipe:** Grupo de mecânicos responsável pela execução da ordem de serviço.
- **Mecânico:** Profissionais com especialidades específicas, vinculados a uma equipe.
- **Ordem de Serviço (OS):** Documento que representa os serviços a serem executados.
- **Serviço:** Atividades que podem ser realizadas em um veículo, com custo de mão de obra.
- **Peça:** Componentes usados na manutenção ou conserto de veículos.

## 🔗 Relacionamentos

- Cada **cliente** pode ter vários **veículos**.
- Cada **veículo** pode gerar várias **ordens de serviço**.
- Cada **ordem de serviço** é atribuída a uma **equipe**.
- Cada **equipe** pode ter vários **mecânicos**.
- Uma **ordem de serviço** pode conter vários **serviços** e várias **peças**.
- Os custos de mão de obra e peças compõem o valor total da OS.

## 🛠️ Tabelas Associativas

- **OS_Servico:** Relaciona os serviços executados em cada OS.
- **OS_Peca:** Relaciona as peças utilizadas em cada OS.

## 📌 Observações

- O modelo assume que o cliente autoriza previamente os serviços executados.
- Os relacionamentos foram modelados com base em práticas comuns em oficinas mecânicas, onde equipes fixas realizam todo o processo.
- Algumas decisões de modelagem foram assumidas para cobrir lacunas da narrativa, como: 
  - Cadastro de peças com valor unitário;
  - Subtotal de cada item para facilitar cálculos e relatórios;
  - Campo `autorizado` como booleano para controle da execução.

## 🧪 Tecnologias

- Modelo criado com **MySQL Workbench**.
- Script SQL disponível na pasta `/sql`.

## 📂 Estrutura

```
/sql
  └── modelo_oficina.sql

/modelo
  └── diagrama.mwb (opcional)

README.md
```