---
description: Capturer un fichier DV de type 1
ms.assetid: fba11e9b-4900-4b29-a0c9-702272cd7387
title: Capturer un fichier DV de type 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8098669f124bdd4c0168e3549cd8eed8e1825c47
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296891"
---
# <a name="capture-a-type-1-dv-file"></a>Capturer un fichier DV de type 1

Un fichier AVI DV type-1 contient un flux entrelacé unique. Pour capturer un fichier type-1 pendant l’aperçu, utilisez le graphique de filtre illustré dans le diagramme suivant.

![capture de type 1 avec aperçu](images/dv1-cap.png)

Les filtres dans ce graphique sont les suivants :

-   Le filtre [tee intelligent](smart-tee-filter.md) divise le DV entrelacé en un flux de capture et un flux d’aperçu. Les deux flux contiennent les mêmes données entrelacées.
-   Le [rédacteur](file-writer-filter.md) [AVI](avi-mux-filter.md) et le writer de fichier écrivent le flux entrelacé sur le disque.
-   Le [séparateur DV](dv-splitter-filter.md) divise le flux entrelacé en un flux vidéo DV et un flux audio. Les deux flux sont rendererd pour la version préliminaire.
-   Le [décodeur vidéo DV](dv-video-decoder-filter.md) décode le flux vidéo DV pour l’aperçu.

Générez ce graphique comme suit :


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)
IBaseFilter           *pAviMux    // Avi Mux filter.

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Create the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("C:\\Example1.avi"), &pAviMux, 0);

// Render the capture stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Interleaved, 
    pDV, 0, pAviMux);

// Render the preview stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Interleaved,
    pDV, 0, 0);

// Remember to release all interfaces.
```



1.  Appelez [**ICaptureGraphBuilder2 :: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) pour connecter le filtre multiplex MUX au filtre du writer de fichier.
2.  Appelez [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) avec la catégorie PIN catégorie code confidentiel \_ \_ capturer pour restituer le flux de capture. le générateur de Graph de Capture insère automatiquement le filtre Tee intelligent.
3.  Appelez à nouveau RenderStream, mais avec l’aperçu catégorie pin catégorie PIN \_ \_ , pour afficher le flux d’aperçu. Ignorez cet appel si vous ne souhaitez pas afficher un aperçu de la vidéo.

Pour les deux appels à RenderStream, le type de média est MEDIATYPE entrelacé, ce qui signifie qu’il s’agit d’une \_ vidéo DV entrelacée. dans ce code, le générateur de Graph de capture ajoute automatiquement chaque filtre requis, à l’exception du filtre de capture MSDV.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vidéo numérique en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



