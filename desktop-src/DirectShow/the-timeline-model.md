---
description: Modèle de chronologie
ms.assetid: 53e782a2-0fab-46b4-b029-20017d9905bd
title: Modèle de chronologie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e5eeb60dce31fa466a518476bb3da341a3d2fda4fdeaa47ca58a89a904dded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903807"
---
# <a name="the-timeline-model"></a>Modèle de chronologie

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

une *chronologie* est un objet que [DirectShow Services de modification](directshow-editing-services.md) (DES) utilise pour représenter un projet de montage vidéo. Un projet d’édition commence sous la forme d’une collection d’éléments sources, issus de fichiers vidéo, de fichiers audio ou de fichiers image toujours. Une séquence linéaire d’éléments forme une *piste*. dans DirectShow les Services d’édition, l’audio et la vidéo sont placés dans des pistes distinctes.

Les pistes peuvent également être superposées. Plusieurs pistes audio sont mélangées et peuvent inclure des effets audio, tels qu’un fondu ou une réverbération. Plusieurs pistes vidéo sont utilisées pour créer des transitions. Par exemple, vous pouvez créer une réinitialisation d’un élément à un autre. Un autre exemple est une clé Chroma, dans laquelle l’arrière-plan d’un clip est entré et remplacé par une autre piste. (Les prévisions météorologiques devant une image satelite sont un exemple de masquage Chroma.)

DES utilise une structure arborescente pour représenter une modification :

-   Les clips audio et vidéo forment les nœuds terminaux ou les objets *sources* .
-   Une collection de sources avec un type de média uniforme (audio ou vidéo) est une *piste*.
-   Une collection de pistes est une *composition*. Une composition est rendue comme composite de toutes les pistes qu’elle contient. Les compositions peuvent contenir d’autres compositions, ce qui permet des dispositions complexes des pistes.
-   Une collection de niveau supérieur de compositions et de pistes (représentant toutes le même type de média) est un *groupe*.
-   Un ensemble d’un ou plusieurs groupes forme une *chronologie*. La chronologie est le nœud racine de l’arborescence.

Une chronologie doit contenir au moins un groupe. Chaque groupe représente un seul flux dans la production finale. Un projet standard comprend un groupe vidéo et un groupe audio. Les compositions sont facultatives. ils existent pour fournir davantage de structure si nécessaire.

L’illustration suivante montre les relations parent-enfant qui composent une chronologie :

![structure de nœud](images/timeline1.png)

L’exemple suivant montre une chronologie sous la forme d’une séquence temporelle :

![illustration de la chronologie](images/timeline2.png)

La flèche située en haut représente le sens de la chronologie, à partir de l’heure zéro. Dans le groupe vidéo, Track 1 a une priorité plus élevée que Track 0. Les objets sources de Track 1 les masquent dans Track 0. Où Track 1 est vide, Track 0» s’affiche. Comme mentionné précédemment, les pistes audio sont simplement mélangées.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main avec les Services d’édition DirectShow](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[Construction d’une chronologie](constructing-a-timeline.md)
</dt> </dl>

 

 



