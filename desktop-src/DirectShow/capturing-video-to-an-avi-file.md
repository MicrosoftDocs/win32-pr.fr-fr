---
description: Capture vidéo dans un fichier AVI
ms.assetid: 0f5f4a82-4a2e-4c48-b201-bda641cb8619
title: Capture vidéo dans un fichier AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86504e9ce149f495e1ea31664f56382340d33887
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104551755"
---
# <a name="capturing-video-to-an-avi-file"></a><span data-ttu-id="6078a-103">Capture vidéo dans un fichier AVI</span><span class="sxs-lookup"><span data-stu-id="6078a-103">Capturing Video to an AVI File</span></span>

<span data-ttu-id="6078a-104">L’illustration suivante montre le graphique le plus simple possible pour capturer des vidéos dans un fichier AVI.</span><span class="sxs-lookup"><span data-stu-id="6078a-104">The following illustration shows the simplest possible graph for capturing video to an AVI file.</span></span>

![graphique de capture vidéo AVI](images/vidcap02.png)

<span data-ttu-id="6078a-106">Le filtre [multiplex MUX](avi-mux-filter.md) prend le flux vidéo de la broche de capture et le reporte dans un flux avi.</span><span class="sxs-lookup"><span data-stu-id="6078a-106">The [AVI Mux](avi-mux-filter.md) filter takes the video stream from the capture pin and packages it into an AVI stream.</span></span> <span data-ttu-id="6078a-107">Un flux audio peut également être connecté au filtre multiplex MUX, auquel cas le multiplexeur entrelace les deux flux.</span><span class="sxs-lookup"><span data-stu-id="6078a-107">An audio stream could also be connected to the AVI Mux filter, in which case the mux would interleave the two streams.</span></span> <span data-ttu-id="6078a-108">Le filtre du [writer de fichier](file-writer-filter.md) écrit le flux AVI sur le disque.</span><span class="sxs-lookup"><span data-stu-id="6078a-108">The [File Writer](file-writer-filter.md) filter writes the AVI stream to disk.</span></span>

<span data-ttu-id="6078a-109">Pour générer le graphique, commencez par appeler la méthode [**ICaptureGraphBuilder2 :: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) , comme suit :</span><span class="sxs-lookup"><span data-stu-id="6078a-109">To build the graph, start by calling the [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) method, as follows:</span></span>


```C++
IBaseFilter *pMux;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Avi,  // Specifies AVI for the target file.
    L"C:\\Example.avi", // File name.
    &pMux,              // Receives a pointer to the mux.
    NULL);              // (Optional) Receives a pointer to the file sink.
```



<span data-ttu-id="6078a-110">Le premier paramètre spécifie le type de fichier, en l’occurrence AVI.</span><span class="sxs-lookup"><span data-stu-id="6078a-110">The first parameter specifies the file type — in this case, AVI.</span></span> <span data-ttu-id="6078a-111">Le deuxième paramètre donne le nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="6078a-111">The second parameter gives the file name.</span></span> <span data-ttu-id="6078a-112">Pour AVI, la méthode SetOutputFileName cocrée le filtre multiplex MUX et le filtre de writer de fichier et les ajoute au graphique.</span><span class="sxs-lookup"><span data-stu-id="6078a-112">For AVI, the SetOutputFileName method cocreates the AVI Mux filter and the File Writer filter and adds them to the graph.</span></span> <span data-ttu-id="6078a-113">Il définit également le nom de fichier sur le filtre du writer de fichier, en appelant la méthode [**IFileSinkFilter :: SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) et connecte les deux filtres.</span><span class="sxs-lookup"><span data-stu-id="6078a-113">It also sets the file name on the File Writer filter, by calling the [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) method, and connects the two filters.</span></span> <span data-ttu-id="6078a-114">La méthode retourne un pointeur vers le multiplexeur de la valeur AVI dans le troisième paramètre.</span><span class="sxs-lookup"><span data-stu-id="6078a-114">The method returns a pointer to the AVI Mux in the third parameter.</span></span> <span data-ttu-id="6078a-115">Le cas échéant, elle retourne un pointeur vers l’interface [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) dans le quatrième paramètre.</span><span class="sxs-lookup"><span data-stu-id="6078a-115">Optionally, it returns a pointer to the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface in the fourth parameter.</span></span> <span data-ttu-id="6078a-116">Si vous n’avez pas besoin de cette interface, vous pouvez définir ce paramètre sur la **valeur null**, comme indiqué dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="6078a-116">If you don't need this interface, you can set this parameter to **NULL**, as shown in the previous example.</span></span>

<span data-ttu-id="6078a-117">Ensuite, appelez la méthode [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) pour connecter le filtre de capture à AVI MUX, comme suit :</span><span class="sxs-lookup"><span data-stu-id="6078a-117">Next, call the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method to connect the capture filter to the AVI Mux, as follows:</span></span>


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                  // Capture filter.
    NULL,                  // Intermediate filter (optional).
    pMux);                 // Mux or file sink filter.

// Release the mux filter.
pMux->Release();
```



<span data-ttu-id="6078a-118">Le premier paramètre donne la catégorie pin, qui est la \_ \_ capture de catégorie pin pour la capture.</span><span class="sxs-lookup"><span data-stu-id="6078a-118">The first parameter gives the pin category, which is PIN\_CATEGORY\_CAPTURE for capture.</span></span> <span data-ttu-id="6078a-119">Le deuxième paramètre donne le type de média.</span><span class="sxs-lookup"><span data-stu-id="6078a-119">The second parameter gives the media type.</span></span> <span data-ttu-id="6078a-120">Le troisième paramètre est un pointeur vers l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) du filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="6078a-120">The third parameter is a pointer to the capture filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="6078a-121">Le quatrième paramètre est facultatif ; elle vous permet d’acheminer le flux vidéo via un filtre intermédiaire, tel qu’un encodeur, avant de le passer au filtre Mux.</span><span class="sxs-lookup"><span data-stu-id="6078a-121">The fourth parameter is optional; it lets you route the video stream through an intermediate filter, such as an encoder, before passing it to the mux filter.</span></span> <span data-ttu-id="6078a-122">Sinon, affectez la valeur **null** à ce paramètre, comme indiqué dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="6078a-122">Otherwise, set this parameter to **NULL**, as shown in the previous example.</span></span> <span data-ttu-id="6078a-123">Le cinquième paramètre est le pointeur vers le filtre Mux.</span><span class="sxs-lookup"><span data-stu-id="6078a-123">The fifth parameter is the pointer to the mux filter.</span></span> <span data-ttu-id="6078a-124">Ce pointeur est obtenu en appelant la méthode SetOutputFileName.</span><span class="sxs-lookup"><span data-stu-id="6078a-124">This pointer is obtained by calling the SetOutputFileName method.</span></span>

<span data-ttu-id="6078a-125">Pour capturer l’audio, appelez RenderStream avec le type de média \_ audio MediaType.</span><span class="sxs-lookup"><span data-stu-id="6078a-125">To capture audio, call RenderStream with the media type MEDIATYPE\_Audio.</span></span> <span data-ttu-id="6078a-126">Si vous capturez des données audio et vidéo à partir de deux appareils distincts, il est judicieux de faire en sorte que le flux audio soit le flux principal.</span><span class="sxs-lookup"><span data-stu-id="6078a-126">If you are capturing audio and video from two separate devices, it is a good idea to make the audio stream the master stream.</span></span> <span data-ttu-id="6078a-127">Cela permet d’éviter la dérive entre les deux flux, car le filtre multiplex MUX ajuste la vitesse de lecture du flux vidéo pour qu’elle corresponde au flux audio.</span><span class="sxs-lookup"><span data-stu-id="6078a-127">This helps to prevent drift between the two streams, because the AVI Mux filter adjust the playback rate on the video stream to match the audio stream.</span></span> <span data-ttu-id="6078a-128">Pour définir le flux principal, appelez la méthode [**IConfigAviMux :: SetMasterStream**](/windows/desktop/api/Strmif/nf-strmif-iconfigavimux-setmasterstream) sur le filtre multiplex Mux :</span><span class="sxs-lookup"><span data-stu-id="6078a-128">To set the master stream, call the [**IConfigAviMux::SetMasterStream**](/windows/desktop/api/Strmif/nf-strmif-iconfigavimux-setmasterstream) method on the AVI Mux filter:</span></span>


```C++
IConfigAviMux *pConfigMux = NULL;
hr = pMux->QueryInterface(IID_IConfigAviMux, (void**)&pConfigMux);
if (SUCCEEDED(hr))
{
    pConfigMux->SetMasterStream(1);
    pConfigMux->Release();
}
```



<span data-ttu-id="6078a-129">Le paramètre de SetMasterStream est le numéro du flux, qui est déterminé par l’ordre dans lequel vous appelez RenderStream.</span><span class="sxs-lookup"><span data-stu-id="6078a-129">The parameter to SetMasterStream is the stream number, which is determined by the order in which you call RenderStream.</span></span> <span data-ttu-id="6078a-130">Par exemple, si vous appelez d’abord RenderStream pour la vidéo, puis pour l’audio, la vidéo est Stream 0 et l’audio est Stream 1.</span><span class="sxs-lookup"><span data-stu-id="6078a-130">For example, if you call RenderStream first for video and then for audio, the video is stream 0 and the audio is stream 1.</span></span>

<span data-ttu-id="6078a-131">Vous pouvez également définir la manière dont le filtre multiplex MUX entrelace les flux audio et vidéo, en appelant la méthode [**IConfigInterleaving ::p ut \_ mode**](/windows/desktop/api/Strmif/nf-strmif-iconfiginterleaving-put_mode) .</span><span class="sxs-lookup"><span data-stu-id="6078a-131">You may also want to set how the AVI Mux filter interleaves the audio and video streams, by calling the [**IConfigInterleaving::put\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iconfiginterleaving-put_mode) method.</span></span>


```C++
IConfigInterleaving *pInterleave = NULL;
hr = pMux->QueryInterface(IID_IConfigInterleaving, (void**)&pInterleave);
if (SUCCEEDED(hr))
{
    pInterleave->put_Mode(INTERLEAVE_CAPTURE);
    pInterleave->Release();
}
```



<span data-ttu-id="6078a-132">Avec l’indicateur ENTRELACement \_ , le multiplexeur de contenu AVI effectue l’entrelacement à un débit adapté à la capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="6078a-132">With the INTERLEAVE\_CAPTURE flag, the AVI Mux performs interleaving at a rate that is suitable for video capture.</span></span> <span data-ttu-id="6078a-133">Vous pouvez également utiliser l’ENTRELACement \_ aucun, ce qui signifie qu’il n’y a pas d’entrelacement. le multiplexeur de données AVI écrira simplement les données dans l’ordre dans lequel elles arrivent.</span><span class="sxs-lookup"><span data-stu-id="6078a-133">You can also use INTERLEAVE\_NONE, which means no interleaving — the AVI Mux will simply write the data in the order that it arrives.</span></span> <span data-ttu-id="6078a-134">L’indicateur d’ENTRELACement \_ complet signifie que le multiplexeur de contenu AVI effectue un entrelacement complet. Toutefois, ce mode est moins adapté à la capture vidéo, car il requiert le plus de surentendus.</span><span class="sxs-lookup"><span data-stu-id="6078a-134">The INTERLEAVE\_FULL flag means the AVI Mux performs full interleaving; however, this mode is less suitable for video capture because it requires the most overheard.</span></span>

<span data-ttu-id="6078a-135">Encodage du flux vidéo</span><span class="sxs-lookup"><span data-stu-id="6078a-135">Encoding the Video Stream</span></span>

<span data-ttu-id="6078a-136">Vous pouvez encoder le flux vidéo en insérant un filtre d’encodeur entre le filtre de capture et le filtre multiplex Mux.</span><span class="sxs-lookup"><span data-stu-id="6078a-136">You can encode the video stream by inserting an encoder filter between the capture filter and the AVI Mux filter.</span></span> <span data-ttu-id="6078a-137">Utilisez l' [énumérateur de périphérique système](system-device-enumerator.md) ou le [Mappeur de filtre](filter-mapper.md) pour sélectionner un filtre d’encodeur.</span><span class="sxs-lookup"><span data-stu-id="6078a-137">Use the [System Device Enumerator](system-device-enumerator.md) or the [Filter Mapper](filter-mapper.md) to select an encoder filter.</span></span> <span data-ttu-id="6078a-138">(Pour plus d’informations, consultez [énumération d’appareils et de filtres](enumerating-devices-and-filters.md).)</span><span class="sxs-lookup"><span data-stu-id="6078a-138">(For more information, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).)</span></span>

<span data-ttu-id="6078a-139">Spécifiez le filtre d’encodeur en tant que quatrième paramètre de RenderStream, affiché en gras dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="6078a-139">Specify the encoder filter as the fourth parameter to RenderStream, shown in bold in the following example:</span></span>


```C++
IBaseFilter *pEncoder;
/* Create the encoder filter (not shown). */
// Add it to the filter graph.
pGraph->AddFilter(pEncoder, L"Encoder");

/* Call SetOutputFileName as shown previously. */

// Render the stream.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, 
    pCap, 
pEncoder, pMux);
pEncoder->Release();
```



<span data-ttu-id="6078a-140">Le filtre d’encodeur peut prendre en charge les [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) ou d’autres interfaces pour définir les paramètres d’encodage.</span><span class="sxs-lookup"><span data-stu-id="6078a-140">The encoder filter might support [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) or other interfaces for setting the encoding parameters.</span></span> <span data-ttu-id="6078a-141">Pour obtenir la liste des interfaces possibles, consultez [encodage et décodage des interfaces](file-encoding-and-decoding-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="6078a-141">For a list of possible interfaces, see [File Encoding and Decoding Interfaces](file-encoding-and-decoding-interfaces.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6078a-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6078a-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6078a-143">Capture vidéo dans un fichier</span><span class="sxs-lookup"><span data-stu-id="6078a-143">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



