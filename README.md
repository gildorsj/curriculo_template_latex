# curriculo_template_latex

Template de currículo (CV) escrito em LaTeX, compilado com **XeLaTeX**.

## Requisitos

- Distribuição LaTeX:
  - [TeX Live](https://www.tug.org/texlive/) (Linux/macOS)
  - [MiKTeX](https://miktex.org/) (Windows)
- Compilador: **XeLaTeX** (incluso nas distribuições acima)
- Fontes (veja a seção [Fontes](#fontes))

## Fontes

As fontes abaixo devem estar instaladas no sistema para que o documento seja compilado corretamente:

| Fonte | Uso | Link |
|-------|-----|------|
| [Source Sans Pro](https://fonts.google.com/specimen/Source+Sans+3) | Texto principal | Google Fonts |
| [Lato](https://fonts.google.com/specimen/Lato) | Títulos e destaques | Google Fonts |
| [Font Awesome 5](https://fontawesome.com/download) | Ícones | fontawesome.com |

> **Dica (Linux/macOS):** Baixe os arquivos `.ttf` ou `.otf` e copie para `~/.fonts/` (Linux) ou `~/Library/Fonts/` (macOS). Execute `fc-cache -fv` para atualizar o cache de fontes.

## Tema de cores

O currículo possui dois esquemas de cores prontos para uso:

| Tema | Variável base | Prévia |
|------|---------------|--------|
| Azul (padrão) | `cvblue` | Azul petróleo `#1D6E9E` |
| Verde | `cvgreen` | Verde esmeralda `#1D9E75` |

Para **trocar o tema**, faça um _find & replace_ em `main.tex` com as substituições abaixo:

**Azul → Verde:**
| Encontrar | Substituir por |
|-----------|----------------|
| `cvblue`     | `cvgreen`     |
| `cvbluelt`   | `cvgreenlt`   |
| `cvbluemid`  | `cvgreenmid`  |
| `cvbluedark` | `cvgreendark` |

**Verde → Azul:** faça o inverso da tabela acima.

> **Dica:** No VS Code use `Ctrl+H` → marque _Match Case_ e _Match Whole Word_ para evitar substituições parciais indesejadas. No Overleaf use o menu _Find & Replace_ (`Ctrl+H`).

## Como compilar

### Compilação direta

```bash
xelatex main.tex
```

### Com latexmk (recomendado)

```bash
latexmk -xelatex main.tex
```

Para limpar os arquivos auxiliares gerados:

```bash
latexmk -c
```

## Estrutura do projeto

```
cv_latex/
├── main.tex          # Arquivo principal do currículo
├── main.pdf          # PDF gerado (não versionado)
└── README.md
```

## Licença

Distribuído sob a licença MIT. Consulte o arquivo [LICENSE](LICENSE) para mais detalhes.
