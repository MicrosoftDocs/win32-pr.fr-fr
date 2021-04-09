---
description: Sous-objets
ms.assetid: 03cbd590-b573-4a98-9ab7-fe548800cfcb
title: Sous-objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8b427a315231577f1608a168629bc8b77d2cc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867082"
---
# <a name="subobjects"></a>Sous-objets

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Les sources, les effets et les transitions ont des pointeurs internes vers d’autres objets COM, appelés sous- *objets*. Le sous-objet effectue le travail réel de l’objet. Le sous-objet d’une source est le composant qui crée les données vidéo ou audio. Le sous-objet d’un effet ou d’une transition est le composant qui transforme les données ; par exemple, dans un effet vidéo, il crée l’effet visuel dans le flux vidéo.

Le type de sous-objet dépend du type d’objet :

-   Source : tout filtre de filtre ou d’analyseur source DirectShow qui prend en charge la recherche et produit un format pris en charge par. Il peut s’agir d’un format compressé si des filtres DirectShow existent pour le décoder.
-   Effet : pour la vidéo, n’importe quel objet de transformation Microsoft® DirectX® à un seul entré. Pour l’audio, tout filtre d’effet audio DirectShow.
-   Transition : pour la vidéo, tout objet de transformation DirectX à deux entrées 2D. L’audio ne prend pas en charge les transitions.

Les groupes, les compositions et les suivis n’ont pas de sous-objets.

L’application ne définit pas directement le pointeur de sous-objet. Pour les effets et les transitions, l’application appelle la méthode [**IAMTimelineObj :: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) pour spécifier le GUID du sous-objet. Pour les objets sources, une application appelle généralement [**IAMTimelineSrc :: SetMediaName**](iamtimelinesrc-setmedianame.md) pour spécifier le nom d’un fichier source. Toutefois, la méthode **SetSubObjectGUID** peut également être utilisée pour les objets sources, pour spécifier l’identificateur de classe (CLSID) d’un filtre.

Pour plus d’informations, consultez [utilisation des sources](working-with-sources.md) et [utilisation des effets et des transitions](working-with-effects-and-transitions.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble des composants de la chronologie](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



