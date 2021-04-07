---
description: Mappage de coordonnées dans VMR
ms.assetid: f0821b90-51d1-4e77-8aed-04337a3dd623
title: Mappage de coordonnées dans VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c18b38249471e6e68e36f1b9051f51e920f62b31
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846009"
---
# <a name="coordinate-mapping-in-the-vmr"></a>Mappage de coordonnées dans VMR

Cette section décrit les cinq transformations appliquées à une image source avant qu’elle ne soit mappée par VMR sur l’image finale de sortie.

1.  La transformation *T (SRC)* mappe le rectangle source au rectangle de destination. Celles-ci sont spécifiées par les membres **rcSource** et **rcTarget** de la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) ou [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) dans le type de média. Ce mappage prétraite l’image source lorsqu’elle est transmise au VMR.
2.  La transformation *T (indicateur)* effectue toute manipulation d’image spécifiée par des indicateurs dans l’exemple de support. Ces transformations incluses, telles que la translation verticale et l’échelle, permettent de gérer les indicateurs entrelacés de Bob. La transformation entrelacée double la hauteur de l’image et éventuellement convertit l’image par la moitié d’une ligne vidéo, si elle se trouve dans le champ impair.
3.  La transformation *T (AR)* ajuste l’image en pixels carrés, en fonction des proportions de l’image. Pour les types de média **VIDEOINFOHEADER** , les proportions sont déterminées par la taille de l’image. Pour les types **VIDEOINFOHEADER2** , les proportions sont déterminées par les champs **dwPictAspectRatioX** et **dwPictAspectRatioY** , à moins que les indicateurs de remplissage 16 x 9 \_ ou AMCONTROL pour 4x3 \_ \_ \_ \_ \_ soient définis. Cette transformation suppose que le paramètre d’affichage de l’analyse correspond aux proportions physiques de l’analyse. Par exemple, si l’utilisateur a une analyse avec des proportions de 4 x 3, mais définit l’affichage sur 1280 x 768 pixels (5 x 3), l’image n’aura pas les proportions correctes.
4.  Les transformations de transformation *T (Mix)* déplacent l’image dans l’image de destination, à l’aide des rectangles normalisés spécifiés dans les méthodes [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) . Les rectangles normalisés permettent à l’application d’organiser le positionnement et la mise à l’échelle des flux sources l’un par rapport à l’autre. VMR calcule l’image de destination en calculant les dimensions maximales de toutes les images sources et en les recentrant à l’intérieur d’un rectangle englobant global. La plage (0, 0) à (1,1) est assignée aux angles du rectangle englobant. Le rectangle englobant est fixe avant l’exécution du graphique et reste constant même si les flux sont ajoutés ou supprimés. Les rectangles de destination de chaque flux peuvent se trouver en dehors de la plage (0,0) à (1,1) et toujours être valides.
5.  Enfin, une partie de l’image mixte peut être transformée par le mappage *T (DST)*, spécifié par les rectangles source et de destination dans l’interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) sur VMR. Si le Allocator-Presenter est remplacé et que l’interface **IBasicVideo** n’est pas utilisée, l’application doit implémenter l’interface [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) et mapper les coordonnées dans un espace linéaire 2D. Les coordonnées de la souris retournées au navigateur DVD doivent également être dans cet espace. Par exemple, si une application effectue le rendu d’une vidéo sur un cube tournant, elle signale l’affichage entier pour le contrôle sans fenêtre et retourne les coordonnées de la souris par rapport à l’affichage.

La transformation d’image globale à partir des données sources vers le convertisseur final est la suivante :

T = T (SRC) \* t (indicateur) t (AR) t (Mix) t ( \* DST)\*

où \* indique que l’image peut être découpée vers l’image de destination à cette étape. Notez qu’il s’agit de toutes les transformations affines. par conséquent, VMR peut les combiner en une seule transformation.

L’inverse de la transformation est le suivant :

![transformation inverse](images/vmrmapping-t-1.png)

Le facteur T (SRC) T (indicateur) T (AR) est relatif à la résolution de la source. Dans le facteur T (Mix), le rectangle source normalisé est relatif à l’image corrigée à l’aspect. Le rectangle de destination normalisé est relatif à la résolution de sortie. Le diagramme suivant illustre ces relations.

![étapes de transformation d’image](images/vmrmapping-transform-steps.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de VMR pour les développeurs de filtres DirectShow](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



