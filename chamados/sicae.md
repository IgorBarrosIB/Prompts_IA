# Execução de Script SQL — Ambiente de Produção (Schema SICAE)

## Objetivo
Consultar dados de pessoa/pessoa física e inserir novo usuário no schema `sicae`.

## Ambiente
> ⚠️ **PRODUÇÃO** — executar com atenção redobrada.

## Scripts de Consulta (validação prévia)

```sql
-- Buscar pessoa pelo nome
SELECT * FROM corporativo.pessoa WHERE no_pessoa LIKE '%';

-- Buscar pessoa física pelo CPF
SELECT * FROM corporativo.pessoa_fisica WHERE nu_cpf = '';

-- Buscar pessoa pelo sq_pessoa
SELECT * FROM corporativo.pessoa WHERE sq_pessoa = ;

-- Verificar se já existe usuário vinculado
SELECT * FROM sicae.usuario WHERE sq_pessoa = ;

INSERT INTO sicae.usuario (
    sq_pessoa,
    tx_senha,
    st_ativo,
    sq_tipo_documento_login
)
VALUES (
    ,
    '612b06b9a8360fed19556dada4d0fdf5',
    TRUE,
    13
);
