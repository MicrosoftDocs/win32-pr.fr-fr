---
description: 'Cet exemple crée un graphique d’aperçu vidéo à l’aide de la méthode ICaptureGraphBuilder2 :: RenderStream dans DirectShow.'
ms.assetid: 9b401de1-910a-41f7-bf80-dda73ee4a204
title: Aperçu de la vidéo (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482fed2e164bbe867d848b05d417c89d0790256f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127223161"
---
# <a name="previewing-video-directshow"></a>Aperçu de la vidéo (DirectShow)

Pour générer un graphique d’aperçu vidéo, appelez la méthode [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) comme suit :


```C++
ICaptureGraphBuilder2 *pBuild; // Capture Graph Builder
// Initialize pBuild (not shown).

IBaseFilter *pCap; // Video capture filter.

/* Initialize pCap and add it to the filter graph (not shown). */

hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
    pCap, NULL, NULL);
```



Cet exemple suppose les points suivants :

-   *pBuild* a été initialisé, comme décrit dans [à propos du générateur de Graph de Capture](about-the-capture-graph-builder.md).
-   *pCap* a été initialisé, en créant une instance du filtre de capture et en l’ajoutant au graphique de filtre, comme décrit dans [sélection d’un périphérique de capture](selecting-a-capture-device.md).

Le premier paramètre de la méthode [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) spécifie une catégorie de code confidentiel ; pour un graphique en préversion, utilisez l' **\_ \_ aperçu de catégorie pin**. Le deuxième paramètre spécifie un type de média, comme un GUID de type principal. Pour la vidéo, utilisez la **\_ vidéo MediaType**. Les périphériques DV offrent un son et une vidéo entrelacés, pour lesquels le type de média est de type **MediaType \_ entrelacé**. (Pour plus d’informations sur la capture DV, consultez [vidéo numérique dans DirectShow](digital-video-in-directshow.md).)

Le troisième paramètre est un pointeur vers l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) du filtre de capture. Les deux paramètres suivants ne sont pas nécessaires dans cet exemple. Ils sont utilisés pour spécifier des filtres supplémentaires qui peuvent être nécessaires pour restituer le flux. si vous affectez la **valeur NULL** au dernier paramètre, le générateur de Graph de Capture sélectionne un convertisseur par défaut pour le flux, en fonction du type de média. pour la vidéo, le générateur de Graph de Capture utilise toujours le filtre de [convertisseur vidéo](video-renderer-filter.md) comme convertisseur par défaut.

> [!Note]  
> dans Windows XP et versions ultérieures, bien que le convertisseur de mixage vidéo (VMR) soit le convertisseur vidéo par défaut pour les méthodes [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) , il ne s’agit pas du convertisseur par défaut pour la méthode [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) . sur n’importe quelle plateforme, le générateur de Graph de Capture utilise toujours l’ancien filtre de convertisseur vidéo, sauf indication contraire.

 

Bien que la catégorie pin soit fournie en tant qu' **\_ \_ aperçu de la catégorie pin**, il n’est pas important de savoir si le filtre a réellement un pin de préversion ; il peut avoir une broche de port vidéo ou simplement une broche de capture. dans les deux cas, le générateur de Graph de Capture génère automatiquement le graphique approprié.

Le diagramme suivant montre le graphique le plus simple possible pour afficher un aperçu de la vidéo.

![graphique d’aperçu vidéo](images/vidcap01.png)

Dans ce diagramme, le filtre de capture a une broche d’aperçu, qui se connecte directement au convertisseur vidéo.

si le filtre de capture a uniquement un code confidentiel de capture, le générateur de Graph de capture insère un filtre [Tee intelligent](smart-tee-filter.md) , qui fractionne le flux en un flux de capture et un flux d’aperçu. Cela est décrit plus en détail dans [combinaison de capture vidéo et d’aperçu](combining-video-capture-and-preview.md).

dans certains cas, le flux vidéo doit passer par la superposition Mixer filtre. Si c’est le cas, la méthode [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) l’ajoute automatiquement au graphique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Combinaison de la capture vidéo et de l’aperçu](combining-video-capture-and-preview.md)
</dt> <dt>

[Capture vidéo](video-capture.md)
</dt> </dl>

 

 



