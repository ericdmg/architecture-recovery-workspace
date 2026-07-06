# Falha no build do Retriever

Comando executado:

```bash
cd tools/retriever
mvn clean verify
```

Trecho final do log:

```text
/bin/bash: mvn: command not found
```

O build não chegou a iniciar porque o Maven não está instalado.
