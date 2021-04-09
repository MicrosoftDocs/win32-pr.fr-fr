---
description: Transitions
ms.assetid: 432db77f-c3fa-4234-bbce-cf17d8878b99
title: Transitions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01fef1cd888293ad83ab1ba9f05ab4bb83ddafa9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868262"
---
# <a name="transitions"></a>Transitions

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Une transition est un moyen de Segue d’une piste vidéo à une autre, à l’aide d’un effet visuel tel qu’un fondu ou une réinitialisation. L’illustration suivante montre une chronologie avec une transition :

![chronologie avec transition](images/timeline3.png)

L’objet de transition est sur Track 1 et représente une transition de Track 0 à Track 1. Au début de la transition, la vidéo rendue est entièrement à partir de Track 0 (source A). À la fin, la vidéo provient entièrement de Track 1 (source C). Dans between, la sortie passe de la source A à la source C. Par exemple, dans une transition de fondu, une source apparaît progressivement en fondu. La sortie finale est schématisés dans la partie inférieure de l’illustration.

Les transitions ne peuvent pas se chevaucher dans le temps d’une même piste, mais vous pouvez créer des transitions qui se chevauchent à l’aide de l’objet composition, comme décrit dans [composition et structuration en couches](composition-and-layering.md).

Une transition a une direction. Par défaut, il démarre à partir de la piste de priorité la plus basse (source A, dans l’exemple précédent) et se termine à la piste de priorité la plus élevée (source C). Entre-présent, la vidéo est un mélange des deux sources. Toutefois, vous pouvez spécifier le comportement opposé, comme indiqué dans l’illustration suivante :

![nTrack avec deux transitions](images/fade.png)

Ici, la première transition disparaît de la piste 0 atténue la piste 1, qui est le comportement par défaut. La deuxième transition disparaît de la piste 1 vers la piste 0. Notez que les deux transitions se trouvent sur Track 1.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main avec les services d’édition DirectShow](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[Transitions et effets](transitions-and-effects.md)
</dt> <dt>

[Utilisation des effets et des transitions](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



