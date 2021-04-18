---
description: Choix du convertisseur vidéo approprié
ms.assetid: c57c4c68-ea1c-4198-94b4-e9b6e53bb625
title: Choix du convertisseur vidéo approprié
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38a334fec59f6e3631217d48df7f0e8c83d87462
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513113"
---
# <a name="choosing-the-right-video-renderer"></a>Choix du convertisseur vidéo approprié

DirectShow fournit plusieurs filtres de convertisseur vidéo, résumés dans le tableau suivant.



| Filtrer                                                                  | Notes                                           |
|-------------------------------------------------------------------------|---------------------------------------------------|
| [**Rendu vidéo amélioré**](enhanced-video-renderer-filter.md) (EVR) | Utilise Direct3D 9. Nécessite Windows Vista ou une version ultérieure. |
| [Convertisseur de mixage vidéo 9](video-mixing-renderer-filter-9.md) (VMR-9)   | Utilise Direct3D 9. Nécessite Windows XP ou une version ultérieure.    |
| [Filtre de mixage vidéo 7](video-mixing-renderer-filter-7.md) (VMR-7)     | Utilise DirectDraw. Nécessite Windows XP ou une version ultérieure.    |
| [Mixage de superposition](using-the-overlay-mixer-in-video-capture.md)           | Prend en charge les superpositions matérielles via DirectDraw.    |
| Filtre de [convertisseur vidéo](video-renderer-filter.md) hérité.              | Utilise DirectDraw ou (rarement) GDI                   |



 

Le convertisseur à utiliser dépend en grande partie des versions de Windows que vous devez prendre en charge.

-   Dans Windows Vista et versions ultérieures, les applications doivent utiliser le EVR si le matériel le prend en charge. Sinon, revenez à VMR-9 ou VMR-7. Le EVR offre de meilleures performances et une meilleure qualité vidéo que les convertisseurs précédents. En outre, il est conçu pour fonctionner avec le Gestionnaire de fenêtrage (DWM).
-   Avant Windows Vista, utilisez VMR-9 si le matériel prend en charge les fonctionnalités du port informatique et de la vidéo n’est pas nécessaire. Dans le cas contraire, utilisez VMR-7.
-   Sur les systèmes plus anciens, vous devrez peut-être utiliser le mélangeur de superposition (pour le port vidéo ou la prise en charge de la superposition matérielle) ou le filtre de convertisseur vidéo hérité.

Les méthodes [**IGraphBuilder :: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) et [**RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) utilisent VMR-7 par défaut. Si le matériel ne prend pas en charge VMR-7, ces méthodes reviennent au filtre de convertisseur vidéo hérité. EVR et VMR-9 ne sont jamais les convertisseurs par défaut.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu vidéo](video-rendering.md)
</dt> </dl>

 

 



