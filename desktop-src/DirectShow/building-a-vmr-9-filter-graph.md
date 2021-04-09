---
description: Création d’un graphique de filtre VMR-9
ms.assetid: fd83a89c-f1b6-48a3-971e-04ae4ac14c66
title: Création d’un graphique de filtre VMR-9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d7fc1eb0982b47f5ef50a00a1c7a275dd8bf60
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846566"
---
# <a name="building-a-vmr-9-filter-graph"></a><span data-ttu-id="4bc17-103">Création d’un graphique de filtre VMR-9</span><span class="sxs-lookup"><span data-stu-id="4bc17-103">Building a VMR-9 Filter Graph</span></span>

<span data-ttu-id="4bc17-104">Étant donné que le filtre de mixage vidéo 9 Filter (VMR-9) n’est pas le convertisseur vidéo par défaut, une application qui utilise VMR-9 doit l’ajouter explicitement au graphique et la connecter.</span><span class="sxs-lookup"><span data-stu-id="4bc17-104">Because the Video Mixing Renderer 9 Filter (VMR-9) is not the default video renderer, an application that uses the VMR-9 must explicitly add it to the graph and connect it.</span></span> <span data-ttu-id="4bc17-105">Cette section présente deux approches différentes de la création de graphiques de filtre avec VMR-9.</span><span class="sxs-lookup"><span data-stu-id="4bc17-105">This section presents two different approaches to building filter graphs with the VMR-9.</span></span>

<span data-ttu-id="4bc17-106">Utilisation du générateur de graphiques de capture</span><span class="sxs-lookup"><span data-stu-id="4bc17-106">Using the Capture Graph Builder</span></span>

<span data-ttu-id="4bc17-107">Le générateur de graphiques de capture est un objet d’assistance pour la création de graphiques de filtres personnalisés.</span><span class="sxs-lookup"><span data-stu-id="4bc17-107">The Capture Graph Builder is a helper object for building custom filter graphs.</span></span> <span data-ttu-id="4bc17-108">Vous pouvez l’utiliser pour générer des graphiques VMR-9 comme suit :</span><span class="sxs-lookup"><span data-stu-id="4bc17-108">You can use it to build VMR-9 graphs as follows:</span></span>

1.  <span data-ttu-id="4bc17-109">Créez et initialisez le générateur de graphiques de capture, comme décrit dans la rubrique [à propos du générateur de graphiques de capture](about-the-capture-graph-builder.md).</span><span class="sxs-lookup"><span data-stu-id="4bc17-109">Create and initialize the Capture Graph Builder, as described in the topic [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
2.  <span data-ttu-id="4bc17-110">Appelez CoCreateInstance pour créer VMR-9 :</span><span class="sxs-lookup"><span data-stu-id="4bc17-110">Call CoCreateInstance to create the VMR-9:</span></span>
    ```C++
    IBaseFilter *pVmr = NULL;
    hr = CoCreateInstance(CLSID_VideoMixingRenderer9, 0, 
        CLSCTX_INPROC_SERVER, IID_IBaseFilter, (void**)&pVmr);
    ```

    

3.  <span data-ttu-id="4bc17-111">Appelez [**IFilterGraph :: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) sur le gestionnaire de graphique de filtre pour ajouter VMR-9 au graphique de filtre :</span><span class="sxs-lookup"><span data-stu-id="4bc17-111">Call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) on the Filter Graph Manager to add the VMR-9 to the filter graph:</span></span>
    ```C++
    hr = pGraph->AddFilter(pVmr, L"VMR9");
    ```

    

4.  <span data-ttu-id="4bc17-112">Appelez [**IGraphBuilder :: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) pour ajouter un filtre source pour le fichier vidéo :</span><span class="sxs-lookup"><span data-stu-id="4bc17-112">Call [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) to add a source filter for the video file:</span></span>
    ```C++
    IBaseFilter *pSource;
    hr = pGraph->AddSourceFilter(L"C:\\Example.avi", L"Source1", &pSource);
    ```

    

5.  <span data-ttu-id="4bc17-113">Appelez la méthode [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) pour afficher le flux vidéo dans VMR :</span><span class="sxs-lookup"><span data-stu-id="4bc17-113">Call the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method to render the video stream to the VMR:</span></span>
    ```C++
    hr = pBuild->RenderStream(0, 0, pSource, 0, pVmr);  
    ```

    

6.  <span data-ttu-id="4bc17-114">Vous pouvez également appeler RenderStream à nouveau pour afficher le flux audio :</span><span class="sxs-lookup"><span data-stu-id="4bc17-114">Optionally, call RenderStream again to render the audio stream:</span></span>
    ```C++
    hr = pBuild->RenderStream(0, &MEDIATYPE_Audio, pSource, 0, NULL);
    ```

    

<span data-ttu-id="4bc17-115">Vous pouvez mélanger plusieurs flux vidéo en appelant AddSourceFilter et RenderStream pour chaque fichier source.</span><span class="sxs-lookup"><span data-stu-id="4bc17-115">You can mix several video streams by calling AddSourceFilter and RenderStream for each source file.</span></span>

<span data-ttu-id="4bc17-116">Utilisation du gestionnaire de graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="4bc17-116">Using the Filter Graph Manager</span></span>

<span data-ttu-id="4bc17-117">Si vous préférez ne pas utiliser le générateur de graphiques de capture, vous pouvez créer un graphique VMR-9 en utilisant simplement des méthodes sur le gestionnaire de graphique de filtre, comme suit :</span><span class="sxs-lookup"><span data-stu-id="4bc17-117">If you prefer not to use the Capture Graph Builder, you can build a VMR-9 graph simply using methods on the Filter Graph Manager, as follows:</span></span>

1.  <span data-ttu-id="4bc17-118">Créez VMR-9 et ajoutez-le au graphique, comme indiqué dans la procédure précédente.</span><span class="sxs-lookup"><span data-stu-id="4bc17-118">Create the VMR-9 and add it to the graph, as shown in the previous procedure.</span></span>
2.  <span data-ttu-id="4bc17-119">Utilisez AddSourceFilter pour ajouter un filtre source pour le fichier vidéo, comme indiqué dans la procédure précédente.</span><span class="sxs-lookup"><span data-stu-id="4bc17-119">Use AddSourceFilter to add a source filter for the video file, as shown in the previous procedure.</span></span>
3.  <span data-ttu-id="4bc17-120">Si vous souhaitez restituer l’audio, créez une instance du filtre de [convertisseur DirectSound](directsound-renderer-filter.md) et ajoutez-la au graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="4bc17-120">If you want to render the audio, create an instance of the [DirectSound Renderer](directsound-renderer-filter.md) filter and add it to the filter graph.</span></span>
4.  <span data-ttu-id="4bc17-121">Utilisez la méthode IBaseFilter :: EnumPins pour rechercher une broche de sortie sur le filtre source.</span><span class="sxs-lookup"><span data-stu-id="4bc17-121">Use the IBaseFilter::EnumPins method to find an output pin on the source filter.</span></span> <span data-ttu-id="4bc17-122">Pour plus d’informations, consultez [énumération des codes confidentiels](enumerating-pins.md) .</span><span class="sxs-lookup"><span data-stu-id="4bc17-122">See [Enumerating Pins](enumerating-pins.md) for details.</span></span>
5.  <span data-ttu-id="4bc17-123">Interrogez le gestionnaire du graphique de filtre pour l’interface IFilterGraph2.</span><span class="sxs-lookup"><span data-stu-id="4bc17-123">Query the Filter Graph Manager for the IFilterGraph2 interface.</span></span>
6.  <span data-ttu-id="4bc17-124">Appelez [**IFilterGraph2 :: RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) avec l' \_ indicateur AM RenderEx \_ RENDERTOEXISTINGRENDERERS.</span><span class="sxs-lookup"><span data-stu-id="4bc17-124">Call [**IFilterGraph2::RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) with the AM\_RENDEREX\_RENDERTOEXISTINGRENDERERS flag.</span></span> <span data-ttu-id="4bc17-125">Cet appel génère le rendu de la broche de sortie, en utilisant uniquement les filtres de convertisseur déjà présents dans le graphique, dans ce cas, VMR-9 et le convertisseur DirectSound.</span><span class="sxs-lookup"><span data-stu-id="4bc17-125">This call renders the output pin, using only the renderer filters already in the graph — in this case, the VMR-9 and the DirectSound Renderer.</span></span> <span data-ttu-id="4bc17-126">Cela empêche la logique de connexion intelligente d’ajouter le convertisseur vidéo par défaut au graphique, ce qui laisse le VMR-9 non connecté.</span><span class="sxs-lookup"><span data-stu-id="4bc17-126">This prevents the Intelligent Connect logic from adding the default video renderer to the graph, which would leave the VMR-9 unconnected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4bc17-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4bc17-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bc17-128">Création de graphiques à l’aide du générateur de graphiques de capture</span><span class="sxs-lookup"><span data-stu-id="4bc17-128">Building Graphs with the Capture Graph Builder</span></span>](building-graphs-with-the-capture-graph-builder.md)
</dt> </dl>

 

 



