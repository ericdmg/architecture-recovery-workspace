# Falha na instalação das dependências Python do SemArc

A criação de `tools/semarc/.venv` falhou porque o módulo `ensurepip` não está
disponível. No Ubuntu, ele é fornecido por `python3-venv`, cuja instalação ficou
bloqueada pela exigência de senha do `sudo`.

Além disso, o ambiente possui Python 3.12.3, enquanto
`tools/semarc/SemArc/requirements.txt` fixa dependências antigas, incluindo
`numpy==1.21.4`, cuja faixa publicada não contempla Python 3.12.

Ação recomendada:

1. instalar `python3-venv` e as demais dependências de sistema;
2. preferencialmente criar o ambiente com Python 3.10;
3. recriar `.venv` e instalar `SemArc/requirements.txt` sem alterar o código da
   ferramenta nesta etapa.
