---
description: À propos du générateur de graphiques de capture
ms.assetid: 9399a06e-7305-41e8-aefe-3d158052a8ed
title: À propos du générateur de graphiques de capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae321665e0eae65a1d464bf87a12ac33e935d7ac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950291"
---
# <a name="about-the-capture-graph-builder"></a>À propos du générateur de graphiques de capture

Un graphique de filtre qui effectue une capture vidéo ou audio est appelé *graphique de capture*. Les graphiques de capture sont souvent plus complexes que les graphiques de lecture de fichier. Pour faciliter la création de graphiques de capture par les applications, DirectShow fournit un objet d’assistance appelé le générateur de graphiques de capture. Le générateur de graphiques de capture expose l’interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) , qui contient des méthodes pour la génération et le contrôle d’un graphique de capture. Le diagramme suivant illustre le générateur de graphiques de capture et l’interface **ICaptureGraphBuilder2** .

![utilisation du générateur de graphiques de capture](images/cgb01.png)

Commencez par appeler CoCreateInstance pour créer de nouvelles instances du générateur de graphiques de capture et du gestionnaire de graphes de filtre. Ensuite, initialisez le générateur de graphiques de capture en appelant [**ICaptureGraphBuilder2 :: SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) avec un pointeur vers l’interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) du gestionnaire de graphique de filtre. Le diagramme suivant illustre ce processus.

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



Tout au long de cette section sur la capture vidéo, il est supposé que vous utilisez le générateur de graphiques de capture pour créer le graphique de capture. Toutefois, il est possible de créer des graphiques de capture entièrement à l’aide de méthodes IGraphBuilder. Il s’agit d’une rubrique avancée, toutefois, et les méthodes de création de graphiques de capture sont préférées. Pour plus d’informations, consultez [Rubriques avancées](advanced-capture-topics.md)sur la capture.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de la capture vidéo dans DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



