---
description: Le type de données de capteur principal pour les capteurs de lumière ambiante est l’éclairage en lux (lumens par mètre carré). Les principes énoncés dans cette rubrique sont basés sur l’utilisation de valeurs en Lux comme entrée et la réaction à ces données dans un programme.
ms.assetid: 29855779-7c27-4cfe-b8af-b33bc86a1f62
title: Compréhension et interprétation des valeurs LX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8012f983eeac29cc07b18ac2d27918d2df6ed52
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233184"
---
# <a name="understanding-and-interpreting-lux-values"></a>Compréhension et interprétation des valeurs LX

Le type de données de capteur principal pour les capteurs de lumière ambiante est l’éclairage en lux (lumens par mètre carré). Les principes énoncés dans cette rubrique sont basés sur l’utilisation de valeurs en Lux comme entrée et la réaction à ces données dans un programme.

Les lectures en Lux sont directement proportionnelles à l’énergie par mètre carré absorbée par seconde. La perception humaine des niveaux de lumière n’est pas si simple. La perception humaine de la lumière est compliquée, car nos yeux évoluent constamment et d’autres processus biologiques affectent notre perception. Toutefois, nous pouvons considérer cette perception d’un point de vue simplifié en créant plusieurs plages d’intérêt avec des seuils supérieurs et inférieurs connus.

L’exemple de jeu de données suivant représente des seuils approximatifs pour les conditions d’éclairage courantes et l’étape d’éclairage correspondante. Ici, chaque étape d’éclairage représente une modification de l’environnement d’éclairage.

> [!Note]  
> Ce jeu de données est à titre d’illustration et peut ne pas être complètement précis pour tous les utilisateurs ou situations.

 



| Condition d’éclairage | De (Lux) | À (Lux) | Valeur moyenne (Lux) | Étape d’éclairage |
|--------------------|------------|----------|------------------|---------------|
| Noir tonal        | 0          | 10       | 5                | 1             |
| Très sombre          | 11         | 50       | 30               | 2             |
| Inportes sombres       | 51         | 200      | 125              | 3             |
| Dimensions de l’intérieur        | 201        | 400      | 300              | 4             |
| Inportes normales     | 401        | 1 000     | 700              | 5             |
| Portes lumineuses     | 1001       | 5 000     | 3000             | 6             |
| Dim Outdoors       | 5001       | 10 000   | 7500             | 7             |
| Cloud Outdoors    | 10 001     | 30,000   | 20 000           | 8             |
| Soleil direct    | 30 001     | 100 000  | 65 000           | 9             |



 

Si nous affichons ces données à l’aide des valeurs moyennes de ce tableau, nous voyons que la relation de l’étape Lux-à-éclairage n’est pas linéaire, comme indiqué dans le graphique suivant.

![graphique d’éclairage linéaire](images/luxtostep.png)

Toutefois, si vous affichez ces données à l’aide d’une échelle logarithmique sur l’axe des x, nous voyons qu’une relation à peu près linéaire émerge.

![graphique d’éclairage logarithmique](images/luxlogtostep.png)

### <a name="an-example-transform"></a>Exemple de transformation

Sur la base de l’exemple de jeu de données pour les capteurs de lumière ambiante précédemment fournis, vous pouvez obtenir l’équation suivante pour mapper les valeurs Lux à la perception humaine. Dans cet exemple, la plage de valeurs attendue est comprise entre 0 Lux et 1 million Lux.

![équation de valeur Lux](images/sensor-lux-equation.jpg)

Cette équation donne des valeurs qui varient à peu près de manière linéaire entre 0,0 et 1,0. Ce résultat indique comment l’éclairage perçu par l’homme a été modifié en fonction de l’exemple de jeu de données indiqué précédemment.

 

 



