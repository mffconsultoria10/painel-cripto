# Projeto Cripto

Painel pessoal de acompanhamento das carteiras cripto, com posições Aave V3, pools de liquidez Uniswap e um simulador de patrimônio.

**Publicado em:** https://mffconsultoria10.github.io/painel-cripto/

## Estrutura

- `index.html` — painel principal (saldo consolidado, posições Aave, exposição por ativo)
- `simulador.html` — simulador de patrimônio (cenários de preço BTC/ETH/câmbio)
- `pools.html` — controle de pools de liquidez na Uniswap V3

## Carteiras monitoradas

- Carteira 1: `0x2af9997fc77e50a3cde92b6452ee2faa0ddf2a47`
- Carteira 2: `0x68f0271fd7d9813f951419a1108fc1c9c0ba2072`

## Dados ao vivo

Quando hospedado fora do sandbox de Artifacts do Claude (por exemplo, no GitHub Pages), as páginas leem direto da blockchain, sem custo e sem conta:

- **Aave V3**: Health Factor, fornecido e emprestado (Polygon, Arbitrum, Base)
- **Saldo em carteira**: cbBTC, WBTC, ETH nativo, WETH, POL, SOL, UNI, HYPE
- **Pools Uniswap V3**: detecção de posições ativas, faixa de preço e proporção

Ficam apenas no snapshot manual (poeira sem endereço mapeado, valor irrelevante): MM.Finance, Merkl, MON, WGC.

## Como atualizar o site publicado

1. Peça ao Claude os arquivos atualizados (ou peça para ele regenerar este projeto)
2. No GitHub, vá no repositório `painel-cripto` → **Add file → Upload files**
3. Arraste os arquivos atualizados (substituem os antigos) → **Commit changes**
4. O GitHub Pages republica automaticamente em ~1 minuto

## Impermanent loss / rentabilidade de pools

Nas pools detectadas automaticamente pela Uniswap, clique no ícone de lápis no card para adicionar valor investido, preço de entrada e data de abertura — isso libera o cálculo de impermanent loss e rentabilidade real.
