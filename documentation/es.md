<!-- ELUCENIA technical documentation · indice-de-baux-revisado · es · no clinical/professional/rights approval -->

# Índice de Baux revisado

[condiciones, fuentes y permisos](https://elucenia.org/es/herramientas/indice-de-baux-revisado)

## Cómo usar

Utilice la herramienta en el portal o abra index.html mediante un servidor HTTP local. Seleccione el idioma, complete los campos y calcule.

## Entradas y unidades

### Edad

`idade`

años · intervalo: 0–110

### Superficie corporal quemada

`scq`

% · intervalo: 0–100

### ¿Lesión por inhalación?

`inalacao`

- `0` — No
- `1` — Sí

## Edición del método

Baux revisado/Osler 2010: edad+superficie quemada+17 lesión inhalatoria; logística original

## Fórmula documentada

Baux revisado = edad (años) + superficie quemada (%) + 17 × lesión inhalatoria (1=sí, 0=no).

En Osler (39888 quemados del registro estadounidense), edad y superficie quemada pesaron casi igual; la lesión inhalatoria equivalía a 17 años o 17% de superficie. La probabilidad de muerte es la transformación logística de la puntuación.

## Límites y población

El Baux revisado suma edad, porcentaje de superficie quemada y 17 para lesión por inhalación. El total bruto no es un porcentaje de mortalidad: la probabilidad requiere la transformación logística de la versión. El modelo simplificado tuvo un rendimiento inferior al modelo más complejo del artículo y exige interpretación en la población clínica adecuada.

## Referencias

- [Osler T, Glance LG, Hosmer DW. Simplified estimates of the probability of death after burn injuries: extending and updating the Baux score. J Trauma, 2010.](https://doi.org/10.1097/TA.0b013e3181c453b3)

- [Dokter J et al. External validation of the revised Baux score for the prediction of mortality in patients with acute burn injury. J Trauma Acute Care Surg, 2014.](https://doi.org/10.1097/TA.0000000000000124)

## Reproducir las pruebas técnicas

Ejecute node test.cjs en el directorio raíz de este repositorio para repetir los casos sintéticos registrados. Se conservan las entradas, los resultados esperados y las tolerancias originales. Las pruebas técnicas no constituyen validación clínica.

```sh
node test.cjs
```

tool.json contiene las fuentes, la edición y el alcance de la revisión. examples.json conserva las entradas y los resultados esperados de los casos sintéticos; results.json registra los resultados obtenidos.

[Ficha y referencias](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referencia](../examples.json) · [results.json](../results.json)

## Revisión y condiciones de uso

No se ha realizado una revisión clínica independiente.

Esta interfaz es una traducción de elaboración propia, no una edición oficial o certificada. No se han realizado la revisión clínica independiente, la revisión lingüística profesional ni la autorización de derechos de los instrumentos.

Resultado de la fórmula o clasificación. La interpretación, la conducta y la aplicabilidad dependen de la evaluación profesional y de la fuente seleccionada.

## Licencia y atribución

Apache-2.0 se aplica únicamente al código de ELUCENIA. Los derechos de los instrumentos, publicaciones, traducciones y datos permanecen en manos de sus respectivos titulares. Conserve LICENSE y NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
