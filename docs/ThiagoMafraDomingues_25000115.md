# Avaliação — Engenharia de Software
Sistema Integrado de Gestão de Farmácia — MVP Definido pelo Estudante

## Aluno: Thiago Mafra Domingues
## RA: 25000115
## Data: 25/03/2026

# 1. Definição do MVP
O MVP vai cobrir todo o processo de venda do produto, do cadastro do cliente até a emissão da nota fiscal, isso inclui a atualização automática do estoque de produtos após a compra.

## O que está dentro do MVP:

- Cadastro do clientes
- Consulta do produtos
- Registro da vendas
- Verificação do estoque
- Atualização do estoque
- Emissão do comprovante

## O que está fora do MVP:
- Compras com fornecedor
- Contas a pagar
- Relatórios avançados

## Por que você fez essas escolhas:
 Pois representa melhor a área de vendas da farmácia venda, além que, garante o funcionamento básico do negócio.

# 2. Regras de Negócio (mínimo: 5)
Liste e descreva cada RN de forma clara.

## RN01 — Venda somente com estoque disponível
O sistema não permite venda de produtos sem quantidade suficiente.

## RN02 — Cadastro obrigatório para venda a prazo
O cliente deve ter uma conta na loja para fazer vendas a prazo

## RN03 — Atualização automática de estoque
Toda venda reduz o numero do estoque.

## RN04 — Vendas devem ter numeração de identificação
Vendas geram um numero unico para identificação e busca.

## RN05 — Produtos devem possuir preço válido
Nenhum produto pode ser vendido sem um preço escolhido anteriormente.

(Adicione mais se quiser.)

# 3. Requisitos Funcionais (mínimo: 8)
Liste os requisitos funcionais do seu MVP.

## RF01 — Cadastrar cliente
## RF02 — Consultar cliente
## RF03 — Cadastrar produto
## RF04 — Consultar produto
## RF05 — Registrar venda
## RF06 — Consultar venda
## RF07 — Emitir comprovante da venda
## RF08 — Atualizar estoque após venda

(Adicione mais se quiser.)

# 4. Requisitos Não Funcionais (mínimo: 4)
Liste os RNFs do sistema conforme seu MVP.

## RNF01 — Desempenho
O sistema deve responder consultas em até 3 segundos.
## RNF02 — Segurança
Somente usuários com autoridade podem realizar vendas.
## RNF03 — Disponibilidade
O sistema deve estar disponível 100% do tempo.
## RNF04 — Usabilidade
A interface deve ser simples e intuitiva.

(Adicione mais se quiser.)

# 5. Casos de Uso (mínimo: 10)
Atores: Atendente e Cliente

<img width="680" height="282" alt="image" src="https://github.com/user-attachments/assets/f1018c4e-091a-4219-ad69-af31f25ded12" />

# 6. Documentação dos Casos de Uso
Para cada caso de uso, utilize o template abaixo:
UCXX — Nome do Caso de Uso
Ator(es):
Descrição:
Pré-condições:
Pós-condições:

Fluxo Principal
Fluxos Alternativos / Exceções
FA01 —
FA02 —
Relacionamentos
Include: (listar quando aplicável)
Extend: (listar quando aplicável)
Inserir o diagrama de atividades do Caso de Uso, demonstrando tudo o fluxo princial e alternativos/exceções.
Repita essa estrutura para todos os seus casos de uso (mínimo 10).
