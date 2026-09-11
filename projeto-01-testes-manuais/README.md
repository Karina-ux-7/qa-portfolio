# Projeto 01 Testes Manuais

Este projeto tem como objetivo demonstrar atividades práticas de Quality Assurance com foco em testes manuais de uma aplicação web.

A aplicação utilizada foi o SauceDemo, com execução de cenários relacionados a autenticação, carrinho e checkout.

## Objetivo do projeto

Aplicar técnicas de testes de software em uma aplicação web, documentando o processo de análise, execução, validação de resultados e registro de evidências.

## Escopo testado

Foram validadas as seguintes funcionalidades:

### Login

- Login com dados válidos
- Login com usuário inválido
- Login com senha inválida
- Login com campos vazios
- Login com usuário bloqueado

### Carrinho

- Adição de produto ao carrinho
- Remoção de produto
- Atualização do contador do carrinho
- Validação de múltiplos produtos

### Checkout

- Checkout com dados válidos
- Conclusão de compra com sucesso
- Validação de nome obrigatório
- Validação de CEP obrigatório

## Casos de teste

Foram executados 12 casos de teste manuais.

Todos os casos possuem:

- objetivo
- pré-condição
- passos
- resultado esperado
- resultado obtido
- status
- evidência

Os casos completos estão disponíveis em:

`casos-de-teste.md`

## Evidências

As evidências das execuções estão organizadas na pasta:

`evidencias/`

Cada caso de teste possui um link direto para sua respectiva evidência.

## Resultado

Foram executados 12 casos de teste.

Status final:

- 12 casos aprovados
- 0 casos reprovados
- 0 bugs confirmados

Durante a execução, também foi feita validação do ambiente para diferenciar possíveis falhas da aplicação de comportamentos causados pelo navegador.

## Estrutura do projeto

- `casos-de-teste.md` documentação dos casos de teste
- `bugs.md` estrutura para registro de defeitos
- `evidencias/` evidências das execuções

## Status

Concluído.

---

**Karina**  
Quality Assurance
