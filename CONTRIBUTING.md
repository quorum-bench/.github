# Como contribuir com a organização quorum-bench

Documento interno QUORUM · 15/11/2026 · Estação: Construir · Artefato: guia de contribuição da organização

Vale para pessoa e para agente, em todos os repositórios desta organização que não tenham guia próprio. As regras de trabalho, o método e as decisões estão no repositório [docs](https://github.com/quorum-bench/docs): `CLAUDE.md`, `CONSTITUICAO.md` e o índice dos ADRs.

## O caminho de uma mudança

1. Uma fatia por PR, com a estação e o artefato no primeiro parágrafo.
2. O teste primeiro. Teste que falha significa código errado: nunca enfraqueça, pule ou desligue um teste para passar.
3. Antes do push, rode `npm run verificar` e cole a saída no PR. O que não rodou aparece como "não rodou", com o motivo.
4. Uma leitura que não escreveu o código revisa o diff.
5. A junção e a publicação são de uma pessoa.

## Mudança que atravessa repositórios

A ordem é `design-system` e `banco`, depois `pacotes`, depois os serviços, um PR por repositório, cada um com o link dos outros. O consumidor só abre o PR dele depois que o produtor publicou a versão. Ninguém aponta para um ramo de outro repositório (ADR-0034).

## Commits

Português do Brasil, no imperativo do que a mudança faz. Nenhum identificador de modelo de IA em commit, PR ou comentário de código.

## O que nunca entra

- Dado de pessoa em teste, semente, print ou log. Semente só com pessoas fictícias (`.example`, `.test`).
- Segredo. Chave ou senha é colada pela pessoa numa ferramenta `npm run <x>:configurar`; nunca em `.env` versionado, variável de build ou log.
- Versão flutuante de dependência.

## Onde mais olhar

- [SECURITY.md](SECURITY.md): como avisar de uma falha.
- [SUPPORT.md](SUPPORT.md): onde pedir ajuda.
- [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md): como a gente trabalha junto.
