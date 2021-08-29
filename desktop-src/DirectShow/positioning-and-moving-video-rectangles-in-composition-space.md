---
title: Placer et déplacer des rectangles vidéo dans l’espace de composition
description: Positionnement et déplacement de rectangles vidéo dans l’espace de composition
ms.assetid: 97e7bb24-79f6-4638-a9c4-ac09dbd29be9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 563509e062335f496f001d8d61dae8eecfe2cff998da6e63320a7c95c347438c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583603"
---
# <a name="position-and-move-video-rectangles-in-composition-space"></a>Placer et déplacer des rectangles vidéo dans l’espace de composition

Lorsque VMR mélange plusieurs flux d’entrée, il place chaque flux dans un rectangle normalisé, appelé « espace de composition ». Dans l’espace de composition, les coordonnées (0,0, 0,0) à (1,0, 1,0) forment le rectangle vidéo visible. Toutes les coordonnées qui se trouvent en dehors de ce rectangle sont découpées.

Une application peut effectuer des effets spéciaux en déplaçant, en étirant et en réduisant la vidéo d’un flux d’entrée, en modifiant le rectangle de destination dans l’espace de composition pour ce flux. Si le rectangle spécifié est d’une taille différente de celle du rectangle vidéo natif, la vidéo Native sera réduite ou étirée pour s’ajuster. Le rectangle de destination est spécifié en appelant la méthode [**IVMRMixerControl :: SetOutputRect**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs) .

Supposons, par exemple, que le flux 0 (qui correspond à la broche 0) contient le flux vidéo principal et que Stream 1 (qui correspond à pin 1) contienne une vidéo secondaire. Stream 1 peut être positionné complètement hors-écran en spécifiant un rectangle normalisé de {-1.0 f, 0.0 f, 0.0 f, 1.0 f}. Stream 1 peut ensuite être déplacé dans la zone visible en modifiant les côtés gauche et droit du rectangle lors des appels successifs à **SetOutputRect**:



| Étiquette | Valeur |
|--------|-----------------------------|
| Heure   | Rectangle                   |
| t + 0  | {-1.0 f, 0.0 f, 0.0 f, 1.0 f} |
| t + 1  | {-0,9 f, 0.0 f, 0.1 f, 1.0 f} |
| t + 2  | {-0,8 f, 0.0 f, 0,2 f, 1.0 f} |
| ...    | ...                         |
| t + 10 | {0.0 f, 0.0 f, 1.0 f, 1.0 f}  |



 

![déplacement d’un flux vidéo dans l’espace de composition](images/composition-space.png)

À l’heure t + 10, la vidéo de Stream 1 est entièrement visible. Dans cet exemple, la taille native de Stream 1 a été maintenue pendant le déplacement. Vous pouvez également étirer ou réduire le rectangle pour produire des effets intéressants. Vous pouvez également retourner la vidéo verticalement, en spécifiant une valeur supérieure à la partie inférieure du bas, ou mettre la vidéo en miroir horizontalement en spécifiant une valeur supérieure pour la gauche par rapport à la droite.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du mode de mixage VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



