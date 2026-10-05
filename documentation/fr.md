<!-- ELUCENIA technical documentation · indice-de-baux-revisado · fr · no clinical/professional/rights approval -->

# Score de Baux révisé

[conditions, sources et autorisations](https://elucenia.org/fr/outils/indice-de-baux-revisado)

## Mode d’emploi

Utilisez l’outil sur le portail ou ouvrez index.html via un serveur HTTP local. Sélectionnez la langue, remplissez les champs et lancez le calcul.

## Données d’entrée et unités

### Âge

`idade`

ans · intervalle: 0–110

### Surface corporelle brûlée

`scq`

% · intervalle: 0–100

### Lésion d’inhalation ?

`inalacao`

- `0` — Non
- `1` — Oui

## Édition de la méthode

Baux révisé/Osler 2010 : âge+surface brûlée+17 inhalation ; modèle logistique original

## Formule documentée

Baux révisé = âge (ans) + surface brûlée (%) + 17 × lésion d’inhalation (1=oui, 0=non).

Dans Osler (39888 brûlés du registre américain), âge et surface avaient un poids presque égal ; l’inhalation équivalait à 17 ans ou 17% de surface. La probabilité de décès est la transformation logistique du score.

## Limites et population

Le Baux révisé additionne l’âge, le pourcentage de surface brûlée et 17 pour une lésion d’inhalation. Le total brut n’est pas un pourcentage de mortalité : la probabilité nécessite la transformation logistique de la version. Le modèle simplifié avait une performance moindre que le modèle plus complexe dans l’article et doit être interprété dans une population clinique appropriée.

## Références

- [Osler T, Glance LG, Hosmer DW. Simplified estimates of the probability of death after burn injuries: extending and updating the Baux score. J Trauma, 2010.](https://doi.org/10.1097/TA.0b013e3181c453b3)

- [Dokter J et al. External validation of the revised Baux score for the prediction of mortality in patients with acute burn injury. J Trauma Acute Care Surg, 2014.](https://doi.org/10.1097/TA.0000000000000124)

## Reproduire les tests techniques

Exécutez node test.cjs dans le répertoire racine de ce dépôt pour reproduire les cas synthétiques enregistrés. Les données d’entrée, les résultats attendus et les tolérances d’origine sont conservés. Les tests techniques ne constituent pas une validation clinique.

```sh
node test.cjs
```

tool.json contient les sources, l’édition et le périmètre de la revue. examples.json conserve les données d’entrée et les résultats attendus des cas synthétiques ; results.json consigne les résultats obtenus.

[Fiche et références](../tool.json) · [Code JavaScript](../calculator.js) · [Cas de référence](../examples.json) · [results.json](../results.json)

## Revue et conditions d’utilisation

Aucune révision clinique indépendante n’a été effectuée.

Cette interface est une traduction réalisée par nos soins, et non une édition officielle ou certifiée. La revue clinique indépendante, la révision linguistique professionnelle et l’autorisation des droits sur les instruments n’ont pas été réalisées.

Résultat de la formule ou de la classification. L’interprétation, la conduite et l’applicabilité dépendent de l’évaluation professionnelle et de la source sélectionnée.

## Licence et attribution

Apache-2.0 s’applique uniquement au code d’ELUCENIA. Les droits sur les instruments, publications, traductions et données restent ceux de leurs titulaires respectifs. Conservez LICENSE et NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
