# Segurança da organização quorum-bench

Documento interno QUORUM · 15/11/2026 · Estação: Construir · Artefato: política de segurança da organização

Vale para todos os repositórios desta organização que não tenham política própria.

## Como avisar de uma falha

Não abra issue: a issue fica à vista de todo colaborador. Mande o aviso direto a quem mantém a organização, por mensagem fechada. Diga o que acontece, como reproduzir, o que fica exposto e desde quando. Não teste em produção nem com dado de pessoa: use o ambiente local, que só tem dado fictício.

## O que acontece depois

1. A falha é confirmada e classificada pelo manual do plantão (repositório [docs](https://github.com/quorum-bench/docs), `docs/06-operacao/`).
2. Se houver dado de pessoa envolvido, vale o runbook de vazamento, com o encarregado.
3. A correção entra como qualquer mudança: o teste que reprovava antes, a revisão separada e a publicação aprovada por uma pessoa.

## O que já protege

- O gitleaks roda antes de cada envio, e nenhum segredo entra em repositório.
- A semente fictícia recusa rodar fora do ambiente local.
- Cada serviço entra no banco com o próprio papel e só executa as funções que o código dele chama.
