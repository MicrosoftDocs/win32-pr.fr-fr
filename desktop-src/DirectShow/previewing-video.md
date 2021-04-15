---
description: Aperçu de la vidéo
ms.assetid: 9b401de1-910a-41f7-bf80-dda73ee4a204
title: Aperçu de la vidéo (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0a8f0d0a422794c4e887693e80391a99bd8d70
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104570009"
---
# <a name="previewing-video-directshow"></a><span data-ttu-id="1120c-103">Aperçu de la vidéo (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="1120c-103">Previewing Video (DirectShow)</span></span>

<span data-ttu-id="1120c-104">Pour générer un graphique d’aperçu vidéo, appelez la méthode [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) comme suit :</span><span class="sxs-lookup"><span data-stu-id="1120c-104">To build a video preview graph, call the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuild; // Capture Graph Builder
// Initialize pBuild (not shown).

IBaseFilter *pCap; // Video capture filter.

/* Initialize pCap and add it to the filter graph (not shown). */

hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
    pCap, NULL, NULL);
```



<span data-ttu-id="1120c-105">Cet exemple suppose les points suivants :</span><span class="sxs-lookup"><span data-stu-id="1120c-105">This example assumes the following:</span></span>

-   <span data-ttu-id="1120c-106">*pBuild* a été initialisé, comme décrit dans [à propos du générateur de graphiques de capture](about-the-capture-graph-builder.md).</span><span class="sxs-lookup"><span data-stu-id="1120c-106">*pBuild* was initialized, as described in [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
-   <span data-ttu-id="1120c-107">*pCap* a été initialisé, en créant une instance du filtre de capture et en l’ajoutant au graphique de filtre, comme décrit dans [sélection d’un périphérique de capture](selecting-a-capture-device.md).</span><span class="sxs-lookup"><span data-stu-id="1120c-107">*pCap* was initialized, by creating an instance of the capture filter and adding it to the filter graph, as described in [Selecting a Capture Device](selecting-a-capture-device.md).</span></span>

<span data-ttu-id="1120c-108">Le premier paramètre de la méthode [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) spécifie une catégorie de code confidentiel ; pour un graphique en préversion, utilisez l' **\_ \_ aperçu de catégorie pin**.</span><span class="sxs-lookup"><span data-stu-id="1120c-108">The first parameter to the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method specifies a pin category; for a preview graph, use **PIN\_CATEGORY\_PREVIEW**.</span></span> <span data-ttu-id="1120c-109">Le deuxième paramètre spécifie un type de média, comme un GUID de type principal.</span><span class="sxs-lookup"><span data-stu-id="1120c-109">The second parameter specifies a media type, as a major type GUID.</span></span> <span data-ttu-id="1120c-110">Pour la vidéo, utilisez la **\_ vidéo MediaType**.</span><span class="sxs-lookup"><span data-stu-id="1120c-110">For video, use **MEDIATYPE\_Video**.</span></span> <span data-ttu-id="1120c-111">Les périphériques DV offrent un son et une vidéo entrelacés, pour lesquels le type de média est de type **MediaType \_ entrelacé**.</span><span class="sxs-lookup"><span data-stu-id="1120c-111">DV devices deliver interleaved audio and video, for which the media type is **MEDIATYPE\_Interleaved**.</span></span> <span data-ttu-id="1120c-112">(Pour plus d’informations sur la capture DV, consultez [vidéo numérique dans DirectShow](digital-video-in-directshow.md).)</span><span class="sxs-lookup"><span data-stu-id="1120c-112">(For more information about DV capture, see [Digital Video in DirectShow](digital-video-in-directshow.md).)</span></span>

<span data-ttu-id="1120c-113">Le troisième paramètre est un pointeur vers l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) du filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="1120c-113">The third parameter is a pointer to the capture filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="1120c-114">Les deux paramètres suivants ne sont pas nécessaires dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="1120c-114">The next two parameters are not needed in this example.</span></span> <span data-ttu-id="1120c-115">Ils sont utilisés pour spécifier des filtres supplémentaires qui peuvent être nécessaires pour restituer le flux.</span><span class="sxs-lookup"><span data-stu-id="1120c-115">They are used to specify additional filters that might be needed to render the stream.</span></span> <span data-ttu-id="1120c-116">Si vous affectez la **valeur null** au dernier paramètre, le générateur de graphiques de capture sélectionne un convertisseur par défaut pour le flux, en fonction du type de média.</span><span class="sxs-lookup"><span data-stu-id="1120c-116">Setting the last parameter to **NULL** causes the Capture Graph Builder to select a default renderer for the stream, based on the media type.</span></span> <span data-ttu-id="1120c-117">Pour la vidéo, le générateur de graphiques de capture utilise toujours le filtre de [convertisseur vidéo](video-renderer-filter.md) comme convertisseur par défaut.</span><span class="sxs-lookup"><span data-stu-id="1120c-117">For video, the Capture Graph Builder always uses the [Video Renderer](video-renderer-filter.md) filter as the default renderer.</span></span>

> [!Note]  
> <span data-ttu-id="1120c-118">Dans Windows XP et versions ultérieures, bien que le convertisseur de mixage vidéo (VMR) soit le convertisseur vidéo par défaut pour les méthodes [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) , il ne s’agit pas du convertisseur par défaut pour la méthode [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) .</span><span class="sxs-lookup"><span data-stu-id="1120c-118">In Windows XP and later, although the Video Mixing Renderer (VMR) is the default video renderer for [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) methods, it is not the default renderer for the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method.</span></span> <span data-ttu-id="1120c-119">Sur n’importe quelle plateforme, le générateur de graphiques de capture utilise toujours l’ancien filtre de convertisseur vidéo, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="1120c-119">On any platform, the Capture Graph Builder always uses the old Video Renderer filter unless you specify otherwise.</span></span>

 

<span data-ttu-id="1120c-120">Bien que la catégorie pin soit fournie en tant qu' **\_ \_ aperçu de la catégorie pin**, il n’est pas important de savoir si le filtre a réellement un pin de préversion ; il peut avoir une broche de port vidéo ou simplement une broche de capture.</span><span class="sxs-lookup"><span data-stu-id="1120c-120">Although the pin category is given as **PIN\_CATEGORY\_PREVIEW**, it does not matter whether the filter actually has a preview pin; it could have a video port pin or just a capture pin.</span></span> <span data-ttu-id="1120c-121">Dans les deux cas, le générateur de graphiques de capture génère automatiquement le graphique approprié.</span><span class="sxs-lookup"><span data-stu-id="1120c-121">In either case, the Capture Graph Builder automatically builds the correct graph.</span></span>

<span data-ttu-id="1120c-122">Le diagramme suivant montre le graphique le plus simple possible pour afficher un aperçu de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="1120c-122">The following diagram shows the simplest possible graph for previewing video.</span></span>

![graphique d’aperçu vidéo](images/vidcap01.png)

<span data-ttu-id="1120c-124">Dans ce diagramme, le filtre de capture a une broche d’aperçu, qui se connecte directement au convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="1120c-124">In this diagram, the capture filter has a preview pin, which connects directly to the video renderer.</span></span>

<span data-ttu-id="1120c-125">Si le filtre de capture a uniquement une broche de capture, le générateur de graphiques de capture insère un filtre [tee intelligent](smart-tee-filter.md) , qui fractionne le flux en un flux de capture et un flux d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="1120c-125">If the capture filter has only a capture pin, the Capture Graph Builder inserts a [Smart Tee](smart-tee-filter.md) filter, which splits the stream into a capture stream and a preview stream.</span></span> <span data-ttu-id="1120c-126">Cela est décrit plus en détail dans [combinaison de capture vidéo et d’aperçu](combining-video-capture-and-preview.md).</span><span class="sxs-lookup"><span data-stu-id="1120c-126">This is described in more detail in [Combining Video Capture and Preview](combining-video-capture-and-preview.md).</span></span>

<span data-ttu-id="1120c-127">Dans certains cas, le flux vidéo doit passer par le filtre de mixage de superposition.</span><span class="sxs-lookup"><span data-stu-id="1120c-127">In some cases, the video stream must go through the Overlay Mixer filter.</span></span> <span data-ttu-id="1120c-128">Si c’est le cas, la méthode [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) l’ajoute automatiquement au graphique.</span><span class="sxs-lookup"><span data-stu-id="1120c-128">If so, the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method adds it to the graph automatically.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1120c-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1120c-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1120c-130">Combinaison de la capture vidéo et de l’aperçu</span><span class="sxs-lookup"><span data-stu-id="1120c-130">Combining Video Capture and Preview</span></span>](combining-video-capture-and-preview.md)
</dt> <dt>

[<span data-ttu-id="1120c-131">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="1120c-131">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



