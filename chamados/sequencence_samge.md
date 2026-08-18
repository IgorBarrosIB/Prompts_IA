# Execução de Script SQL — Ambiente TCTI

## Objetivo
Criar a sequência `sequence_generator` no schema `public`, ambiente **TCTI**.

## Script

```sql
CREATE SEQUENCE IF NOT EXISTS public.sequence_generator
    INCREMENT 50
    START 1050
    MINVALUE 1
    MAXVALUE 9223372036854775807
    CACHE 1;

ALTER SEQUENCE public.sequence_generator
    OWNER TO usr_samgeold;

GRANT ALL ON SEQUENCE public.sequence_generator TO usr_samgeold;
