---
description: à propos du générateur de Graph de Capture
ms.assetid: 9399a06e-7305-41e8-aefe-3d158052a8ed
title: à propos du générateur de Graph de Capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae321665e0eae65a1d464bf87a12ac33e935d7ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112406"
---
# <a name="about-the-capture-graph-builder"></a>à propos du générateur de Graph de Capture

Un graphique de filtre qui effectue une capture vidéo ou audio est appelé *graphique de capture*. Les graphiques de capture sont souvent plus complexes que les graphiques de lecture de fichier. pour faciliter la création de graphiques de capture par les applications, DirectShow fournit un objet d’assistance appelé capture Graph Builder. le générateur de Graph de capture expose l’interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) , qui contient des méthodes pour la génération et le contrôle d’un graphique de Capture. le diagramme suivant illustre le générateur de Graph de Capture et l’interface **ICaptureGraphBuilder2** .

![utilisation du générateur de graphiques de capture](images/cgb01.png)

commencez par appeler CoCreateInstance pour créer des instances de Capture Graph Builder et le gestionnaire de Graph de filtre. initialisez ensuite le générateur de Graph de Capture en appelant [**ICaptureGraphBuilder2 :: SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) avec un pointeur vers l’interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) du filtre Graph Manager. Le diagramme suivant illustre ce processus.

![initialisation du générateur de graphiques de capture](images/cgb03.png)

Le code suivant illustre une fonction d’assistance pour effectuer les étapes suivantes :


```C++
HRESULT InitCaptureGraphBuilder(
  IGraphBuilder **ppGraph,  // Receives the pointer.
  ICaptureGraphBuilder2 **ppBuild  // Receives the pointer.
)
{
    if (!ppGraph || !ppBuild)
    {
        return E_POINTER;
    }
    IGraphBuilder *pGraph = NULL;
    ICaptureGraphBuilder2 *pBuild = NULL;

    // Create the Capture Graph Builder.
    HRESULT hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL, 
        CLSCTX_INPROC_SERVER, IID_ICaptureGraphBuilder2, (void**)&pBuild );
    if (SUCCEEDED(hr))
    {
        // Create the Filter Graph Manager.
        hr = CoCreateInstance(CLSID_FilterGraph, 0, CLSCTX_INPROC_SERVER,
            IID_IGraphBuilder, (void**)&pGraph);
        if (SUCCEEDED(hr))
        {
            // Initialize the Capture Graph Builder.
            pBuild->SetFiltergraph(pGraph);

            // Return both interface pointers to the caller.
            *ppBuild = pBuild;
            *ppGraph = pGraph; // The caller must release both interfaces.
            return S_OK;
        }
        else
        {
            pBuild->Release();
        }
    }
    return hr; // Failed
}
```



tout au long de cette section sur la capture vidéo, il est supposé que vous utilisez le générateur de Graph de capture pour créer le graphique de capture. Toutefois, il est possible de créer des graphiques de capture entièrement à l’aide de méthodes IGraphBuilder. il s’agit d’une rubrique avancée, toutefois, et les méthodes de création de Graph de Capture sont préférées. Pour plus d’informations, consultez [Rubriques avancées](advanced-capture-topics.md)sur la capture.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de la capture vidéo dans DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



