---
description: Transmettre à partir du fichier de type 2
ms.assetid: c14c1798-aeff-44d8-a2e4-2fe4c146dfb9
title: Transmettre à partir du fichier de type 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96e15cb0b3aae5b5119739f327a84204730c9d05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952188"
---
# <a name="transmit-from-type-2-file"></a><span data-ttu-id="5c4a0-103">Transmettre à partir du fichier de type 2</span><span class="sxs-lookup"><span data-stu-id="5c4a0-103">Transmit from Type-2 File</span></span>

<span data-ttu-id="5c4a0-104">Pour transmettre un fichier de type 2 lors de l’aperçu, utilisez le graphique de filtre illustré dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="5c4a0-104">To transmit a type-2 file while previewing, use the filter graph shown in the following diagram.</span></span>

![type-2 transmettre avec la version préliminaire](images/dv2-transmit.png)

<span data-ttu-id="5c4a0-106">Un fichier de type 2 contient deux flux, un flux audio et un flux vidéo encodé au format DV.</span><span class="sxs-lookup"><span data-stu-id="5c4a0-106">A type-2 file has two streams, one audio stream and one DV-encoded video stream.</span></span> <span data-ttu-id="5c4a0-107">Ce graphique utilise le filtre [DV du multiplexeur](dv-muxer-filter.md) pour combiner les flux audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="5c4a0-107">This graph uses the [DV Muxer](dv-muxer-filter.md) filter to combine the audio and video streams.</span></span> <span data-ttu-id="5c4a0-108">Elle envoie le flux entrelacé au filtre MSDV, mais fractionne à nouveau le flux pour l’aperçu.</span><span class="sxs-lookup"><span data-stu-id="5c4a0-108">It sends the interleaved stream to the MSDV filter, but splits the stream again for preview.</span></span>

<span data-ttu-id="5c4a0-109">Générez ce graphique comme suit :</span><span class="sxs-lookup"><span data-stu-id="5c4a0-109">Build this graph as follows:</span></span>


```C++
// Add the DV Mux filter to the graph.
IBaseFilter *pDVMux;
hr = CoCreateInstance(CLSID_DVMux, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pDVMux));
hr = pGraph->AddFilter(pDVMux, L"DV Mux");

// Add the File Source filter to the graph.
IBaseFilter *pFileSource;
hr = pGraph->AddSourceFilter(L"C:\\Example2.avi", L"Source", 
    &pFileSource);

hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pDVMux);
hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pDVMux);

// Add the Infinite Pin Tee filter to the graph.
IBaseFilter *pTee;
hr = CoCreateInstance(CLSID_InfTee, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pTee));
hr = pGraph->AddFilter(pTee, L"Tee");

hr = pBuilder->RenderStream(0, 0, pDVMux, 0, pTee);
hr = pBuilder->RenderStream(0, 0, pTee, 0, pDV);
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pTee, 0, 0);
```



<span data-ttu-id="5c4a0-110">Ce code effectue plusieurs appels à **RenderStream**:</span><span class="sxs-lookup"><span data-stu-id="5c4a0-110">This code makes several calls to **RenderStream**:</span></span>

<span data-ttu-id="5c4a0-111">Les deux premiers connectent le filtre source au séparateur AVI et le séparateur AVI au DV Mux.</span><span class="sxs-lookup"><span data-stu-id="5c4a0-111">The first two connect the source filter to the AVI Splitter and the AVI Splitter to the DV Mux.</span></span> <span data-ttu-id="5c4a0-112">Dans le premier appel, le générateur de graphiques de capture ajoute automatiquement le séparateur AVI au graphique et connecte l’une des broches de sortie du séparateur AVI au DV Mux.</span><span class="sxs-lookup"><span data-stu-id="5c4a0-112">In the first call, the Capture Graph Builder automatically adds the AVI Splitter to the graph and connects one of the AVI Splitter's output pins to the DV Mux.</span></span> <span data-ttu-id="5c4a0-113">Dans le deuxième appel, le générateur de graphiques de capture trouve la deuxième broche de sortie du séparateur AVI et le connecte au DV Mux.</span><span class="sxs-lookup"><span data-stu-id="5c4a0-113">In the second call, the Capture Graph Builder finds the AVI Splitter's second output pin and connects that to the DV Mux.</span></span>

<span data-ttu-id="5c4a0-114">Le troisième appel à **RenderStream** connecte la DV du multiplexeur au filtre tee du pin infini.</span><span class="sxs-lookup"><span data-stu-id="5c4a0-114">The third call to **RenderStream** connects the DV Muxer to the Infinite Pin Tee filter.</span></span> <span data-ttu-id="5c4a0-115">L’appel suivant connecte un flux à partir du code confidentiel infini au filtre de capture MSDV.</span><span class="sxs-lookup"><span data-stu-id="5c4a0-115">The next call connects one stream from the Infinite Pin Tee to the MSDV capture filter.</span></span> <span data-ttu-id="5c4a0-116">Ce flux est transmis à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5c4a0-116">This stream is transmitted to the device.</span></span> <span data-ttu-id="5c4a0-117">Le dernier appel à **RenderStream** génère la section d’aperçu du graphique.</span><span class="sxs-lookup"><span data-stu-id="5c4a0-117">The last call to **RenderStream** builds the preview section of the graph.</span></span>

<span data-ttu-id="5c4a0-118">Si vous ne souhaitez pas afficher un aperçu lors de la transmission, vous pouvez omettre le tee-pin infini et connecter simplement le multiplexeur multiplex au filtre MSDV :</span><span class="sxs-lookup"><span data-stu-id="5c4a0-118">If you do not want to preview while transmitting, you can omit the Infinite Pin Tee, and simply connect the DV Mux to the MSDV filter:</span></span>


```C++
hr = pBuilder->RenderStream(0, 0, pDVMux, 0, pDV);
```



## <a name="related-topics"></a><span data-ttu-id="5c4a0-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5c4a0-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c4a0-120">Vidéo numérique dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="5c4a0-120">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



