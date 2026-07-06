# Falha na instalação das dependências de sistema

Status: bloqueado por privilégios administrativos.

Comandos tentados:

```bash
sudo apt update
sudo apt install -y git curl wget unzip zip build-essential ca-certificates \
  software-properties-common openjdk-17-jdk maven python3 python3-pip \
  python3-venv python3-dev graphviz universal-ctags
```

Resultado: o `sudo` exigiu senha em terminal interativo. Uma tentativa direta com
`apt` também falhou por falta de permissão para obter o lock em
`/var/lib/apt/lists/lock`.

Dependências ausentes confirmadas: Java, Maven, pip, Graphviz e ctags. O Python
3.12.3 e o Git 2.43.0 já estão disponíveis.

Ação necessária: executar os comandos acima em um terminal local com um usuário
autorizado a usar `sudo` e repetir as validações.
