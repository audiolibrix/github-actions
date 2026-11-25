# GitHub Actions

Sdílené composite actions pro GitHub workflow. Repo je veřejné, aby šly
volat z jakéhokoli repozitáře. Nepatří sem nic tajného ani specifického
pro konkrétní projekt — webhooky, tokeny a podobné hodnoty přicházejí jako
inputy ze secretů volajícího repa.

| action | k čemu |
|---|---|
| [`notify-slack`](notify-slack/action.yml) | začátek a výsledek běhu workflow do Slacku |

Vedle nich je tu znovupoužitelné workflow, které se volá celým jobem
(`jobs.<id>.uses`). Jak ho zapojit, je v komentáři na jeho začátku.

| workflow | k čemu |
|---|---|
| [`release`](.github/workflows/release.yml) | release přes release-it a deploy na novém tagu, ručně nebo automaticky jen s aktualizacemi od bota |

## Verze

Volá se přes hlavní tag, třeba `@v1`. Zpětně kompatibilní změna posune `v1`
na nový commit, rozbíjející dostane `v2`.
