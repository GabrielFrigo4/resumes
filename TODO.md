# TODO / Melhorias Futuras

### Evolução: Geração Automática dos Templates

**Objetivo:** Eliminar a necessidade de atualizar os arquivos `template-pt.tex` e `template-en.tex` manualmente. Quando o `resume-pt.tex` ou `resume-en.tex` mudarem estruturalmente, os templates devem ser re-gerados por um script que limpa as informações pessoais.

**Como implementar:**

1. Criar um script (ex: `scripts/generate_templates.py` ou `.sh`).
2. O script deve ler `Resume/resume-pt.tex`.
3. Utilizar Expressões Regulares (Regex) ou parser para buscar e substituir blocos como os detalhes de _Experiência Profissional_, _Projetos_, e _Formação_ por _placeholders_ como:
   `% PERSONALIZAR: Adicione suas experiências aqui.`
4. O script cospe o resultado formatado dentro da pasta `Template/`.
5. (**Bônus**) Adicionar um comando no `Makefile` (ex: `make generate-templates`) para rodar esse script e até integrar isso no GitHub Actions!
