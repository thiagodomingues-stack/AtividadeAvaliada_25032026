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

## UC01 — Emitir Comprovante

- Ator(es): Sistema
- Descrição: Gera o comprovante da venda realizada
- Pré-condições: Venda finalizada
- Pós-condições: Comprovante emitido

## Fluxo Principal
- Sistema recebe dados da venda
- Gera comprovante
- Disponibiliza para impressão

##Fluxos Alternativos / Exceções
FA01 — Falha na geração
→ Sistema exibe erro

- Relacionamentos

- Include: —
- Extend: —

## UC02 — Consultar Produto

- Ator(es): Atendente
- Descrição: Permite buscar produtos no sistema
- Pré-condições: Sistema ativo
- Pós-condições: Produto exibido

## Fluxo Principal
- Atendente informa nome/código
- Sistema busca produto
- Sistema exibe resultado
- Fluxos Alternativos / Exceções

## FA01 — Produto não encontrado
- Sistema informa indisponibilidade

- Relacionamentos

- Include: —
- Extend: —

## UC03 — Gerar Conta a Receber

- Ator(es): Sistema
- Descrição: Cria registro financeiro de venda a prazo
- Pré-condições: Venda a prazo realizada
- Pós-condições: Conta registrada

## Fluxo Principal
- Sistema recebe dados da venda
- Define vencimento
- Registra conta

## Fluxos Alternativos / Exceções

- FA01 — Erro no registro
- Sistema notifica falha

- Relacionamentos

- Include: —
- Extend: Registrar Venda a Prazo

## UC04 — Identificar Cliente

- Ator(es): Atendente
- Descrição: Localiza cliente no sistema
- Pré-condições: Sistema ativo
- Pós-condições: Cliente identificado

## Fluxo Principal
- Atendente informa dados
- Sistema busca cliente
- Exibe cliente

## Fluxos Alternativos / Exceções

- FA01 — Cliente não encontrado
- Redireciona para cadastro

- Relacionamentos

- Include: —
- Extend: Cadastrar Cliente

## UC05 — Registrar Itens da Venda

- Ator(es): Atendente
- Descrição: Adiciona produtos à venda
- Pré-condições: Venda iniciada
- Pós-condições: Itens registrados

## Fluxo Principal
- Atendente seleciona produto
- Informa quantidade
- Sistema adiciona item
## Fluxos Alternativos / Exceções

- FA01 — Quantidade inválida
- Sistema solicita correção

- Relacionamentos

- Include: —
- Extend: —

## UC06 — Finalizar Venda

- Ator(es): Atendente
- Descrição: Conclui o processo de venda
- Pré-condições: Itens registrados
- Pós-condições: Venda concluída

##Fluxo Principal
- Atendente confirma venda
- Sistema calcula total
- Sistema finaliza

##Fluxos Alternativos / Exceções

- FA01 — Erro no fechamento
- Sistema cancela operação

- Relacionamentos

- Include: —
- Extend: Registrar Venda a Prazo

## UC07 — Cadastrar Cliente

- Ator(es): Atendente
- Descrição: Registra novo cliente
- Pré-condições: Cliente não cadastrado
- Pós-condições: Cliente salvo

##Fluxo Principal
- Atendente insere dados
- Sistema valida
- Sistema salva

##Fluxos Alternativos / Exceções

- FA01 — Dados inválidos
- Sistema solicita correção

- Relacionamentos

- Include: —
- Extend: —

## UC08 — Verificar Estoque

- Ator(es): Sistema
- Descrição: Verifica disponibilidade de produto
- Pré-condições: Produto selecionado
- Pós-condições: Estoque validado

## Fluxo Principal
- Sistema consulta estoque
- Retorna quantidade

##Fluxos Alternativos / Exceções

- FA01 — Estoque insuficiente
- Sistema bloqueia venda

- Relacionamentos

- Include: —
- Extend: —

## UC09 — Registrar Venda a Prazo

- Ator(es): Sistema
- Descrição: Registra venda com pagamento futuro
- Pré-condições: Venda selecionada como a prazo
- Pós-condições: Venda registrada

## Fluxo Principal
- Sistema identifica tipo de pagamento
- Marca como a prazo
- Continua processo

## Fluxos Alternativos / Exceções

- FA01 — Cliente inválido
- Sistema impede operação

- Relacionamentos

- Include: —
- Extend: Gerar Conta a Receber

## UC10 — Realizar Venda

- Ator(es): Atendente, Cliente
- Descrição: Processo completo de venda
- Pré-condições: Sistema ativo
- Pós-condições: Venda registrada

## Fluxo Principal
- Atendente inicia venda
- Identifica cliente
- Consulta produto
- Verifica estoque
- Registra itens
- Finaliza venda
- Emite comprovante

##Fluxos Alternativos / Exceções

- FA01 — Produto sem estoque
-  Venda interrompida

- FA02 — Cliente não cadastrado
-  Direciona para cadastro

- Relacionamentos

- Include: Identificar Cliente, Consultar Produto, Verificar Estoque
- Extend: Finalizar Venda
