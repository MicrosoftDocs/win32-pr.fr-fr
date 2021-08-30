---
description: Choix du convertisseur vidéo approprié
ms.assetid: c57c4c68-ea1c-4198-94b4-e9b6e53bb625
title: Choix du convertisseur vidéo approprié
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b09c47357a61680902e47df080ae971b1d4bba4e569660aa3ad41df1c300c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131229"
---
# <a name="choosing-the-right-video-renderer"></a>Choix du convertisseur vidéo approprié

DirectShow fournit plusieurs filtres de convertisseur vidéo, résumés dans le tableau suivant.



| Filtrer                                                                  | Remarques                                           |
|-------------------------------------------------------------------------|---------------------------------------------------|
| [**Rendu vidéo amélioré**](enhanced-video-renderer-filter.md) (EVR) | Utilise Direct3D 9. requiert Windows Vista ou version ultérieure. |
| [Convertisseur de mixage vidéo 9](video-mixing-renderer-filter-9.md) (VMR-9)   | Utilise Direct3D 9. requiert Windows XP ou version ultérieure.    |
| [Filtre de mixage vidéo 7](video-mixing-renderer-filter-7.md) (VMR-7)     | Utilise DirectDraw. requiert Windows XP ou version ultérieure.    |
| [Superposition Mixer](using-the-overlay-mixer-in-video-capture.md)           | Prend en charge les superpositions matérielles via DirectDraw.    |
| Filtre de [convertisseur vidéo](video-renderer-filter.md) hérité.              | Utilise DirectDraw ou (rarement) GDI                   |



 

le convertisseur à utiliser dépend en grande partie des versions de Windows que vous devez prendre en charge.

-   dans Windows Vista et versions ultérieures, les applications doivent utiliser le EVR si le matériel le prend en charge. Sinon, revenez à VMR-9 ou VMR-7. Le EVR offre de meilleures performances et une meilleure qualité vidéo que les convertisseurs précédents. En outre, il est conçu pour fonctionner avec le Gestionnaire de fenêtrage (DWM).
-   avant Windows Vista, utilisez VMR-9 si le matériel prend en charge les fonctionnalités du port informatique et de la vidéo n’est pas nécessaire. Dans le cas contraire, utilisez VMR-7.
-   sur les systèmes plus anciens, vous devrez peut-être utiliser la Mixer de superposition (pour la prise en charge de port vidéo ou de recouvrement matériel) ou le filtre de convertisseur vidéo hérité.

Les méthodes [**IGraphBuilder :: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) et [**RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) utilisent VMR-7 par défaut. Si le matériel ne prend pas en charge VMR-7, ces méthodes reviennent au filtre de convertisseur vidéo hérité. EVR et VMR-9 ne sont jamais les convertisseurs par défaut.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu vidéo](video-rendering.md)
</dt> </dl>

 

 



