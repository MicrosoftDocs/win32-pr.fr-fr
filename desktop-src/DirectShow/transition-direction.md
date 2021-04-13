---
description: Sens de la transition
ms.assetid: d18525de-bb75-4c5e-b387-cfec7ba03df7
title: Sens de la transition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01d43ec4258d2f23c8b8961e3e1b8fd3d554b057
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104552014"
---
# <a name="transition-direction"></a>Sens de la transition

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Une transition passe de l’entrée A à l’entrée B et de l’heure t ₀ à t ₁. Par conséquent, la *direction* d’une transition peut signifier l’un des deux éléments suivants :

-   Mappage des couches de la chronologie aux entrées.
-   Progression dans le temps.

La première est la *direction d’entrée*, tandis que la seconde est la *direction de progression*. Vous pouvez contrôler les deux directions.

-   Direction d’entrée : par défaut, une transition passe de l’composite des couches de faible priorité à la couche qui contient la transition. Pour inverser cette direction, appelez la méthode [**IAMTimelineTrans :: SetSwapInputs**](iamtimelinetrans-setswapinputs.md) .
-   Direction de la progression : la plupart des transitions prennent en charge une propriété de **progression** standard, qui spécifie le pourcentage de la transition qui est reflété dans la sortie à un moment donné. Par défaut, la valeur de la propriété **Progress** passe de 0,0 à 1,0 pendant la durée de la transition. Pour inverser la progression, affectez à la propriété **Progress** la valeur allant de 1,0 à 0,0.

Le diagramme suivant illustre la différence entre la direction d’entrée et la direction de progression. Il présente quatre variations sur une transition de [réinitialisation SMPTE](smpte-wipe-transition.md) standard.

![instructions de réinitialisation](images/wipedirections.png)

La transition réside sur la piste 1. Par défaut, la réinitialisation va de gauche à droite et de Track 0 à Track 1. Si vous échangez des entrées, la réinitialisation passe de Track 1 pour suivre 0, mais toujours de gauche à droite. L’inversion de la progression fait passer la transition de droite à gauche. Vous pouvez combiner les deux, comme indiqué à l’extrême gauche.

Pour plus d’informations sur l’affichage DES transitions par, consultez [le modèle de chronologie](the-timeline-model.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des effets et des transitions](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



