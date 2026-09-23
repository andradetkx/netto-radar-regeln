# Netto-Radar — regras

Este repositório tem **um arquivo só**, `regras.json`. A extensão Netto-Radar
o baixa a cada 12 horas (e ao abrir o navegador) de:

    https://raw.githubusercontent.com/andradetkx/netto-radar-regeln/main/regras.json

Serve para corrigir a extensão **sem publicar versão nova** na Chrome Web
Store. Mudou aqui, deu `git push`: em até 12 horas vale para todo mundo. Para
testar na hora no seu Chrome: `chrome://extensions` → ↻ na extensão (ela
busca as regras ao ser recarregada).

**Só dados, nunca código.** A loja proíbe executar código baixado. A extensão
aceita apenas listas de palavras, números e liga/desliga, e **descarta em
silêncio** tudo o que não se encaixa. JSON quebrado = ela usa as regras de
fábrica, não quebra.

## Campos

| Campo | Para quê | Exemplo |
|---|---|---|
| `formato` | Sempre `1`. Outro valor = arquivo ignorado. | `1` |
| `atualizado` | Data da última mudança (`AAAA-MM-DD`). Aparece nos ajustes e nos relatórios de problema. | `"2026-10-02"` |
| `desligado` | `true` desliga a extensão inteira. Freio de emergência: ela passou a errar em massa. | `false` |
| `sites.stepstone` / `.indeed` / `.linkedin` | `false` desliga um site só (ele mudou e a correção ainda não saiu). **Não dá para ligar site novo por aqui** — isso exige permissão, logo versão nova. | `"linkedin": false` |
| `leitor.naoSalario` | Palavras que, num texto com euro, dizem que o valor NÃO é salário (além das de fábrica: Bonus, Zuschuss, Jobticket…). | `["Umzugspauschale"]` |
| `leitor.salario` | Palavras que confirmam que é salário (além de Gehalt, Lohn, Vergütung…). | `["Grundvergütung"]` |
| `leitor.periodos.jahr` etc. | Sinônimos novos de período. | `"jahr": ["jährl."]` |
| `leitor.mensalMin` / `mensalMax` | Faixa plausível em € brutos por mês (100–2.000 / 10.000–100.000). | `300` / `40000` |
| `leitor.faixaMaxRazao` | Faixa mais larga que isto (máx ÷ mín) é chute e é ignorada (1,5–10). | `3` |
| `lugares.adicionar` | Lugar de fora da Alemanha que faltou: `"Nome": "CH"`, `"AT"`, `"LI"` ou `"X"`. | `{"Pfäffikon": "CH"}` |
| `lugares.remover` | Lugar marcado como estrangeiro por engano (existe na Alemanha). | `["Baden"]` |
| `contato` | E-mail que recebe o "Problem melden". `null` = o botão some. | `"nettoradar@…"` |

Palavras: 2 a 40 caracteres, só letras, dígitos, espaço e `. / - ' €`. Até
100 por lista. Maiúscula e minúscula tanto faz.
