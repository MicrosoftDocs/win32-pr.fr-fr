---
description: Courbes de paramètres
ms.assetid: c073e7d0-c119-4c36-a5b2-b31dd6326ac8
title: Courbes de paramètres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3c482112c8bd76217f5cbdabdf3cda13b09c3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109511"
---
# <a name="parameter-curves"></a>Courbes de paramètres

Les paramètres de média peuvent suivre une courbe dans le temps. Chaque courbe est décrite par une formule mathématique et deux points de terminaison. Chaque point de terminaison est défini par une heure de référence et la valeur de la courbe à ce moment-là. La formule est utilisée pour calculer les valeurs intermédiaires entre les points et détermine la forme de la courbe. Les courbes possibles sont les suivantes :

-   Y
-   Linéaire
-   Carré
-   Carré inverse
-   Sinus

« Jump » signifie passer directement à la valeur de fin. Les autres courbes sont présentées dans le diagramme suivant.

![courbes de paramètres](images/param-curves01.png)

Mathématiquement, les courbes fonctionnent comme suit. Supposons qu’une courbe commence à l’heure *t*₀ avec la valeur *v*₀ et se termine à l’heure *t*₁ par une valeur *v*₁. Les deux points qui définissent la courbe sont (*t*₀, *v*₀) et (*t*₁, *v*₁).

-   Laissez Δ *t* la durée totale de la courbe, *t*₁ –*t*₀.
-   Laissez Δ *v* correspondre à l’intervalle entre les valeurs de début et de fin, *v*₁ –*v*₀.
-   À tout moment *t* comme t *₀ <*= *t*  <=  *t*₁, laissez Δ *t*' = *t*-*t*₀.

![calcul des paramètres](images/param-curves02.png)

La valeur du paramètre à l’heure *t* est la suivante :

*v* = f (Δ *t*'/Δ *t* ) \* Δ *v*  +  *v*₀

où f (x) est une fonction déterminée par le type de courbe :

-   Linéaire : y = x
-   Square : y = x ^ 2
-   Carré inverse : y = sqrt (x)
-   Sinus : y = \[ Sin (πx – π/2) + 1 \] /2

Notez que Δ *t*' < Δ *t*, donc le terme Δ *t*'/Δ *t* est compris entre 0 et 1. Par conséquent, f (x) est également compris entre 0 et 1, et *v* se situe toujours entre *v*₀ et *v*₁. C’est vrai que *v*₀ < *v*₁ ou vice versa. En d’autres termes, la courbe est délimitée par le rectangle (*t*₀, *v*₀, *t*₁, *v*₁).

Pour la courbe sinusoïdale, la valeur de (πx – π/2) est comprise entre – π/2 et π/2, ce qui signifie que sin (πx – π/2) est compris entre-1 et 1. Le résultat est ensuite normalisé afin que f (x) se trouve dans la plage (0 – 1).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Paramètres de média](media-parameters.md)
</dt> </dl>

 

 



