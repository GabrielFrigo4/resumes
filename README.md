# 📄 Gabriel Frigo | Currículos e Cartas de Apresentação (Resumes & Cover Letters)

[![Último Commit](https://img.shields.io/github/last-commit/GabrielFrigo4/Resumes?style=flat-square)](https://github.com/GabrielFrigo4/Resumes)
[![CI/CD LaTeX](https://img.shields.io/github/actions/workflow/status/GabrielFrigo4/Resumes/LaTeX.yml?label=LaTeX%20Build&style=flat-square)](https://github.com/GabrielFrigo4/Resumes/actions)

|                            🇧🇷 Português (PT-BR)                             |                               🇺🇸 English (EN-US)                                |
| :-------------------------------------------------------------------------: | :-----------------------------------------------------------------------------: |
|  [![Baixar CV em Português][download_resume_pt_icon]][download_resume_pt]   |    [![Baixar Resume em Inglês][download_resume_en_icon]][download_resume_en]    |
| [![Baixar Carta em Português][download_letter_pt_icon]][download_letter_pt] | [![Baixar Cover Letter em Inglês][download_letter_en_icon]][download_letter_en] |

---

## 📌 Sobre o Repositório

Este repositório armazena o código-fonte estruturado em LaTeX dos meus currículos profissionais e cartas de apresentação. Os documentos destacam minha experiência como **Engenheiro de Software versátil**, com competências que abrangem desde **programação de sistemas e computação gráfica** até **administração de servidores Linux/FreeBSD, arquitetura de software e infraestrutura em nuvem**.

A escolha de utilizar LaTeX reflete a busca por um controle tipográfico absoluto, versionamento de texto e a filosofia de tratar a documentação como código (_Docs as Code_).

## ⚙️ Automação (CI/CD)

Para manter o fluxo de atualização rápido e eficiente, este repositório conta com uma esteira de Integração e Entrega Contínuas (CI/CD) via **GitHub Actions**.

Sempre que uma alteração é enviada à branch principal:

1.  Um _runner_ do GitHub inicializa um ambiente com uma distribuição TeX e a ferramenta `chktex`.
2.  É feito um **Linting Automático**, emitindo avisos de qualidade e formatação diretamente nos logs da Action.
3.  Os arquivos `.tex` são compilados nativamente. Em caso de erros sintáticos críticos no código LaTeX, a execução é interrompida para evitar a publicação de PDFs quebrados.
4.  Os PDFs gerados ([`resume-pt.pdf`][download_resume_pt], [`resume-en.pdf`][download_resume_en], [`letter-pt.pdf`][download_letter_pt] e [`letter-en.pdf`][download_letter_en]) são automaticamente atualizados e disponibilizados para download na aba de _Releases_.

---

## 📖 Estrutura do Repositório

Os documentos estão divididos em dois idiomas, mantendo a mesma base de layout com informações adaptadas para os respectivos mercados:

```
Resumes/
├── Resume/
│   ├── resume-pt.tex        # Currículo em Português (PT-BR)
│   └── resume-en.tex        # Resume em Inglês (EN-US)
├── Letter/
│   ├── letter-pt.tex        # Carta de Apresentação em Português
│   └── letter-en.tex        # Cover Letter em Inglês
├── Template/
│   ├── template-pt.tex      # Template base em Português (com guias de personalização)
│   └── template-en.tex      # Template base em Inglês (com guias de personalização)
├── .github/workflows/
│   └── LaTeX.yml            # Pipeline CI/CD para compilação automática
└── README.md
```

### 📄 [Currículos](./Resume)

- 🇧🇷 **[`resume-pt.tex`](./Resume/resume-pt.tex):** Currículo em Português (PT-BR), ideal para vagas no Brasil, com foco no ecossistema de tecnologia nacional.
- 🇺🇸 **[`resume-en.tex`](./Resume/resume-en.tex):** Resume em Inglês (EN-US), direcionado para oportunidades internacionais.

### ✉️ [Cartas de Apresentação](./Letter)

- 🇧🇷 **[`letter-pt.tex`](./Letter/letter-pt.tex):** Carta de Apresentação em Português, com variáveis customizáveis para cargo e empresa.
- 🇺🇸 **[`letter-en.tex`](./Letter/letter-en.tex):** Cover Letter em Inglês, estruturada para candidaturas globais.

### 📝 [Templates Base](./Template)

Templates "limpos" e comentados do layout, otimizados para ATS e com **guias de personalização** (`% PERSONALIZAR:` / `% CUSTOMIZE:`) em cada seção para facilitar a criação de versões customizadas para cada vaga:

- 🇧🇷 **[`template-pt.tex`](./Template/template-pt.tex):** Template genérico em Português.
- 🇺🇸 **[`template-en.tex`](./Template/template-en.tex):** Template genérico em Inglês.

---

## 🎯 Como Personalizar para uma Vaga

1. **Copie o template** da sua língua preferida (`template-pt.tex` ou `template-en.tex`).
2. **Procure os comentários `% PERSONALIZAR:`** (ou `% CUSTOMIZE:`) — cada seção tem instruções de como adaptar.
3. **Nas cartas de apresentação**, edite apenas os `\newcommand` no início do arquivo:
    ```latex
    \newcommand{\targetRole}{Estágio em Desenvolvimento}
    \newcommand{\targetCompany}{Nome da Empresa}
    ```
4. **Compile** e envie!

---

## 🛠️ Como Compilar Localmente

Caso queira clonar este repositório para inspecionar o código, utilizar o layout ou fazer testes locais sem depender do CI/CD:

1.  Certifique-se de ter uma distribuição LaTeX instalada no seu sistema (como TeX Live no Linux/FreeBSD, ou MiKTeX/TeX Live no Windows via MSYS2).

2.  Clone este repositório na sua máquina:

```bash
git clone "https://github.com/GabrielFrigo4/Resumes.git"
```

3.  Utilize o `Makefile` incluído na raiz do projeto para automatizar e otimizar as compilações. Você pode gerar todos de uma vez ou direcionar para pastas específicas:

```bash
# Compilar todos os documentos do repositório
make all

# Compilar apenas os currículos (pasta Resume)
make resumes

# Compilar apenas as cartas (pasta Letter)
make letters

# Compilar apenas os templates (pasta Template)
make templates
```

4.  Para manter o ambiente limpo, removendo arquivos intermediários (como `.log`, `.aux`, `.out`) e os PDFs gerados localmente, basta utilizar o comando:

```bash
make clean
```

---

## 🔗 Links Úteis

- **Meu Perfil do GitHub:** [GabrielFrigo4](https://github.com/GabrielFrigo4)
- **LinkedIn:** [gabriel-frigo](https://www.linkedin.com/in/gabriel-frigo-b6727b275/)
- **Portfólio:** [gabrielfrigo.dev.br](https://gabrielfrigo.dev.br)

[download_resume_pt]: https://github.com/GabrielFrigo4/Resumes/releases/latest/download/resume-pt.pdf
[download_resume_pt_icon]: https://img.shields.io/badge/CURRÍCULO_PT--BR-Baixar_PDF-red?style=for-the-badge&logo=adobeacrobatreader
[download_resume_en]: https://github.com/GabrielFrigo4/Resumes/releases/latest/download/resume-en.pdf
[download_resume_en_icon]: https://img.shields.io/badge/RESUME_EN--US-Baixar_PDF-blue?style=for-the-badge&logo=adobeacrobatreader
[download_letter_pt]: https://github.com/GabrielFrigo4/Resumes/releases/latest/download/letter-pt.pdf
[download_letter_pt_icon]: https://img.shields.io/badge/CARTA_PT--BR-Baixar_PDF-darkred?style=for-the-badge&logo=adobeacrobatreader
[download_letter_en]: https://github.com/GabrielFrigo4/Resumes/releases/latest/download/letter-en.pdf
[download_letter_en_icon]: https://img.shields.io/badge/LETTER_EN--US-Baixar_PDF-darkblue?style=for-the-badge&logo=adobeacrobatreader
