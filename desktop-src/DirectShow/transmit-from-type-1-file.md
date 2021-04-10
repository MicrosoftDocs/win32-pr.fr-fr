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
# <a name="transmit-from-type-1-file"></a><span data-ttu-id="4f55d-103">Transmettre à partir d’un fichier de type-1</span><span class="sxs-lookup"><span data-stu-id="4f55d-103">Transmit from Type-1 File</span></span>

<span data-ttu-id="4f55d-104">Pour transmettre un fichier de type 1 lors de l’aperçu du fichier, utilisez le graphique de filtre illustré dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="4f55d-104">To transmit a type-1 file while previewing the file, use the filter graph shown in the following diagram.</span></span>

![type-1 transmettre avec aperçu](images/dv1-transmit.png)

<span data-ttu-id="4f55d-106">Les filtres dans ce graphique sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="4f55d-106">Filters in this graph include:</span></span>

-   <span data-ttu-id="4f55d-107">Le [séparateur AVI](avi-splitter-filter.md) analyse le fichier avi.</span><span class="sxs-lookup"><span data-stu-id="4f55d-107">The [AVI Splitter](avi-splitter-filter.md) parses the AVI file.</span></span> <span data-ttu-id="4f55d-108">Pour un fichier DV de type 1, la broche de sortie fournit des exemples DV entrelacés.</span><span class="sxs-lookup"><span data-stu-id="4f55d-108">For a type-1 DV file, the output pin delivers interleaved DV samples.</span></span>
-   <span data-ttu-id="4f55d-109">Le filtre [tee de pin infini](infinite-pin-tee-filter.md) divise le DV entrelacé en un flux de transmission et un flux d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="4f55d-109">The [Infinite Pin Tee](infinite-pin-tee-filter.md) filter splits the interleaved DV into a transmit stream and a preview stream.</span></span> <span data-ttu-id="4f55d-110">Les deux flux contiennent les mêmes données entrelacées.</span><span class="sxs-lookup"><span data-stu-id="4f55d-110">Both streams contain the same interleaved data.</span></span> <span data-ttu-id="4f55d-111">(Ce graphique utilise le code PIN infini plutôt que le [tee intelligent](smart-tee-filter.md), car il n’y a aucun risque de supprimer des frames lors de la lecture d’un fichier, comme c’est le cas avec la capture en direct.)</span><span class="sxs-lookup"><span data-stu-id="4f55d-111">(This graph uses the Infinite Pin Tee instead of the [Smart Tee](smart-tee-filter.md), because there is no danger of dropping frames when reading from a file, as there is with live capture.)</span></span>
-   <span data-ttu-id="4f55d-112">Le [séparateur DV](dv-splitter-filter.md) divise le flux entrelacé en un flux vidéo DV, qui est décodé par le [décodeur vidéo DV](dv-video-decoder-filter.md), et un flux audio.</span><span class="sxs-lookup"><span data-stu-id="4f55d-112">The [DV Splitter](dv-splitter-filter.md) splits the interleaved stream into a DV video stream, which is decoded by the [DV Video Decoder](dv-video-decoder-filter.md), and an audio stream.</span></span> <span data-ttu-id="4f55d-113">Les deux flux sont rendererd pour la version préliminaire.</span><span class="sxs-lookup"><span data-stu-id="4f55d-113">Both streams are rendererd for preview.</span></span>

<span data-ttu-id="4f55d-114">Générez ce graphique comme suit :</span><span class="sxs-lookup"><span data-stu-id="4f55d-114">Build this graph as follows:</span></span>


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



1.  <span data-ttu-id="4f55d-115">Appelez [**IGraphBuilder :: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) pour ajouter le filtre source au graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="4f55d-115">Call [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) to add the source filter to the filter graph.</span></span>
2.  <span data-ttu-id="4f55d-116">Créez le séparateur AVI et le code confidentiel infini, puis ajoutez-les au graphique.</span><span class="sxs-lookup"><span data-stu-id="4f55d-116">Create the AVI Splitter and the Infinite Pin Tee, and add them to the graph.</span></span>
3.  <span data-ttu-id="4f55d-117">Appelez [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) pour connecter le filtre source au séparateur avi.</span><span class="sxs-lookup"><span data-stu-id="4f55d-117">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) to connect the source filter to the AVI Splitter.</span></span> <span data-ttu-id="4f55d-118">La spécification \_ de MediaType entrelacée pour s’assurer que la méthode échoue si le fichier source n’est pas un fichier DV de type 1.</span><span class="sxs-lookup"><span data-stu-id="4f55d-118">Specifying MEDIATYPE\_Interleaved to ensure that the method fails if the source file is not a type-1 DV file.</span></span> <span data-ttu-id="4f55d-119">Dans ce cas, vous pouvez revenir en arrière et tenter de générer un graphique de type 2 transmit à la place.</span><span class="sxs-lookup"><span data-stu-id="4f55d-119">In that case, you can back out and attempt to build a type-2 transmit graph instead.</span></span>
4.  <span data-ttu-id="4f55d-120">Appelez à nouveau **RenderStream** pour acheminer le flux entrelacé du séparateur AVI vers le code PIN tee infini</span><span class="sxs-lookup"><span data-stu-id="4f55d-120">Call **RenderStream** again to route the interleaved stream from the AVI Splitter to the Infinite Pin Tee</span></span>
5.  <span data-ttu-id="4f55d-121">Appelez RenderStream une troisième fois pour acheminer un flux du code confidentiel infini vers le filtre MSDV, pour la transmettre à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4f55d-121">Call RenderStream a third time to route one stream from the Infinite Pin Tee to the MSDV filter, for transmit to the device.</span></span>
6.  <span data-ttu-id="4f55d-122">Appelez **RenderStream** une dernière fois pour générer la section d’aperçu du graphique.</span><span class="sxs-lookup"><span data-stu-id="4f55d-122">Call **RenderStream** one last time, to build the preview section of the graph.</span></span>

<span data-ttu-id="4f55d-123">Si vous ne souhaitez pas afficher l’aperçu, connectez simplement la source du fichier au filtre MSDV :</span><span class="sxs-lookup"><span data-stu-id="4f55d-123">If you do not want preview, simply connect the file source to the MSDV filter:</span></span>


```C++
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pFileSource, 0, pDV);
```



## <a name="related-topics"></a><span data-ttu-id="4f55d-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4f55d-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f55d-125">Vidéo numérique dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="4f55d-125">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



