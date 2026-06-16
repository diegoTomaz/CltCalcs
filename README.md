# SimulaCLT

Calculadoras gratuitas para a vida financeira do brasileiro — salário líquido, INSS, férias, rescisão, juros compostos e financiamento. Atualizadas para 2026.

Online em **[simulaclt.com.br](https://simulaclt.com.br)**.

## Calculadoras

| Página | URL | O que faz |
|---|---|---|
| `index.html` | `/` | Página inicial com a listagem das ferramentas |
| `calculadora-salario-liquido.html` | `/calculadora-salario-liquido` | Salário líquido com descontos de INSS e IRRF 2026 (isenção até R$ 5.000 — Lei 15.270/2025) |
| `calculadora-inss.html` | `/calculadora-inss` | Desconto de INSS pela tabela progressiva 2026 (7,5% a 14%), faixa por faixa |
| `calculadora-ferias.html` | `/calculadora-ferias` | Valor líquido das férias com 1/3 constitucional e venda de 1/3 (abono pecuniário) |
| `calculadora-rescisao.html` | `/calculadora-rescisao` | Verbas rescisórias por motivo de desligamento (saldo, aviso, 13º, férias, multa do FGTS) |
| `calculadora-juros-compostos.html` | `/calculadora-juros-compostos` | Crescimento do dinheiro com aportes mensais e juros compostos |
| `calculadora-financiamento.html` | `/calculadora-financiamento` | Parcela, juros totais e tabela de amortização pela Tabela Price |

## Como funciona

- HTML/CSS/JS puros — sem build, sem dependências, sem framework.
- Todos os cálculos rodam no navegador. Nada é enviado para servidores.
- Sem cadastro, sem tracker, sem cookies.
- Cada arquivo é independente e pode ser aberto direto no navegador (`file://`) para testar.

## Cálculo — referências oficiais

- **INSS 2026**: Portaria do MPS — tabela progressiva com 4 faixas (7,5% / 9% / 12% / 14%) e teto de contribuição.
- **IRRF 2026**: Lei 15.270/2025 — isenção integral até R$ 5.000, redução gradual entre R$ 5.000,01 e R$ 7.350.
- **Dedução por dependente**: R$ 189,59 / mês (valor mantido).
- **Desconto simplificado**: R$ 607,20 / mês (alternativa às deduções legais — calculadoras usam a opção mais vantajosa).
- Cálculos em centavos inteiros para evitar erro de ponto flutuante.

> Atualizar anualmente junto com as novas tabelas — as constantes ficam no `<script>` no topo de cada arquivo.

## Subir o site

Qualquer hospedagem estática serve (GitHub Pages, Cloudflare Pages, Netlify, Vercel, S3, Nginx). Basta:

1. Subir os 7 arquivos `.html` para a raiz.
2. Apontar o domínio `simulaclt.com.br` para o host.
3. Configurar o servidor para servir URLs sem extensão (`/calculadora-inss` → `calculadora-inss.html`), seja com regras de rewrite ou com a opção "clean URLs" do provedor.

## SEO

- Cada página tem `title`, `description`, `canonical` e Open Graph próprios.
- A `index.html` traz dois blocos de JSON-LD (`WebSite` + `ItemList`) para o Google indexar as 6 ferramentas como uma coleção.
- Conteúdo em texto + FAQ no final de cada página para rich results e long-tail.

## Estrutura

```
.
├── index.html
├── calculadora-salario-liquido.html
├── calculadora-inss.html
├── calculadora-ferias.html
├── calculadora-rescisao.html
├── calculadora-juros-compostos.html
└── calculadora-financiamento.html
```

## Licença

Uso pessoal e educacional. Os resultados são estimativas e não substituem o holerite oficial nem orientação contábil.
