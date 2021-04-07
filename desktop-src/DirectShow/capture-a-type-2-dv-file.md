---
description: Capturer un fichier DV de type 2
ms.assetid: c7d49c86-1b5d-43bf-98a5-78b297682375
title: Capturer un fichier DV de type 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b919928a4c02ce9e3f3f3e6fcf3d2cd376f880a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845850"
---
# <a name="capture-a-type-2-dv-file"></a><span data-ttu-id="b0f39-103">Capturer un fichier DV de type 2</span><span class="sxs-lookup"><span data-stu-id="b0f39-103">Capture a Type-2 DV File</span></span>

<span data-ttu-id="b0f39-104">Un fichier AVI DV type-2 a deux flux, un qui contient une vidéo DV et un autre qui contient des données audio.</span><span class="sxs-lookup"><span data-stu-id="b0f39-104">A type-2 DV AVI file has two streams, one that contains DV video and another that contains audio.</span></span> <span data-ttu-id="b0f39-105">Pour capturer un fichier de type 2 lors de l’aperçu, utilisez le graphique de filtre illustré dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="b0f39-105">To capture a type-2 file while previewing, use the filter graph shown in the following diagram.</span></span>

![capture de type 2 avec aperçu](images/dv2-cap.png)

<span data-ttu-id="b0f39-107">Ce graphique est quasiment identique au graphique pour la capture de type 1 (voir [capture d’un fichier DV de type 1](capture-a-type-1-dv-file.md)).</span><span class="sxs-lookup"><span data-stu-id="b0f39-107">This graph is almost the same as the graph for type-1 capture (see [Capture a Type-1 DV File](capture-a-type-1-dv-file.md)).</span></span> <span data-ttu-id="b0f39-108">Toutefois, le flux de capture traverse le filtre de [séparateur DV](dv-splitter-filter.md) avant d’atteindre le filtre [multiplex MUX](avi-mux-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="b0f39-108">However, the capture stream goes through the [DV Splitter](dv-splitter-filter.md) filter before reaching the [AVI Mux](avi-mux-filter.md) filter.</span></span> <span data-ttu-id="b0f39-109">Le multiplexeur de données AVI reçoit donc deux flux, un flux audio et un flux vidéo encodé au format DV.</span><span class="sxs-lookup"><span data-stu-id="b0f39-109">The AVI Mux therefore receives two streams, an audio stream and a DV-encoded video stream.</span></span>

<span data-ttu-id="b0f39-110">Générez ce graphique comme suit :</span><span class="sxs-lookup"><span data-stu-id="b0f39-110">Build this graph as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)
IBaseFilter           *pAviMux    // Avi Mux filter.
IBaseFilter           *pDVSplit;  // DV Splitter

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Create the DV Splitter and add it to the filter graph.
hr = CoCreateInstance(CLSID_DVSplitter, 0, CLSCTX_INPROC_SERVER,
    IID_IBaseFilter, reinterpret_cast<void**>)(&pDVSplit));
hr = pGraph->AddFilter(pDVSplit, L"DV Splitter");

// Create the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi,
    OLESTR("C:\\Example2.avi"), &pAviMux, 0);

// Connect the capture pin to the DV Splitter, and render one stream from
// the DV Splitter to the AVI Mux. 
hr = pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Interleaved, 
    pDV, pDVSplit, pAviMux);

// Render the other stream from the DV splitter to the AVI Mux.
hr = pBuilder->RenderStream(0, 0, pDVSplit, 0, pAviMux);

// Render the preview stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Interleaved, 
    pDV, 0, 0);

// Remember to release all interfaces.
```



1.  <span data-ttu-id="b0f39-111">Créez le séparateur DV et ajoutez-le au graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="b0f39-111">Create the DV Splitter and add it to the filter graph.</span></span>
2.  <span data-ttu-id="b0f39-112">Appelez [**ICaptureGraphBuilder2 :: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) pour connecter le filtre multiplex MUX au filtre du writer de fichier.</span><span class="sxs-lookup"><span data-stu-id="b0f39-112">Call [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) to connect the AVI Mux filter to the File Writer filter.</span></span>
3.  <span data-ttu-id="b0f39-113">Appelez [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) pour connecter le filtre de capture MSDV au séparateur DV.</span><span class="sxs-lookup"><span data-stu-id="b0f39-113">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) to connect the MSDV capture filter to the DV Splitter.</span></span> <span data-ttu-id="b0f39-114">Cet appel connecte également l’une des broches de sortie du séparateur DV à AVI Mux.</span><span class="sxs-lookup"><span data-stu-id="b0f39-114">This call also connects one of the DV Splitter's output pins to the AVI Mux.</span></span>
4.  <span data-ttu-id="b0f39-115">Appelez à nouveau RenderStream pour connecter l’autre code confidentiel DV au multiplexeur AVI.</span><span class="sxs-lookup"><span data-stu-id="b0f39-115">Call RenderStream again to connect the DV Splitter's other pin to the AVI Mux.</span></span>
5.  <span data-ttu-id="b0f39-116">Appelez RenderStream une troisième fois pour afficher le flux d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="b0f39-116">Call RenderStream a third time to render the preview stream.</span></span> <span data-ttu-id="b0f39-117">Ignorez cette étape si vous ne souhaitez pas afficher un aperçu de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="b0f39-117">Skip this step if do not want to preview the video.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0f39-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b0f39-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0f39-119">Vidéo numérique dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="b0f39-119">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



