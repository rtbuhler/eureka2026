# Plano de medição: Mapa Eureka 2026

**Decisão que os dados informam:** o site gera visitas qualificadas ao vestibular 2027? Quais áreas e botões funcionam?

## Convenção de UTM (já nos links para maua.br)
`utm_source=eureka2026` · `utm_medium=mapa` · `utm_campaign=vestibular2027` · `utm_content=<local>`
Valores de `utm_content`: `topo`, `rodape`, `artes-aplicadas`, `computacao`, `engenharia`, `negocios`.
Os cliques aparecem no analytics do maua.br (origem/campanha).

## Eventos no dataLayer (para GTM/GA4; nomes no formato objeto_ação)
| Evento | Quando | Parâmetros |
|---|---|---|
| `cta_click` | clique em link para maua.br / eureka.maua.br | `destino`, `local` |
| `view_changed` | troca de visão (mapa, áreas, lista em texto) | `visao` |
| `stand_selected` | seleção de um estande | `estande`, `visao` |
| `search_used` | busca digitada (após 0,9 s) | `tamanho_termo`, `resultados` |

Sem texto digitado nem dados pessoais nos eventos.

## Para ativar
1. Marketing cria o contêiner GTM (ou propriedade GA4) e informa o ID.
2. Inserir o snippet do GTM em `index.html` e configurar tags para os eventos acima.
3. Respeitar a política de cookies/LGPD do IMT antes de ativar.
4. Validar no modo de depuração (Tag Assistant) e conferir `cta_click` com UTM no maua.br.

## Indicadores
- Cliques em `cta_click` por local e por 1.000 visitas.
- Visões mais usadas e buscas sem resultado (`resultados = 0`).
