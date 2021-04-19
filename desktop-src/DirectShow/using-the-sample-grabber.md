---
description: L’exemple de filtre d’accrochage est un filtre de transformation qui peut être utilisé pour récupérer des échantillons de média à partir d’un flux lorsqu’ils passent par le graphique de filtre.
ms.assetid: ec0e367e-9ef9-4de6-9132-b462c233bc98
title: Utilisation de l’exemple d’accrochage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4886c796691e83e02b58ddea129d60d5004c9f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535445"
---
# <a name="using-the-sample-grabber"></a><span data-ttu-id="3eb51-103">Utilisation de l’exemple d’accrochage</span><span class="sxs-lookup"><span data-stu-id="3eb51-103">Using the Sample Grabber</span></span>

<span data-ttu-id="3eb51-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="3eb51-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="3eb51-105">L’exemple de filtre d' [**accrochage**](sample-grabber-filter.md) est un filtre de transformation qui peut être utilisé pour récupérer des échantillons de média à partir d’un flux lorsqu’ils passent par le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="3eb51-105">The [**Sample Grabber**](sample-grabber-filter.md) filter is a transform filter that can be used to grab media samples from a stream as they pass through the filter graph.</span></span>

<span data-ttu-id="3eb51-106">Si vous souhaitez simplement récupérer une image bitmap à partir d’un fichier vidéo, il est plus facile d’utiliser l’objet [MediaDet (Media DETECTER)](media-detector--mediadet.md) .</span><span class="sxs-lookup"><span data-stu-id="3eb51-106">If you simply want to grab a bitmap from a video file, it is easier to use the [Media Detector (MediaDet)](media-detector--mediadet.md) object.</span></span> <span data-ttu-id="3eb51-107">Pour plus d’informations, consultez [saisie d’un cadre d’affiche](grabbing-a-poster-frame.md) .</span><span class="sxs-lookup"><span data-stu-id="3eb51-107">See [Grabbing a Poster Frame](grabbing-a-poster-frame.md) for details.</span></span> <span data-ttu-id="3eb51-108">Toutefois, cette accroche est plus souple, car elle fonctionne avec presque n’importe quel type de média (consultez [**ISampleGrabber :: SetMediaType**](isamplegrabber-setmediatype.md) pour les rares exceptions) et offre davantage de contrôle à l’application.</span><span class="sxs-lookup"><span data-stu-id="3eb51-108">The Sample Grabber is more flexible, however, because it works with nearly any media type (see [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) for the few exceptions), and offers more control to the application.</span></span>

-   [<span data-ttu-id="3eb51-109">Créer le gestionnaire de graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="3eb51-109">Create the Filter Graph Manager</span></span>](#create-the-filter-graph-manager)
-   [<span data-ttu-id="3eb51-110">Ajouter l’exemple d’accrochage au graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="3eb51-110">Add the Sample Grabber to the Filter Graph</span></span>](#add-the-sample-grabber-to-the-filter-graph)
-   [<span data-ttu-id="3eb51-111">Définir le type de média</span><span class="sxs-lookup"><span data-stu-id="3eb51-111">Set the Media Type</span></span>](#set-the-media-type)
-   [<span data-ttu-id="3eb51-112">Générer le graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="3eb51-112">Build the Filter Graph</span></span>](#build-the-filter-graph)
-   [<span data-ttu-id="3eb51-113">Exécuter le graphique</span><span class="sxs-lookup"><span data-stu-id="3eb51-113">Run the Graph</span></span>](#run-the-graph)
-   [<span data-ttu-id="3eb51-114">Extraire l’exemple</span><span class="sxs-lookup"><span data-stu-id="3eb51-114">Grab the Sample</span></span>](#grab-the-sample)
-   [<span data-ttu-id="3eb51-115">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="3eb51-115">Example Code</span></span>](#example-code)
-   [<span data-ttu-id="3eb51-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3eb51-116">Related topics</span></span>](#related-topics)

## <a name="create-the-filter-graph-manager"></a><span data-ttu-id="3eb51-117">Créer le gestionnaire de graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="3eb51-117">Create the Filter Graph Manager</span></span>

<span data-ttu-id="3eb51-118">Pour commencer, créez le [Gestionnaire de graphique de filtre](filter-graph-manager.md) et la requête pour les interfaces [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) et [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) .</span><span class="sxs-lookup"><span data-stu-id="3eb51-118">To start, create the [Filter Graph Manager](filter-graph-manager.md) and query for the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) and [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interfaces.</span></span>


```C++
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEventEx *pEvent = NULL;


    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER,IID_PPV_ARGS(&pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pEvent));
    if (FAILED(hr))
    {
        goto done;
    }
```





## <a name="add-the-sample-grabber-to-the-filter-graph"></a><span data-ttu-id="3eb51-119">Ajouter l’exemple d’accrochage au graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="3eb51-119">Add the Sample Grabber to the Filter Graph</span></span>

<span data-ttu-id="3eb51-120">Créez une instance de l’exemple de filtre d’accrochage et Addit dans le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="3eb51-120">Create an instance of the Sample Grabber filter and addit to the filter graph.</span></span> <span data-ttu-id="3eb51-121">Interrogez l’exemple de filtre d’accrochage pour l’interface [**ISampleGrabber**](isamplegrabber.md) .</span><span class="sxs-lookup"><span data-stu-id="3eb51-121">Query the Sample Grabber filter for the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span>


```C++
    IBaseFilter *pGrabberF = NULL;
    ISampleGrabber *pGrabber = NULL;


    // Create the Sample Grabber filter.
    hr = CoCreateInstance(CLSID_SampleGrabber, NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pGrabberF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pGrabberF, L&quot;Sample Grabber&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabberF->QueryInterface(IID_PPV_ARGS(&pGrabber));
    if (FAILED(hr))
    {
        goto done;
    }
```





## <a name="set-the-media-type"></a><span data-ttu-id="3eb51-122">Définir le type de média</span><span class="sxs-lookup"><span data-stu-id="3eb51-122">Set the Media Type</span></span>

<span data-ttu-id="3eb51-123">Lorsque vous créez pour la première fois la accroche, elle n’a pas de type de média préféré.</span><span class="sxs-lookup"><span data-stu-id="3eb51-123">When you first create the Sample Grabber, it has no preferred media type.</span></span> <span data-ttu-id="3eb51-124">Cela signifie que vous pouvez vous connecter à presque n’importe quel filtre dans le graphique, mais que vous n’avez aucun contrôle sur le type de données qu’il a reçu.</span><span class="sxs-lookup"><span data-stu-id="3eb51-124">This means you can connect to almost any filter in the graph, but you would have no control over the type of data that it received.</span></span> <span data-ttu-id="3eb51-125">Avant de générer le reste du graphique, par conséquent, vous devez définir un type de média pour la accroche d’échantillon, en appelant la méthode [**ISampleGrabber :: SetMediaType**](isamplegrabber-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="3eb51-125">Before building the rest of the graph, therefore, you must set a media type for the Sample Grabber, by calling the [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) method.</span></span>

<span data-ttu-id="3eb51-126">Lorsque l’accrochage de l’exemple se connecte, il compare ce type de média au type de média proposé par l’autre filtre.</span><span class="sxs-lookup"><span data-stu-id="3eb51-126">When the Sample Grabber connects, it will compare this media type against the media type offered by the other filter.</span></span> <span data-ttu-id="3eb51-127">Les seuls champs qu’il vérifie sont le type, le sous-type et le type de format principaux.</span><span class="sxs-lookup"><span data-stu-id="3eb51-127">The only fields that it checks are the major type, subtype, and format type.</span></span> <span data-ttu-id="3eb51-128">Pour l’une de ces valeurs, la valeur de GUID \_ null signifie « accepter n’importe quelle valeur ».</span><span class="sxs-lookup"><span data-stu-id="3eb51-128">For any of these, the value GUID\_NULL means "accept any value."</span></span> <span data-ttu-id="3eb51-129">La plupart du temps, vous voudrez définir le type et le sous-type principaux.</span><span class="sxs-lookup"><span data-stu-id="3eb51-129">Most of the time, you will want to set the major type and subtype.</span></span> <span data-ttu-id="3eb51-130">Par exemple, le code suivant spécifie une vidéo RGB 24 bits non compressée :</span><span class="sxs-lookup"><span data-stu-id="3eb51-130">For example, the following code specifies uncompressed 24-bit RGB video:</span></span>


```C++
    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(mt));
    mt.majortype = MEDIATYPE_Video;
    mt.subtype = MEDIASUBTYPE_RGB24;

    hr = pGrabber->SetMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }
```



## <a name="build-the-filter-graph"></a><span data-ttu-id="3eb51-131">Générer le graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="3eb51-131">Build the Filter Graph</span></span>

<span data-ttu-id="3eb51-132">Vous pouvez maintenant créer le reste du graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="3eb51-132">Now you can build the rest of the filter graph.</span></span> <span data-ttu-id="3eb51-133">Étant donné que l’exemple d’accrochage se connecte uniquement à l’aide du type de média que vous avez spécifié, vous pouvez ainsi tirer parti des mécanismes de [connexion intelligente](intelligent-connect.md) du gestionnaire de graphique de filtre lorsque vous générez le graphique.</span><span class="sxs-lookup"><span data-stu-id="3eb51-133">Because the Sample Grabber will only connect using the media type you have specified, this lets you take advantage of the Filter Graph Manager's [Intelligent Connect](intelligent-connect.md) mechanisms when you build the graph.</span></span>

<span data-ttu-id="3eb51-134">Par exemple, si vous avez spécifié une vidéo non compressée, vous pouvez connecter un filtre source à la accroche d’échantillon, et le gestionnaire de graphes de filtre ajoutera automatiquement l’analyseur de fichiers et le décodeur.</span><span class="sxs-lookup"><span data-stu-id="3eb51-134">For example, if you specified uncompressed video, you can connect a source filter to the Sample Grabber, and the Filter Graph Manager will automatically add the file parser and the decoder.</span></span> <span data-ttu-id="3eb51-135">L’exemple suivant utilise la fonction d’assistance ConnectFilters, qui est indiquée dans [connecter deux filtres](connect-two-filters.md):</span><span class="sxs-lookup"><span data-stu-id="3eb51-135">The following example uses the ConnectFilters helper function, which is listed in [Connect Two Filters](connect-two-filters.md):</span></span>


```C++
    IBaseFilter *pSourceF = NULL;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;


    hr = pGraph->AddSourceFilter(pszVideoFile, L&quot;Source&quot;, &pSourceF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSourceF->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = ConnectFilters(pGraph, pPin, pGrabberF);
        SafeRelease(&pPin);
        if (SUCCEEDED(hr))
        {
            break;
        }
    }

    if (FAILED(hr))
    {
        goto done;
    }
```





<span data-ttu-id="3eb51-136">L’échantillon est un filtre de transformation, donc la broche de sortie doit être connectée à un autre filtre.</span><span class="sxs-lookup"><span data-stu-id="3eb51-136">The Sample Grabber is a transform filter, so the output pin must be connected to another filter.</span></span> <span data-ttu-id="3eb51-137">Souvent, vous pouvez simplement ignorer les exemples une fois que vous avez fini de les utiliser.</span><span class="sxs-lookup"><span data-stu-id="3eb51-137">Often, you may simply want to discard the samples after you are done with them.</span></span> <span data-ttu-id="3eb51-138">Dans ce cas, connectez l’exemple d’accrochage au [**filtre de convertisseur null**](null-renderer-filter.md), qui ignore les données qu’il reçoit.</span><span class="sxs-lookup"><span data-stu-id="3eb51-138">In that case, connect the Sample Grabber to the [**Null Renderer Filter**](null-renderer-filter.md), which discards the data that it receives.</span></span>

<span data-ttu-id="3eb51-139">L’exemple suivant connecte l’exemple d’accrochage au filtre de convertisseur NULL :</span><span class="sxs-lookup"><span data-stu-id="3eb51-139">The following example connects the Sample Grabber to the Null Renderer filter:</span></span>


```C++
    IBaseFilter *pNullF = NULL;


    hr = CoCreateInstance(CLSID_NullRenderer, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pNullF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pNullF, L&quot;Null Filter&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConnectFilters(pGraph, pGrabberF, pNullF);
    if (FAILED(hr))
    {
        goto done;
    }
```





<span data-ttu-id="3eb51-140">Sachez que le placement de l’échantillon entre un décodeur vidéo et le convertisseur vidéo peut considérablement nuire aux performances de rendu.</span><span class="sxs-lookup"><span data-stu-id="3eb51-140">Be aware that placing the Sample Grabber between a video decoder and the video renderer can significantly hurt rendering performance.</span></span> <span data-ttu-id="3eb51-141">L’exemple d’accrochage est un filtre de transfert sur place, ce qui signifie que la mémoire tampon de sortie est la même que la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3eb51-141">The Sample Grabber is a trans-in-place filter, which means the output buffer is the same as the input buffer.</span></span> <span data-ttu-id="3eb51-142">Pour le rendu vidéo, la mémoire tampon de sortie est susceptible de se trouver sur la carte graphique, où les opérations de lecture sont beaucoup plus lentes, par rapport aux opérations de lecture dans la mémoire principale.</span><span class="sxs-lookup"><span data-stu-id="3eb51-142">For video rendering, the output buffer is likely to be located on the graphics card, where read operations are much slower, compared with read operations in main memory.</span></span>

## <a name="run-the-graph"></a><span data-ttu-id="3eb51-143">Exécuter le graphique</span><span class="sxs-lookup"><span data-stu-id="3eb51-143">Run the Graph</span></span>

<span data-ttu-id="3eb51-144">L’exemple de la accroche fonctionne dans l’un des deux modes suivants :</span><span class="sxs-lookup"><span data-stu-id="3eb51-144">The Sample Grabber operates in one of two modes:</span></span>

-   <span data-ttu-id="3eb51-145">Le mode de mise en mémoire tampon effectue une copie de chaque exemple avant de transmettre l’exemple en aval.</span><span class="sxs-lookup"><span data-stu-id="3eb51-145">Buffering mode makes a copy of each sample before delivering the sample downstream.</span></span>
-   <span data-ttu-id="3eb51-146">Le mode de rappel appelle une fonction de rappel définie par l’application sur chaque échantillon.</span><span class="sxs-lookup"><span data-stu-id="3eb51-146">Callback mode invokes an application-defined callback function on each sample.</span></span>

<span data-ttu-id="3eb51-147">Cet article décrit le mode de mise en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="3eb51-147">This article describes buffering mode.</span></span> <span data-ttu-id="3eb51-148">(Avant d’utiliser le mode rappel, sachez que la fonction de rappel doit être assez limitée.</span><span class="sxs-lookup"><span data-stu-id="3eb51-148">(Before using callback mode, be aware that the callback function must be quite limited.</span></span> <span data-ttu-id="3eb51-149">Dans le cas contraire, elle peut réduire considérablement les performances, voire entraîner des interblocages.</span><span class="sxs-lookup"><span data-stu-id="3eb51-149">Otherwise, it can drastically reduce performance or even cause deadlocks.</span></span> <span data-ttu-id="3eb51-150">Pour plus d’informations, consultez [**ISampleGrabber :: SetCallback**](isamplegrabber-setcallback.md).) Pour activer le mode de mise en mémoire tampon, appelez la méthode [**ISampleGrabber :: SetBufferSamples**](isamplegrabber-setbuffersamples.md) avec la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="3eb51-150">For more information, see [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md).) To activate buffering mode, call the [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) method with the value **TRUE**.</span></span>

<span data-ttu-id="3eb51-151">Si vous le souhaitez, appelez la méthode [**ISampleGrabber :: SetOneShot**](isamplegrabber-setoneshot.md) avec la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="3eb51-151">Optionally, call the [**ISampleGrabber::SetOneShot**](isamplegrabber-setoneshot.md) method with the value **TRUE**.</span></span> <span data-ttu-id="3eb51-152">Cela provoque l’arrêt de la capture de l’exemple après avoir reçu le premier exemple de support, ce qui est utile si vous souhaitez récupérer une image unique à partir du flux.</span><span class="sxs-lookup"><span data-stu-id="3eb51-152">This causes the Sample Grabber to halt after it receives the first media sample, which is useful if you want to grab a single frame from the stream.</span></span> <span data-ttu-id="3eb51-153">Recherchez l’heure souhaitée, exécutez le graphique et attendez la [**\_ fin**](ec-complete.md) de l’événement ce.</span><span class="sxs-lookup"><span data-stu-id="3eb51-153">Seek to the desired time, run the graph, and wait for the [**EC\_COMPLETE**](ec-complete.md) event.</span></span> <span data-ttu-id="3eb51-154">Notez que le niveau de précision du frame dépend de la source.</span><span class="sxs-lookup"><span data-stu-id="3eb51-154">Note that the level of frame accuracy depends on the source.</span></span> <span data-ttu-id="3eb51-155">Par exemple, la recherche d’un fichier MPEG n’est souvent pas correcte.</span><span class="sxs-lookup"><span data-stu-id="3eb51-155">For example, seeking an MPEG file is often not frame accurate.</span></span>

<span data-ttu-id="3eb51-156">Pour exécuter le graphique aussi rapidement que possible, activez l’horloge du graphique comme décrit dans [définition de l’horloge du graphique](setting-the-graph-clock.md).</span><span class="sxs-lookup"><span data-stu-id="3eb51-156">To run the graph as fast as possible, turn of the graph clock as described in [Setting the Graph Clock](setting-the-graph-clock.md).</span></span>

<span data-ttu-id="3eb51-157">L’exemple suivant active le mode de mise en mémoire tampon et le mode à une seule capture, exécute le graphique de filtre et attend la fin de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="3eb51-157">The following example enables one-shot mode and buffering mode, runs the filter graph, and waits for completion.</span></span>


```C++
    hr = pGrabber->SetOneShot(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetBufferSamples(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pControl->Run();
    if (FAILED(hr))
    {
        goto done;
    }

    long evCode;
    hr = pEvent->WaitForCompletion(INFINITE, &evCode);
```



## <a name="grab-the-sample"></a><span data-ttu-id="3eb51-158">Extraire l’exemple</span><span class="sxs-lookup"><span data-stu-id="3eb51-158">Grab the Sample</span></span>

<span data-ttu-id="3eb51-159">En mode de mise en mémoire tampon, l’exemple de la accroche stocke une copie de chaque exemple.</span><span class="sxs-lookup"><span data-stu-id="3eb51-159">In buffering mode, the Sample Grabber stores a copy of every sample.</span></span> <span data-ttu-id="3eb51-160">La méthode [**ISampleGrabber :: GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) copie la mémoire tampon dans un tableau alloué par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="3eb51-160">The [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) method copies the buffer into a caller-allocated array.</span></span> <span data-ttu-id="3eb51-161">Pour déterminer la taille du tableau nécessaire, appelez d’abord **GetCurrentBuffer** avec un pointeur **null** pour l’adresse du tableau.</span><span class="sxs-lookup"><span data-stu-id="3eb51-161">To determine the size of the array that is needed, first call **GetCurrentBuffer** with a **NULL** pointer for the array address.</span></span> <span data-ttu-id="3eb51-162">Allouez ensuite le tableau et appelez la méthode une deuxième fois pour copier la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="3eb51-162">Then allocate the array and call the method a second time to copy the buffer.</span></span> <span data-ttu-id="3eb51-163">L'exemple suivant affiche ces étapes.</span><span class="sxs-lookup"><span data-stu-id="3eb51-163">The following example shows these steps.</span></span>


```C++
    // Find the required buffer size.
    long cbBuffer;
    hr = pGrabber->GetCurrentBuffer(&cbBuffer, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    pBuffer = (BYTE*)CoTaskMemAlloc(cbBuffer);
    if (!pBuffer) 
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pGrabber->GetCurrentBuffer(&cbBuffer, (long*)pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }
```



<span data-ttu-id="3eb51-164">Vous devez connaître le format exact des données dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="3eb51-164">You will need to know the exact format of the data in the buffer.</span></span> <span data-ttu-id="3eb51-165">Pour récupérer ces informations, appelez la méthode [**ISampleGrabber :: GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="3eb51-165">To get this information, call the [**ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) method.</span></span> <span data-ttu-id="3eb51-166">Cette méthode remplit une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) avec le format.</span><span class="sxs-lookup"><span data-stu-id="3eb51-166">This method fills in an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure with the format.</span></span>

<span data-ttu-id="3eb51-167">Pour un flux vidéo non compressé, les informations de format sont contenues dans une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="3eb51-167">For an uncompressed video stream, the format information is contained in a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span> <span data-ttu-id="3eb51-168">L’exemple suivant montre comment obtenir les informations de mise en forme d’un flux vidéo non compressé.</span><span class="sxs-lookup"><span data-stu-id="3eb51-168">The following example shows how to get the format information for an uncompressed video stream.</span></span>


```C++
    // Examine the format block.
    if ((mt.formattype == FORMAT_VideoInfo) && 
        (mt.cbFormat >= sizeof(VIDEOINFOHEADER)) &&
        (mt.pbFormat != NULL)) 
    {
        VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)mt.pbFormat;

        hr = WriteBitmap(pszBitmapFile, &pVih->bmiHeader, 
            mt.cbFormat - SIZE_PREHEADER, pBuffer, cbBuffer);
    }
    else 
    {
        // Invalid format.
        hr = VFW_E_INVALIDMEDIATYPE; 
    }
```



> [!Note]  
> <span data-ttu-id="3eb51-169">L’exemple de la accroche ne prend pas en charge [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span><span class="sxs-lookup"><span data-stu-id="3eb51-169">The Sample Grabber does not support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span></span>

 

## <a name="example-code"></a><span data-ttu-id="3eb51-170">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="3eb51-170">Example Code</span></span>

<span data-ttu-id="3eb51-171">Voici le code complet pour les exemples précédents.</span><span class="sxs-lookup"><span data-stu-id="3eb51-171">Here is the complete code for the previous examples.</span></span>

> [!Note]  
> <span data-ttu-id="3eb51-172">Cet exemple utilise la fonction [SafeRelease](../medfound/saferelease.md) pour libérer des pointeurs d’interface.</span><span class="sxs-lookup"><span data-stu-id="3eb51-172">This example uses the [SafeRelease](../medfound/saferelease.md) function to release interface pointers.</span></span>

 


```C++
#include <windows.h>
#include <dshow.h>
#include "qedit.h"

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}



HRESULT WriteBitmap(PCWSTR, BITMAPINFOHEADER*, size_t, BYTE*, size_t);

HRESULT GrabVideoBitmap(PCWSTR pszVideoFile, PCWSTR pszBitmapFile)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEventEx *pEvent = NULL;
    IBaseFilter *pGrabberF = NULL;
    ISampleGrabber *pGrabber = NULL;
    IBaseFilter *pSourceF = NULL;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;
    IBaseFilter *pNullF = NULL;

    BYTE *pBuffer = NULL;

    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER,IID_PPV_ARGS(&pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pEvent));
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the Sample Grabber filter.
    hr = CoCreateInstance(CLSID_SampleGrabber, NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pGrabberF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pGrabberF, L&quot;Sample Grabber&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabberF->QueryInterface(IID_PPV_ARGS(&pGrabber));
    if (FAILED(hr))
    {
        goto done;
    }

    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(mt));
    mt.majortype = MEDIATYPE_Video;
    mt.subtype = MEDIASUBTYPE_RGB24;

    hr = pGrabber->SetMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddSourceFilter(pszVideoFile, L&quot;Source&quot;, &pSourceF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSourceF->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = ConnectFilters(pGraph, pPin, pGrabberF);
        SafeRelease(&pPin);
        if (SUCCEEDED(hr))
        {
            break;
        }
    }

    if (FAILED(hr))
    {
        goto done;
    }

    hr = CoCreateInstance(CLSID_NullRenderer, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pNullF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pNullF, L&quot;Null Filter&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConnectFilters(pGraph, pGrabberF, pNullF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetOneShot(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetBufferSamples(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pControl->Run();
    if (FAILED(hr))
    {
        goto done;
    }

    long evCode;
    hr = pEvent->WaitForCompletion(INFINITE, &evCode);

    // Find the required buffer size.
    long cbBuffer;
    hr = pGrabber->GetCurrentBuffer(&cbBuffer, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    pBuffer = (BYTE*)CoTaskMemAlloc(cbBuffer);
    if (!pBuffer) 
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pGrabber->GetCurrentBuffer(&cbBuffer, (long*)pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->GetConnectedMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }

    // Examine the format block.
    if ((mt.formattype == FORMAT_VideoInfo) && 
        (mt.cbFormat >= sizeof(VIDEOINFOHEADER)) &&
        (mt.pbFormat != NULL)) 
    {
        VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)mt.pbFormat;

        hr = WriteBitmap(pszBitmapFile, &pVih->bmiHeader, 
            mt.cbFormat - SIZE_PREHEADER, pBuffer, cbBuffer);
    }
    else 
    {
        // Invalid format.
        hr = VFW_E_INVALIDMEDIATYPE; 
    }

    FreeMediaType(mt);

done:
    CoTaskMemFree(pBuffer);
    SafeRelease(&pPin);
    SafeRelease(&pEnum);
    SafeRelease(&pNullF);
    SafeRelease(&pSourceF);
    SafeRelease(&pGrabber);
    SafeRelease(&pGrabberF);
    SafeRelease(&pControl);
    SafeRelease(&pEvent);
    SafeRelease(&pGraph);
    return hr;
};

// Writes a bitmap file
//  pszFileName:  Output file name.
//  pBMI:         Bitmap format information (including pallete).
//  cbBMI:        Size of the BITMAPINFOHEADER, including palette, if present.
//  pData:        Pointer to the bitmap bits.
//  cbData        Size of the bitmap, in bytes.

HRESULT WriteBitmap(PCWSTR pszFileName, BITMAPINFOHEADER *pBMI, size_t cbBMI,
    BYTE *pData, size_t cbData)
{
    HANDLE hFile = CreateFile(pszFileName, GENERIC_WRITE, 0, NULL, 
        CREATE_ALWAYS, 0, NULL);
    if (hFile == NULL)
    {
        return HRESULT_FROM_WIN32(GetLastError());
    }

    BITMAPFILEHEADER bmf = { };

    bmf.bfType = &#39;MB&#39;;
    bmf.bfSize = cbBMI+ cbData + sizeof(bmf); 
    bmf.bfOffBits = sizeof(bmf) + cbBMI; 

    DWORD cbWritten = 0;
    BOOL result = WriteFile(hFile, &bmf, sizeof(bmf), &cbWritten, NULL);
    if (result)
    {
        result = WriteFile(hFile, pBMI, cbBMI, &cbWritten, NULL);
    }
    if (result)
    {
        result = WriteFile(hFile, pData, cbData, &cbWritten, NULL);
    }

    HRESULT hr = result ? S_OK : HRESULT_FROM_WIN32(GetLastError());

    CloseHandle(hFile);

    return hr;
}
```





## <a name="related-topics"></a><span data-ttu-id="3eb51-173">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3eb51-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3eb51-174">Utilisation des services de modification DirectShow</span><span class="sxs-lookup"><span data-stu-id="3eb51-174">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 
