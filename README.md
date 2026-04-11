# Heineken Margem PDV

Calculadora de margem para vendedores Heineken de distribuidora de bebidas. Ferramenta de apoio à venda que demonstra ao PDV (ponto de venda) o ganho financeiro ao optar por produtos Heineken/Amstel em vez de Original/Antártica.

**URL**: https://ladsistemas.github.io/heineken-margem-pdv/

## Contexto de negócio

Vendedores de uma distribuidora usam esta ferramenta no celular durante visitas a bares e restaurantes. O objetivo é mostrar de forma visual e objetiva que a margem de lucro por caixa é maior com Heineken e Amstel, convencendo o PDV a trocar ou aumentar o mix.

### Comparações

| Premium (Heineken) | Mainstream (concorrente) |
|---|---|
| Heineken | Original |
| Amstel | Antártica |

## Como funciona

1. Vendedor preenche **custo da caixa (24un)** de cada produto — o sistema calcula o custo unitário automaticamente
2. Preenche o **valor de venda unitário** praticado pelo PDV
3. Informa a **quantidade de caixas vendidas por mês**
4. O sistema mostra:
   - Lucro por caixa de cada produto
   - Barras comparativas visuais
   - Diferença de lucro por caixa (destaque verde)
   - Lucro total no período e quanto o PDV deixa de ganhar

## Stack

- **HTML + CSS + JS vanilla** — arquivo único, zero dependências
- **Mobile-first** — otimizado para uso em celular durante visita ao PDV
- **GitHub Pages** — deploy automático via Actions a cada push na `main`
- Sem backend, sem autenticação, sem banco de dados

## Estrutura

```
index.html          # App completo (single file)
.github/workflows/
  deploy.yml        # GitHub Actions → GitHub Pages
```

## Deploy

Push na branch `main` dispara o workflow `deploy.yml` que publica automaticamente no GitHub Pages. Leva ~20s.

## Possíveis evoluções

- Adicionar mais pares de comparação (ex: Heineken Silver x Brahma)
- Compartilhar resultado via WhatsApp (screenshot ou link com params na URL)
- PWA com ícone na home do celular e funcionamento offline
- Salvar últimos valores preenchidos (localStorage)
- Logo da distribuidora no header
