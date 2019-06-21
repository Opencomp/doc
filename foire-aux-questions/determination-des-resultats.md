---
description: >-
  Dans cette page, apprenez comment Opencomp détermine le positionnement d'un
  élève pour un domaine particulier.
---

# Détermination des résultats

## Comment Opencomp détermine le positionnement de l'élève pour chaque domaine du LSU ?

Opencomp détermine automatiquement le positionnement de chaque élève en fonction des différents résultats que vous avez saisis pour ses différentes évaluations.

Pour chaque évaluation, vous associez des éléments de programmes évalués qui sont eux même "attachés" au domaine correspondant du LSU \(Livret Scolaire Unique\).

Pour chaque domaine du LSU \(Livret Scolaire Unique\), Opencomp dénombre chaque résultat saisi et détermine le positionnement en fonction de la majorité obtenue. Par exemple, si un élève obtient une majorité de **Atteint \(A\)** pour un domaine, le domaine sera positionné à **Atteint \(A\)**. Et ainsi de suite.

La table de décision ci-dessous vous permet de déterminer le résultat arrêté automatiquement par Opencomp \(dans la 5ème colonne\) en fonction des éventuelles égalités.

* Les 4 premières lignes du tableau, représentent le cas le plus fréquent : la somme des différents résultats saisis permet de déterminer une majorité d'un même résultat, c'est alors ce résultat qui est arrêté.
* Les 4 lignes suivantes, représentent le cas où la somme des résultats abouti à une égalité entre 2 positionnement. Dans le cas où l'égalité est entre le positionnement **Dépassé \(DE\)** et **Atteint \(A\)**, le résultat arrêté est **Dépassé \(DE\)**. Dans tous les autres cas, le résultat arrêté est **Partiellement Atteint \(PA\)**.
* Les 4 lignes suivantes, représentent le cas peu probable où la somme des résultats abouti à une égalité entre 3 positionnements. Dans le cas où l'égalité est entre le positionnement **Dépassé \(DE\)**, **Atteint \(A\)** et **Partiellement Atteint \(PA\)**, le résultat arrêté est **Atteint \(A\)**. Dans tous les autres cas, le résultat arrêté est **Partiellement Atteint \(PA\)**.
* La dernière ligne de la table de décisions, représente le cas extrêmement improbable où la somme des résultats abouti à une égalité entre les 4 positionnements. Dans ce cas, le résultat arrêté est **Partiellement Atteint \(PA\)**.

| **DE** | **A** | **PA** | **NA** | **Résultat** |
| :--- | :--- | :--- | :--- | :--- |
| 1 | 0 | 0 | 0 | DE |
| 0 | 1 | 0 | 0 | A |
| 0 | 0 | 1 | 0 | PA |
| 0 | 0 | 0 | 1 | NA |
| 1 | 1 | 0 | 0 | DE |
| 0 | 0 | 1 | 1 | PA |
| 0 | 1 | 1 | 0 | PA |
| 1 | 0 | 0 | 1 | PA |
| 1 | 1 | 1 | 0 | A |
| 0 | 1 | 1 | 1 | PA |
| 1 | 1 | 0 | 1 | PA |
| 1 | 0 | 1 | 1 | PA |
| 1 | 1 | 1 | 1 | PA |

