---
description: Transmettre à partir d’un fichier de type-1
ms.assetid: 5be2248b-7917-4c1b-9ae7-29e06779eac6
title: Transmettre à partir d’un fichier de type-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e38ed3e549b6cd671248ba1df9b24df8fbfe3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034662"
---
# <a name="transmit-from-type-1-file"></a>Transmettre à partir d’un fichier de type-1

Pour transmettre un fichier de type 1 lors de l’aperçu du fichier, utilisez le graphique de filtre illustré dans le diagramme suivant.

![type-1 transmettre avec aperçu](images/dv1-transmit.png)

Les filtres dans ce graphique sont les suivants :

-   Le [séparateur AVI](avi-splitter-filter.md) analyse le fichier avi. Pour un fichier DV de type 1, la broche de sortie fournit des exemples DV entrelacés.
-   Le filtre [tee de pin infini](infinite-pin-tee-filter.md) divise le DV entrelacé en un flux de transmission et un flux d’aperçu. Les deux flux contiennent les mêmes données entrelacées. (Ce graphique utilise le code PIN infini plutôt que le [tee intelligent](smart-tee-filter.md), car il n’y a aucun risque de supprimer des frames lors de la lecture d’un fichier, comme c’est le cas avec la capture en direct.)
-   Le [séparateur DV](dv-splitter-filter.md) divise le flux entrelacé en un flux vidéo DV, qui est décodé par le [décodeur vidéo DV](dv-video-decoder-filter.md), et un flux audio. Les deux flux sont rendererd pour la version préliminaire.

Générez ce graphique comme suit :


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Add the Infinite Pin Tee filter to the graph.
IBaseFilter *pTee;
hr = CoCreateInstance(CLSID_InfTee, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pTee));
hr = pGraph->AddFilter(pTee, L"Tee");

// Add the File Source filter to the graph.
IBaseFilter *pFileSource;
hr = pGraph->AddSourceFilter(
    L"C:\\YourFileNameHere.avi",
    L"Source", 
    &pFileSource);

// Add the AVI Splitter filter to the graph.
IBaseFilter *pAviSplit;
hr = CoCreateInstance(CLSID_AviSplitter, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pAviSplit));
hr = pGraph->AddFilter(pAviSplit, L"AVI Splitter");

// Connect the file source to the AVI Splitter.
hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pAviSplit);
if (FAILED(hr))
{
    // This is not an AVI file. 
}

// Connect the file source to the Infinite Pin Tee.
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pAviSplit, 0, pTee);
if (FAILED(hr))
{
    // This is not a type-1 DV file.
}

// Render one stream from the Infinite Pin Tee to MSDV, for transmit.
hr = pBuilder->RenderStream(0, 0, pTee, 0, pDV);

// Render another stream from the Infinite Pin Tee for preview.
hr = pBuilder->RenderStream(0, 0, pTee, 0, 0);
```



1.  Appelez [**IGraphBuilder :: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) pour ajouter le filtre source au graphique de filtre.
2.  Créez le séparateur AVI et le code confidentiel infini, puis ajoutez-les au graphique.
3.  Appelez [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) pour connecter le filtre source au séparateur avi. La spécification \_ de MediaType entrelacée pour s’assurer que la méthode échoue si le fichier source n’est pas un fichier DV de type 1. Dans ce cas, vous pouvez revenir en arrière et tenter de générer un graphique de type 2 transmit à la place.
4.  Appelez à nouveau **RenderStream** pour acheminer le flux entrelacé du séparateur AVI vers le code PIN tee infini
5.  Appelez RenderStream une troisième fois pour acheminer un flux du code confidentiel infini vers le filtre MSDV, pour la transmettre à l’appareil.
6.  Appelez **RenderStream** une dernière fois pour générer la section d’aperçu du graphique.

Si vous ne souhaitez pas afficher l’aperçu, connectez simplement la source du fichier au filtre MSDV :


```C++
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pFileSource, 0, pDV);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vidéo numérique dans DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



