---
description: Capturer un fichier DV de type 1
ms.assetid: fba11e9b-4900-4b29-a0c9-702272cd7387
title: Capturer un fichier DV de type 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8098669f124bdd4c0168e3549cd8eed8e1825c47
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104556816"
---
# <a name="capture-a-type-1-dv-file"></a><span data-ttu-id="974a5-103">Capturer un fichier DV de type 1</span><span class="sxs-lookup"><span data-stu-id="974a5-103">Capture a Type-1 DV File</span></span>

<span data-ttu-id="974a5-104">Un fichier AVI DV type-1 contient un flux entrelacé unique.</span><span class="sxs-lookup"><span data-stu-id="974a5-104">A type-1 DV AVI file contains a single interleaved stream.</span></span> <span data-ttu-id="974a5-105">Pour capturer un fichier type-1 pendant l’aperçu, utilisez le graphique de filtre illustré dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="974a5-105">To capture a type-1 file while previewing, use the filter graph shown in the following diagram.</span></span>

![capture de type 1 avec aperçu](images/dv1-cap.png)

<span data-ttu-id="974a5-107">Les filtres dans ce graphique sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="974a5-107">Filters in this graph include:</span></span>

-   <span data-ttu-id="974a5-108">Le filtre [tee intelligent](smart-tee-filter.md) divise le DV entrelacé en un flux de capture et un flux d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="974a5-108">The [Smart Tee](smart-tee-filter.md) filter splits the interleaved DV into a capture stream and a preview stream.</span></span> <span data-ttu-id="974a5-109">Les deux flux contiennent les mêmes données entrelacées.</span><span class="sxs-lookup"><span data-stu-id="974a5-109">Both streams contain the same interleaved data.</span></span>
-   <span data-ttu-id="974a5-110">Le [rédacteur](file-writer-filter.md) [AVI](avi-mux-filter.md) et le writer de fichier écrivent le flux entrelacé sur le disque.</span><span class="sxs-lookup"><span data-stu-id="974a5-110">The [AVI Mux](avi-mux-filter.md) and [File Writer](file-writer-filter.md) write the interleaved stream to disk.</span></span>
-   <span data-ttu-id="974a5-111">Le [séparateur DV](dv-splitter-filter.md) divise le flux entrelacé en un flux vidéo DV et un flux audio.</span><span class="sxs-lookup"><span data-stu-id="974a5-111">The [DV Splitter](dv-splitter-filter.md) splits the interleaved stream into a DV video stream and an audio stream.</span></span> <span data-ttu-id="974a5-112">Les deux flux sont rendererd pour la version préliminaire.</span><span class="sxs-lookup"><span data-stu-id="974a5-112">Both streams are rendererd for preview.</span></span>
-   <span data-ttu-id="974a5-113">Le [décodeur vidéo DV](dv-video-decoder-filter.md) décode le flux vidéo DV pour l’aperçu.</span><span class="sxs-lookup"><span data-stu-id="974a5-113">The [DV Video Decoder](dv-video-decoder-filter.md) decodes the DV video stream for previewing.</span></span>

<span data-ttu-id="974a5-114">Générez ce graphique comme suit :</span><span class="sxs-lookup"><span data-stu-id="974a5-114">Build this graph as follows:</span></span>


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



1.  <span data-ttu-id="974a5-115">Appelez [**ICaptureGraphBuilder2 :: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) pour connecter le filtre multiplex MUX au filtre du writer de fichier.</span><span class="sxs-lookup"><span data-stu-id="974a5-115">Call [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) to connect the AVI Mux filter to the File Writer filter.</span></span>
2.  <span data-ttu-id="974a5-116">Appelez [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) avec la catégorie PIN catégorie code confidentiel \_ \_ capturer pour restituer le flux de capture.</span><span class="sxs-lookup"><span data-stu-id="974a5-116">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) with the pin category PIN\_CATEGORY\_CAPTURE to render the capture stream.</span></span> <span data-ttu-id="974a5-117">Le générateur de graphiques de capture insère automatiquement le filtre des tees intelligents.</span><span class="sxs-lookup"><span data-stu-id="974a5-117">The Capture Graph Builder automatically inserts the Smart Tee filter.</span></span>
3.  <span data-ttu-id="974a5-118">Appelez à nouveau RenderStream, mais avec l’aperçu catégorie pin catégorie PIN \_ \_ , pour afficher le flux d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="974a5-118">Call RenderStream again, but with the pin category PIN\_CATEGORY\_PREVIEW, to render the preview stream.</span></span> <span data-ttu-id="974a5-119">Ignorez cet appel si vous ne souhaitez pas afficher un aperçu de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="974a5-119">Skip this call if you do not want to preview the video.</span></span>

<span data-ttu-id="974a5-120">Pour les deux appels à RenderStream, le type de média est MEDIATYPE entrelacé, ce qui signifie qu’il s’agit d’une \_ vidéo DV entrelacée.</span><span class="sxs-lookup"><span data-stu-id="974a5-120">For both calls to RenderStream, the media type is MEDIATYPE\_Interleaved, meaning interleaved DV video.</span></span> <span data-ttu-id="974a5-121">Dans ce code, le générateur de graphiques de capture ajoute automatiquement chaque filtre requis, à l’exception du filtre de capture MSDV.</span><span class="sxs-lookup"><span data-stu-id="974a5-121">In this code, the Capture Graph Builder automatically adds every filter that is needed, except for the MSDV capture filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="974a5-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="974a5-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="974a5-123">Vidéo numérique dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="974a5-123">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



