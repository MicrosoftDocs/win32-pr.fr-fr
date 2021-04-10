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
# <a name="about-the-capture-graph-builder"></a><span data-ttu-id="e1a0e-103">À propos du générateur de graphiques de capture</span><span class="sxs-lookup"><span data-stu-id="e1a0e-103">About the Capture Graph Builder</span></span>

<span data-ttu-id="e1a0e-104">Un graphique de filtre qui effectue une capture vidéo ou audio est appelé *graphique de capture*.</span><span class="sxs-lookup"><span data-stu-id="e1a0e-104">A filter graph that performs video or audio capture is called a *capture graph*.</span></span> <span data-ttu-id="e1a0e-105">Les graphiques de capture sont souvent plus complexes que les graphiques de lecture de fichier.</span><span class="sxs-lookup"><span data-stu-id="e1a0e-105">Capture graphs are often more complicated than file playback graphs.</span></span> <span data-ttu-id="e1a0e-106">Pour faciliter la création de graphiques de capture par les applications, DirectShow fournit un objet d’assistance appelé le générateur de graphiques de capture.</span><span class="sxs-lookup"><span data-stu-id="e1a0e-106">To make it easier for applications to build capture graphs, DirectShow provides a helper object called the Capture Graph Builder.</span></span> <span data-ttu-id="e1a0e-107">Le générateur de graphiques de capture expose l’interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) , qui contient des méthodes pour la génération et le contrôle d’un graphique de capture.</span><span class="sxs-lookup"><span data-stu-id="e1a0e-107">The Capture Graph Builder exposes the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface, which contains methods for building and controlling a capture graph.</span></span> <span data-ttu-id="e1a0e-108">Le diagramme suivant illustre le générateur de graphiques de capture et l’interface **ICaptureGraphBuilder2** .</span><span class="sxs-lookup"><span data-stu-id="e1a0e-108">The following diagram illustrates the Capture Graph Builder and the **ICaptureGraphBuilder2** interface.</span></span>

![utilisation du générateur de graphiques de capture](images/cgb01.png)

<span data-ttu-id="e1a0e-110">Commencez par appeler CoCreateInstance pour créer de nouvelles instances du générateur de graphiques de capture et du gestionnaire de graphes de filtre.</span><span class="sxs-lookup"><span data-stu-id="e1a0e-110">Start by calling CoCreateInstance to create new instances of the Capture Graph Builder and the Filter Graph Manager.</span></span> <span data-ttu-id="e1a0e-111">Ensuite, initialisez le générateur de graphiques de capture en appelant [**ICaptureGraphBuilder2 :: SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) avec un pointeur vers l’interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) du gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="e1a0e-111">Then initialize the Capture Graph Builder by calling [**ICaptureGraphBuilder2::SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) with a pointer to the Filter Graph Manager's [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface.</span></span> <span data-ttu-id="e1a0e-112">Le diagramme suivant illustre ce processus.</span><span class="sxs-lookup"><span data-stu-id="e1a0e-112">The following diagram illustrates this process.</span></span>

![initialisation du générateur de graphiques de capture](images/cgb03.png)

<span data-ttu-id="e1a0e-114">Le code suivant illustre une fonction d’assistance pour effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e1a0e-114">The following code shows a helper function to perform these steps:</span></span>


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



<span data-ttu-id="e1a0e-115">Tout au long de cette section sur la capture vidéo, il est supposé que vous utilisez le générateur de graphiques de capture pour créer le graphique de capture.</span><span class="sxs-lookup"><span data-stu-id="e1a0e-115">Throughout this section on video capture, it is assumed that you are using the Capture Graph Builder to create the capture graph.</span></span> <span data-ttu-id="e1a0e-116">Toutefois, il est possible de créer des graphiques de capture entièrement à l’aide de méthodes IGraphBuilder.</span><span class="sxs-lookup"><span data-stu-id="e1a0e-116">However, it is possible to build capture graphs entirely by using IGraphBuilder methods.</span></span> <span data-ttu-id="e1a0e-117">Il s’agit d’une rubrique avancée, toutefois, et les méthodes de création de graphiques de capture sont préférées.</span><span class="sxs-lookup"><span data-stu-id="e1a0e-117">This is considered an advanced topic, however, and the Capture Graph Builder methods are preferred.</span></span> <span data-ttu-id="e1a0e-118">Pour plus d’informations, consultez [Rubriques avancées](advanced-capture-topics.md)sur la capture.</span><span class="sxs-lookup"><span data-stu-id="e1a0e-118">For more information, see [Advanced Capture Topics](advanced-capture-topics.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1a0e-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e1a0e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1a0e-120">À propos de la capture vidéo dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="e1a0e-120">About Video Capture in DirectShow</span></span>](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



