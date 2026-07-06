# Resumo de validação das ferramentas

Data: 2026-07-06T15:02:32-03:00

## Resultado geral

Status: validação diagnóstica concluída; instalação e testes funcionais
bloqueados pela ausência de privilégios administrativos para instalar pacotes.

## Sistema

```text
Linux ericdmg-Nitro-AN515-47 6.17.0-29-generic #29~24.04.1-Ubuntu SMP PREEMPT_DYNAMIC Mon May 11 10:30:58 UTC 2 x86_64 x86_64 x86_64 GNU/Linux
```

## Ferramentas

```text
Java: ausente
Maven: ausente
Python: Python 3.12.3
pip: ausente
Git: git version 2.43.0
Graphviz: ausente
ctags do sistema: ausente
```

O binário Linux de ctags empacotado no SemArc recebeu permissão de execução em
`SemArc/ext_tools/ctags_linux/ctags`.

## Repositórios

- `tools/retriever`: presente, porém configurado para o repositório inesperado
  `View-Based-Reverse-Engineering/Retriever`;
- `tools/semarc`: presente e configurado para `xjtu-enre/TSE2025SemArc`;
- todos os submódulos listados estavam inicializados.

## Validações

- Retriever: build não iniciado porque `mvn` está ausente;
- SemArc: `.venv` não criado por ausência de `python3-venv`/`ensurepip`;
- dependências Python: não instaladas;
- `SemArc.py --help`: falhou no import de `numpy`;
- recursos NLTK: não baixados porque o ambiente Python não pôde ser preparado;
- `semantic_analysis`: deliberadamente não executado, sem API paga.

Consulte `docs/issues/` para os logs e ações recomendadas.
