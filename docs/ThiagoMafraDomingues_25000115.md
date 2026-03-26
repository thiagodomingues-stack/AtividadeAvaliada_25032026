# Avaliação — Engenharia de Software
Sistema Integrado de Gestão de Farmácia — MVP Definido pelo Estudante

## Aluno: Thiago Mafra Domingues
## RA: 25000115
## Data: 25/03/2026

# 1. Definição do MVP
O MVP vai cobrir o processo de venda de produtos, incluindo a seleção de itens, validação de cliente e finalização da compra, garantindo também a baixa automática no estoque após a conclusão da venda.

## O que está dentro do MVP:

- Identificação de clientes
- Busca de produtos
- Inclusão de itens na venda
- Conferência de disponibilidade
- Baixa automática de estoque
- Finalização da venda

## O que está fora do MVP:
- Controle de fornecedores
- Gestão de contas a pagar
- Emissão de relatórios gerenciais

## Por que você fez essas escolhas:
 Pois esse fluxo representa a operação principal da farmácia, permitindo garantir o funcionamento básico das vendas com controle de estoque.

# 2. Regras de Negócio (mínimo: 5) Liste e descreva cada RN de forma clara.

## RN01 — Não permitir venda com produto inativo
Produtos desativados não podem ser vendidos.

## RN02 — Cliente deve ser identificado antes da finalização
Toda venda deve estar associada a um cliente identificado.

## RN03 — Estoque deve ser reduzido imediatamente após a venda
A baixa no estoque ocorre automaticamente após a finalização.

## RN04 — Cada venda deve registrar data e hora
Todas as vendas devem conter data e horário para controle.

## RN05 — Quantidade vendida deve ser maior que zero
Não é permitido registrar itens com quantidade igual ou menor que zero.

(Adicione mais se quiser.)

# 3. Requisitos Funcionais (mínimo: 8)
Liste os requisitos funcionais do seu MVP.

## RF01 — Identificar cliente
## RF02 — Buscar produto por nome ou código
## RF03 — Adicionar produto à venda
## RF04 — Informar quantidade do item
## RF05 — Validar disponibilidade em estoque
## RF06 — Calcular valor total da venda
## RF07 — Finalizar venda
## RF08 — Registrar saída no estoque

(Adicione mais se quiser.)

# 4. Requisitos Não Funcionais (mínimo: 4)
Liste os RNFs do sistema conforme seu MVP.

## RNF01 — Desempenho
O sistema deve processar vendas em até 2 segundos.

## RNF02 — Segurança
O sistema deve exigir autenticação para acesso às funcionalidades.

## RNF03 — Disponibilidade
O sistema deve funcionar durante o horário comercial sem interrupções.

## RNF04 — Usabilidade
O sistema deve permitir operação com poucos cliques.

(Adicione mais se quiser.)

# 5. Casos de Uso (mínimo: 10)
Atores: Atendente e Cliente

<img width="680" height="282" alt="image" src="https://github.com/user-attachments/assets/f1018c4e-091a-4219-ad69-af31f25ded12" />

# 6. Documentação dos Casos de Uso

## UC01 — Emitir Comprovante

- Ator(es): Sistema
- Descrição: Gera um documento com os dados da venda
- Pré-condições: Venda concluída
- Pós-condições: Documento disponível

## Fluxo Principal
- Sistema coleta informações da venda
- Gera documento
- Exibe ou imprime

##Fluxos Alternativos / Exceções
FA01 — Erro na impressão
→ Sistema informa falha

- Relacionamentos

- Include: —
- Extend: —

## UC02 — Consultar Produto

- Ator(es): Atendente
- Descrição: Permite localizar produtos cadastrados
- Pré-condições: Sistema disponível
- Pós-condições: Lista de produtos exibida

## Fluxo Principal
- Atendente digita informação
- Sistema realiza busca
- Sistema apresenta resultado

## Fluxos Alternativos / Exceções

## FA01 — Nenhum resultado encontrado
- Sistema exibe mensagem

- Relacionamentos

- Include: —
- Extend: —

## UC03 — Gerar Conta a Receber

- Ator(es): Sistema
- Descrição: Registra valor pendente de pagamento
- Pré-condições: Venda com pagamento futuro
- Pós-condições: Registro financeiro criado

## Fluxo Principal
- Sistema recebe dados
- Define vencimento
- Salva registro

## Fluxos Alternativos / Exceções

- FA01 — Falha ao salvar
- Sistema alerta erro

- Relacionamentos

- Include: —
- Extend: Registrar Venda a Prazo

## UC04 — Identificar Cliente

- Ator(es): Atendente
- Descrição: Busca cliente no sistema
- Pré-condições: Sistema ativo
- Pós-condições: Cliente localizado

## Fluxo Principal
- Atendente informa dado
- Sistema consulta base
- Exibe cliente

## Fluxos Alternativos / Exceções

- FA01 — Cliente inexistente
- Sugere cadastro

- Relacionamentos

- Include: —
- Extend: Cadastrar Cliente

## UC05 — Registrar Itens da Venda

- Ator(es): Atendente
- Descrição: Insere produtos na venda
- Pré-condições: Venda iniciada
- Pós-condições: Itens adicionados

## Fluxo Principal
- Seleciona produto
- Define quantidade
- Confirma inclusão

## Fluxos Alternativos / Exceções

- FA01 — Produto inválido
- Sistema rejeita

- Relacionamentos

- Include: —
- Extend: —

## UC06 — Finalizar Venda

- Ator(es): Atendente
- Descrição: Conclui operação de venda
- Pré-condições: Itens inseridos
- Pós-condições: Venda registrada

##Fluxo Principal
- Confirma dados
- Sistema calcula valor
- Registra venda

##Fluxos Alternativos / Exceções

- FA01 — Falha no sistema
- Operação cancelada

- Relacionamentos

- Include: —
- Extend: Registrar Venda a Prazo

## UC07 — Cadastrar Cliente

- Ator(es): Atendente
- Descrição: Adiciona novo cliente
- Pré-condições: Cliente não encontrado
- Pós-condições: Cliente incluído

##Fluxo Principal
- Preenche dados
- Valida informações
- Salva cadastro

##Fluxos Alternativos / Exceções

- FA01 — Dados incompletos
- Solicita correção

- Relacionamentos

- Include: —
- Extend: —

## UC08 — Verificar Estoque

- Ator(es): Sistema
- Descrição: Consulta quantidade disponível
- Pré-condições: Produto selecionado
- Pós-condições: Quantidade exibida

## Fluxo Principal
- Sistema consulta banco
- Retorna valor

##Fluxos Alternativos / Exceções

- FA01 — Sem estoque
- Bloqueia ação

- Relacionamentos

- Include: —
- Extend: —

## UC09 — Registrar Venda a Prazo

- Ator(es): Sistema
- Descrição: Define venda como pagamento futuro
- Pré-condições: Escolha de pagamento a prazo
- Pós-condições: Venda marcada

## Fluxo Principal
- Identifica forma de pagamento
- Marca venda
- Continua fluxo

## Fluxos Alternativos / Exceções

- FA01 — Cliente não autorizado
- Bloqueia operação

- Relacionamentos

- Include: —
- Extend: Gerar Conta a Receber

## UC10 — Realizar Venda

- Ator(es): Atendente, Cliente
- Descrição: Executa todo o fluxo de venda
- Pré-condições: Sistema em funcionamento
- Pós-condições: Venda concluída

## Fluxo Principal
- Inicia operação
- Identifica cliente
- Busca produto
- Confere estoque
- Adiciona itens
- Finaliza venda
- Emite comprovante

##Fluxos Alternativos / Exceções

- FA01 — Item indisponível
- Venda interrompida

- FA02 — Cliente ausente
- Solicita cadastro

- Relacionamentos

- Include: Identificar Cliente, Consultar Produto, Verificar Estoque
- Extend: Finalizar Venda
