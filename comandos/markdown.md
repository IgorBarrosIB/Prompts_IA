## Sumário
1. Títulos
2. Ênfase e Formatação de Texto
3. Parágrafos e Quebras de Linha
4. Listas (ordenadas, não ordenadas, checklist, aninhadas)
5. Links (inline, referência, âncoras, e-mail)
6. Imagens
7. Código (inline, blocos, diff, syntax highlight)
8. Citações (blockquote)
9. Linhas Horizontais
10. Tabelas (alinhamento, células complexas)
11. Notas de Rodapé (footnotes)
12. Listas de Definição
13. HTML dentro de Markdown
14. Caracteres de Escape
15. Comentários
16. Seções Colapsáveis (details/summary)
17. Emojis
18. Diagramas (Mermaid)
19. Fórmulas Matemáticas (LaTeX)
20. Front Matter (metadados YAML)
21. Badges (selos de status)
22. Boas práticas para README de projetos
23. Exemplo completo de README técnico

# 1. Títulos
# Título 1
## Título 2
### Título 3
#### Título 4
##### Título 5
###### Título 6

# 2. Ênfase e Formatação de Texto
**negrito**
*itálico*
***negrito e itálico***
~~riscado~~
`código inline`

# 3. Parágrafos e Quebras de Linha
Este é o primeiro parágrafo.

Este é o segundo parágrafo (separado por linha em branco).

Linha 1  
Linha 2 (dois espaços no final força quebra)

# 4. Listas

## Não ordenada
- Item 1
- Item 2
  - Subitem 2.1

## Ordenada
1. Primeiro
2. Segundo
   1. Sub-item

## Checklist
- [x] Tarefa concluída
- [ ] Tarefa pendente

# 5. Links
[Texto do link](https://exemplo.com)
[Link com título](https://exemplo.com "Título")
[Referência][1]

[1]: https://exemplo.com "Título via referência"

[Âncora interna](#instalação)

<contato@exemplo.com>

# 6. Imagens
![Texto alternativo](https://exemplo.com/imagem.png)

[![Imagem clicável](imagem.png)](https://link-destino.com)

# 7. Código

Inline: `array_map()`

Bloco:
​```php
public function soma($a, $b) {
    return $a + $b;
}
​```

Diff:
​```diff
- $data = $request->all();
+ $data = $request->validated();
​```

# 8. Citações (Blockquote)
> Citação simples.

> Nível 1
> > Nível 2 (aninhado)

> ⚠️ **Atenção:** operação irreversível.

# 9. Linhas Horizontais
---
***
___

# 10. Tabelas
| Nome  | Cargo     |
|-------|-----------|
| Igor  | Tech Lead |

| Esquerda | Centro | Direita |
|:---------|:------:|--------:|
| a        |   b    |       c |

# 11. Notas de Rodapé
Este texto tem uma nota[^1].

[^1]: Explicação da nota de rodapé.

# 12. Listas de Definição
Termo 1
: Definição do termo 1

Termo 2
: Definição do termo 2

# 13. HTML dentro de Markdown
<p align="center">
  <img src="logo.png" width="200">
</p>

Texto em <sub>subscrito</sub> e <sup>sobrescrito</sup>.

# 14. Caracteres de Escape
\*não é itálico\*
\# não é título
Use \` para crase literal

# 15. Comentários
<!-- Isso não aparece na renderização -->

# 16. Seções Colapsáveis
<details>
<summary>Clique para expandir</summary>

Conteúdo oculto aqui.

</details>

# 17. Emojis
:rocket: :white_check_mark: :warning: :bug:

# 18. Diagramas (Mermaid)
​```mermaid
graph TD
    A[Requisição] --> B{Autenticado?}
    B -->|Sim| C[Retorna dados]
    B -->|Não| D[Erro 401]
​```

# 19. Fórmulas Matemáticas (LaTeX)
Inline: $E = mc^2$

Bloco:
$$
\int_0^\infty e^{-x^2} dx = \frac{\sqrt{\pi}}{2}
$$

# 20. Front Matter (YAML)
---
title: "Documentação da API"
author: "Igor Barros"
date: 2026-08-18
---

# 21. Badges
![Build](https://img.shields.io/badge/build-passing-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)

# 22. Boas práticas para README
- H1 (projeto) → H2 (seções) → H3 (subseções)
- Blocos de código com linguagem especificada
- Checklist para roadmap
- Tabelas para parâmetros de API
- `<details>` para logs longos
- Badges no topo do README

# 23. Exemplo completo de README técnico
---
title: "Sistema ICMBio"
author: "Igor Barros"
---

# Sistema de Integração ICMBio

![Build](https://img.shields.io/badge/build-passing-brightgreen)

## Descrição
Integração de dados ambientais com PostgreSQL.

## Instalação
​```bash
git clone https://github.com/icmbio/sistema.git
composer install
​```

## Roadmap
- [x] Migração do banco
- [ ] Dashboard Power BI

