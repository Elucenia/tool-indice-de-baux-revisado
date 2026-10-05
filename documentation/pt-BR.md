<!-- ELUCENIA technical documentation · indice-de-baux-revisado · pt-BR · no clinical/professional/rights approval -->

# Índice de Baux revisado

[condições, fontes e permissões](https://elucenia.org/pt-br/ferramentas/indice-de-baux-revisado)

## Como usar

Use a ferramenta no portal ou abra index.html em um servidor HTTP local. Selecione o idioma, preencha os campos e calcule.

## Entradas e unidades

### Idade

`idade`

anos · intervalo: 0–110

### Superfície corporal queimada

`scq`

% · intervalo: 0–100

### Lesão inalatória?

`inalacao`

- `0` — Não
- `1` — Sim

## Edição do método

Revised Baux/Osler 2010:idade+SCQ+17 lesãoinalatória; modelo logístico original

## Fórmula documentada

Baux revisado = idade (anos) + SCQ (%) + 17 × lesão inalatória (1 = sim, 0 = não).

No modelo de Osler (39.888 queimados do registro norte-americano), idade e SCQ pesaram quase igual, e a lesão inalatória equivaleu a 17 anos ou 17% de SCQ. A probabilidade de óbito vem da transformação logística do escore.

## Limites e população

O Baux revisado soma idade, porcentagem de área queimada e 17 para lesão inalatória. O total bruto não é porcentagem de mortalidade: a probabilidade requer a transformação logística da versão. O modelo simplificado teve desempenho inferior ao modelo mais complexo no artigo e exige interpretação na população clínica adequada.

## Referências

- [Osler T, Glance LG, Hosmer DW. Simplified estimates of the probability of death after burn injuries: extending and updating the Baux score. J Trauma, 2010.](https://doi.org/10.1097/TA.0b013e3181c453b3)

- [Dokter J et al. External validation of the revised Baux score for the prediction of mortality in patients with acute burn injury. J Trauma Acute Care Surg, 2014.](https://doi.org/10.1097/TA.0000000000000124)

## Reproduzir os testes técnicos

Execute node test.cjs na pasta raiz deste repositório para repetir os casos sintéticos registrados. As entradas, expectativas e tolerâncias originais são preservadas. Testes técnicos não constituem validação clínica.

```sh
node test.cjs
```

tool.json contém fontes, edição e escopo de revisão. examples.json conserva as entradas e expectativas sintéticas; results.json registra os resultados obtidos.

[Ficha e referências](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referência](../examples.json) · [results.json](../results.json)

## Revisão e condições de uso

Revisão clínica independente não realizada.

Esta interface é uma tradução autoral, não uma edição oficial ou certificada. Revisão clínica independente, revisão linguística profissional e autorização de direitos de instrumentos não foram realizadas.

Resultado da fórmula ou classificação. Interpretação, conduta e aplicabilidade dependem da avaliação profissional e da fonte selecionada.

## Licença e atribuição

Apache-2.0 aplica-se somente ao código da ELUCENIA. Os instrumentos, publicações, traduções e dados mantêm os direitos dos respectivos titulares. Preserve LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
