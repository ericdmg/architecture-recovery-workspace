# Falha ao abrir help do SemArc

Comando de validação equivalente executado com o Python do sistema, pois o
ambiente virtual não pôde ser criado:

```bash
python3 tools/semarc/SemArc/SemArc.py --help
```

Log:

```text
Traceback (most recent call last):
  File "tools/semarc/SemArc/SemArc.py", line 5, in <module>
    from cluster_project import cluster_project
  File "tools/semarc/SemArc/cluster_project.py", line 7, in <module>
    import numpy as np
ModuleNotFoundError: No module named 'numpy'
```

O teste deve ser repetido depois da criação bem-sucedida do `.venv` e da
instalação das dependências.
