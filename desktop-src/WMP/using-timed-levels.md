---
title: Utilisation de niveaux chronométrés
description: Utilisation de niveaux chronométrés
ms.assetid: 4a253521-3036-488a-98bc-62596b538f68
keywords:
- visualisations, événements chronométrés
- visualisations personnalisées, événements chronométrés
- visualisations, tableau Frequency
- visualisations personnalisées, tableau de fréquence
- visualisations, tableau de forme d’onde
- visualisations personnalisées, tableau de forme d’onde
- visualisations, variable d’État
- visualisations personnalisées, variable d’État
- visualisations, variable timeStamp
- visualisations personnalisées, variable timeStamp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2d9a23818d57305b3b205ea2e17b6dda2884e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029235"
---
# <a name="using-timed-levels"></a>Utilisation de niveaux chronométrés

La structure **TimedLevel** est composée de tableaux 2 2 dimensionnels, d’une valeur d’État et d’une valeur d’horodatage.

## <a name="frequency-array"></a>Tableau Frequency

Le tableau Frequency est un tableau à deux dimensions. La première dimension de chaque tableau correspond au canal audio stéréo (à gauche ou à droite), tandis que la seconde correspond aux niveaux de fréquence (en octets) de l’instantané, où le spectre audio est divisé en zones de 1024.

Vous pouvez récupérer les données de tableau de fréquences fournies par le lecteur Windows Media de la manière suivante :


```C++
TimedLevel *pLevels;
int snapshot = pLevels->frequency[0][0];
```



La valeur de l’instantané est pour le canal gauche et contient la valeur de la partie la plus basse du spectre de fréquences. Par exemple, si l’instantané a une valeur élevée, il indique que la partie 1024th la plus faible du spectre de fréquences est riche en fréquence. La valeur zéro indique qu’il n’y A aucune valeur de fréquence faible dans cette partie du spectre pour le canal de gauche. Si vous avez un signal Monophonic, seule la première dimension a des valeurs valides.

Si le signal n’est pas stéréo, le deuxième tableau contiendra une copie du signal mono. Autrement dit, \[ la fréquence 0 \] \[ *n* \] et \[ la fréquence 1 \] \[ *n* \] contiennent les mêmes données, où *n* est l’index d’une cellule particulière.

## <a name="waveform-array"></a>Tableau de forme d’onde

Le tableau Waveform est également un tableau à deux dimensions. La première dimension du tableau correspond au canal (à gauche ou à droite), tandis que la seconde correspond aux niveaux d’alimentation (en octets) de l’instantané, où la puissance audio est divisée en segments de temps contigus de 1024.

Vous pouvez récupérer les données du tableau de forme d’onde à partir du lecteur Windows Media de la manière suivante :


```C++
TimedLevel *pLevels;
int snapshot = pLevels->waveform[0][0];

```



La valeur de l’instantané est pour le canal gauche et contient la première valeur de l’instantané quantifié des valeurs d’alimentation. Lorsqu’un instantané est pris, il se compose de 1024 petites mesures incrémentielles de la puissance audio. La valeur la plus basse du tableau est générée par la première mesure incrémentielle de la puissance audio. Notez que les valeurs de l’alimentation sont mesurées de-128 à + 127, mais que les valeurs du tableau sont comprises entre 0 et 255. Si vous avez une vague Monophonic, seule la première dimension aura des valeurs valides.

Si le signal n’est pas stéréo, le deuxième tableau contiendra une copie du signal mono. Autrement dit, la forme d’onde \[ 0 \] \[ *n* \] et la forme d’onde \[ 1 \] \[ *n* \] contiennent les mêmes données, où *n* est l’index d’une cellule particulière.

## <a name="state"></a>State

La variable d’État reflète l’état de lecture audio du lecteur Windows Media. Les valeurs d’énumération PlayerState sont


```C++
    stop_state              = 0,    // audio is currently stopped
    pause_state             = 1,    // audio is currently paused
    play_state              = 2     // audio is currently playing

```



Vous pouvez utiliser cette variable pour effectuer des actions différentes en fonction de l’état de lecture audio. Par exemple, vous pouvez lire un type de visualisation lorsque l’audio est lu et un autre quand il est arrêté.

## <a name="time-stamp"></a>Horodatage

La variable timeStamp reflète l’heure actuelle à laquelle l’instantané est pris. Cette valeur peut être utilisée pour mesurer la fréquence à laquelle les instantanés sont pris.

Vous pouvez utiliser cette variable pour l’heure de vos animations. Si les instantanés sont trop fréquents, vous pouvez faire en sorte que votre image s’affiche de la manière appropriée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation du rendu**](implementing-render.md)
</dt> </dl>

 

 




