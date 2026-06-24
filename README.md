# Architecture Recovery Workspace

Repositório de trabalho da pesquisa de recuperação arquitetural em sistemas baseados em microsserviços.

Este repositório organiza sistemas-alvo, ferramentas externas, scripts próprios, configurações experimentais, resultados, modelos de referência e metadados de rastreabilidade.

## Estrutura

- `subjects/`: repositórios dos sistemas analisados.
- `tools/`: ferramentas externas, como Retriever e SemArc.
- `scripts/`: scripts próprios de preparação, execução, parsing e conversão.
- `experiments/`: configurações dos cenários experimentais.
- `results/`: saídas geradas pelos fluxos.
- `ground-truth/`: arquiteturas conhecidas/documentadas e modelos esperados.
- `metadata/`: inventário dos repositórios, commits, versões e observações.
- `docs/`: notas metodológicas e decisões da pesquisa.

## Submódulos

Os repositórios externos devem ser adicionados como submódulos Git para preservar a rastreabilidade dos commits analisados.

Após clonar este repositório em outra máquina, usar:

```bash
git submodule update --init --recursive

Crie o inventário inicial:

```bash
cat > metadata/repositories.tsv <<'EOF'
category	name	path	url	notes
