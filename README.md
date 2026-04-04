# cv_latex

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
