---
description: Capture d’une image à partir d’un code confidentiel d’image continue
ms.assetid: cbcb4d6d-dc85-4ae2-b0a8-110f15092733
title: Capture d’une image à partir d’un code confidentiel d’image continue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3510f318f3107dd698dc753704d6c09d70ddd308
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746085"
---
# <a name="capturing-an-image-from-a-still-image-pin"></a><span data-ttu-id="8b024-103">Capture d’une image à partir d’un code confidentiel d’image continue</span><span class="sxs-lookup"><span data-stu-id="8b024-103">Capturing an Image From a Still Image Pin</span></span>

<span data-ttu-id="8b024-104">Certains appareils photo peuvent produire une image toujours distincte du flux de capture, et l’image continue est souvent d’une qualité supérieure à celle des images générées par le flux de capture.</span><span class="sxs-lookup"><span data-stu-id="8b024-104">Some cameras can produce a still image separate from the capture stream, and often the still image is of higher quality than the images produced by the capture stream.</span></span> <span data-ttu-id="8b024-105">L’appareil photo peut avoir un bouton qui agit comme un déclencheur matériel ou peut prendre en charge le déclenchement de logiciels.</span><span class="sxs-lookup"><span data-stu-id="8b024-105">The camera may have a button that acts as a hardware trigger, or it may support software triggering.</span></span> <span data-ttu-id="8b024-106">Une caméra qui prend en charge les images continues expose une broche d’image continue, qui est la catégorie de code confidentiel catégorie \_ \_ toujours.</span><span class="sxs-lookup"><span data-stu-id="8b024-106">A camera that supports still images will expose a still image pin, which is pin category PIN\_CATEGORY\_STILL.</span></span>

<span data-ttu-id="8b024-107">La méthode recommandée pour l’obtention d’images toujours à partir de l’appareil consiste à utiliser les API WIA (Windows Image Acquisition).</span><span class="sxs-lookup"><span data-stu-id="8b024-107">The recommended way to get still images from the device is to use the Windows Image Acquisition (WIA) APIs.</span></span> <span data-ttu-id="8b024-108">Pour plus d’informations, consultez « acquisition d’images Windows » dans la documentation du kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="8b024-108">For more information, see "Windows Image Acquisition" in the Platform SDK documentation.</span></span> <span data-ttu-id="8b024-109">Toutefois, vous pouvez également utiliser DirectShow pour capturer une image.</span><span class="sxs-lookup"><span data-stu-id="8b024-109">However, you can also use DirectShow to capture an image.</span></span>

<span data-ttu-id="8b024-110">Pour déclencher le code confidentiel toujours, utilisez la méthode [**IAMVideoControl :: setMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) lorsque le graphique est en cours d’exécution, comme suit :</span><span class="sxs-lookup"><span data-stu-id="8b024-110">To trigger the still pin, use the [**IAMVideoControl::SetMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) method when the graph is running, as follows:</span></span>


```C++
IAMVideoControl *pAMVidControl = NULL;

hr = pControl->Run(); // Run the graph.
if (FAILED(hr))
{
    // Handle error.
}

hr = pCap->QueryInterface(IID_IAMVideoControl, (void**)&pAMVidControl);

if (SUCCEEDED(hr))
{
    // Find the still pin.
    IPin *pPin = NULL;

    // pBuild is an ICaptureGraphBuilder2 pointer.

    hr = pBuild->FindPin(
        pCap,                  // Filter.
        PINDIR_OUTPUT,         // Look for an output pin.
        &PIN_CATEGORY_STILL,   // Pin category.
        NULL,                  // Media type (don't care).
        FALSE,                 // Pin must be unconnected.
        0,                     // Get the 0'th pin.
        &pPin                  // Receives a pointer to thepin.
        );

    if (SUCCEEDED(hr))
    {
        hr = pAMVidControl->SetMode(pPin, VideoControlFlag_Trigger);
        pPin->Release();
    }
    pAMVidControl->Release();
}
```



<span data-ttu-id="8b024-111">Interrogez le filtre de capture pour [**IAMVideoControl**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol).</span><span class="sxs-lookup"><span data-stu-id="8b024-111">Query the capture filter for [**IAMVideoControl**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol).</span></span> <span data-ttu-id="8b024-112">Si l’interface est prise en charge, vous pouvez obtenir un pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du code confidentiel, en appelant la méthode [**ICaptureGraphBuilder2 :: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) , comme indiqué dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="8b024-112">If the interface is supported, get a pointer to the still pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface by calling the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method, as shown in the previous example.</span></span> <span data-ttu-id="8b024-113">Appelez ensuite [**IAMVideoControl :: setMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) avec le pointeur **IPIN** et l' \_ indicateur de déclencheur VideoControlFlag.</span><span class="sxs-lookup"><span data-stu-id="8b024-113">Then call [**IAMVideoControl::SetMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) with the **IPin** pointer and the VideoControlFlag\_Trigger flag.</span></span>

> [!Note]  
> <span data-ttu-id="8b024-114">En fonction de l’appareil photo, vous devrez peut-être afficher le code confidentiel de capture (catégorie ÉPINGLer la \_ \_ capture) avant que le code confidentiel reste connecté.</span><span class="sxs-lookup"><span data-stu-id="8b024-114">Depending on the camera, you might need to render the capture pin (PIN\_CATEGORY\_CAPTURE) before the still pin will connect.</span></span>

 

### <a name="example-using-the-sample-grabber-filter"></a><span data-ttu-id="8b024-115">Exemple : utilisation de l’exemple de filtre d’accrochage</span><span class="sxs-lookup"><span data-stu-id="8b024-115">Example: Using the Sample Grabber Filter</span></span>

<span data-ttu-id="8b024-116">L’une des façons de capturer l’image est d’utiliser l’exemple de filtre d' [**accrochage**](sample-grabber-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="8b024-116">One way to capture the image is with the [**Sample Grabber**](sample-grabber-filter.md) filter.</span></span> <span data-ttu-id="8b024-117">L’exemple de la accroche utilise une fonction de rappel définie par l’application pour traiter l’image.</span><span class="sxs-lookup"><span data-stu-id="8b024-117">The Sample Grabber uses an application-defined callback function to process the image.</span></span> <span data-ttu-id="8b024-118">Pour plus d’informations sur l’exemple de filtre d’accrochage, consultez [utilisation de l’exemple de](using-the-sample-grabber.md)collecte.</span><span class="sxs-lookup"><span data-stu-id="8b024-118">For more information about the Sample Grabber filter, see [Using the Sample Grabber](using-the-sample-grabber.md).</span></span>

<span data-ttu-id="8b024-119">L’exemple suivant suppose que la broche continue fournit une image RVB non compressée.</span><span class="sxs-lookup"><span data-stu-id="8b024-119">The following example assumes that the still pin delivers an uncompressed RGB image.</span></span> <span data-ttu-id="8b024-120">Tout d’abord, définissez une classe qui implémentera l’interface de rappel de l’exemple de la accroche, [**ISampleGrabberCB**](isamplegrabbercb.md):</span><span class="sxs-lookup"><span data-stu-id="8b024-120">First, define a class that will implement the Sample Grabber's callback interface, [**ISampleGrabberCB**](isamplegrabbercb.md):</span></span>


```C++
// Class to hold the callback function for the Sample Grabber filter.
class SampleGrabberCallback : public ISampleGrabberCB
{
    // Implementation is described later.
}

// Global instance of the class.
SampleGrabberCallback g_StillCapCB;
```



<span data-ttu-id="8b024-121">L’implémentation de la classe est décrite rapidement.</span><span class="sxs-lookup"><span data-stu-id="8b024-121">The implementation of the class is described shortly.</span></span>

<span data-ttu-id="8b024-122">Ensuite, connectez la broche continue à la accroche d’échantillon et connectez l’exemple de la accroche au filtre de [**convertisseur null**](null-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="8b024-122">Next, connect the still pin to the Sample Grabber, and connect the Sample Grabber to the [**Null Renderer**](null-renderer-filter.md) filter.</span></span> <span data-ttu-id="8b024-123">Le convertisseur null ignore simplement les exemples de supports qu’il reçoit. le travail réel sera effectué dans le rappel.</span><span class="sxs-lookup"><span data-stu-id="8b024-123">The Null Renderer simply discards media samples that it receives; the actual work will be done within the callback.</span></span> <span data-ttu-id="8b024-124">(La seule raison pour laquelle le convertisseur null est de connecter la broche de sortie de l’exemple d’accrochage à un élément.) Appelez [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer les filtres de rendu d’exemple et de convertisseur null, puis appelez [**IFilterGraph :: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) pour ajouter les deux filtres au graphique :</span><span class="sxs-lookup"><span data-stu-id="8b024-124">(The only reason for the Null Renderer is to connect the Sample Grabber's output pin to something.) Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Sample Grabber and Null Renderer filters, and call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add both filters to the graph:</span></span>


```C++
// Add the Sample Grabber filter to the graph.
IBaseFilter *pSG_Filter;
hr = CoCreateInstance(
    CLSID_SampleGrabber, 
    NULL, 
    CLSCTX_INPROC_SERVER,
    IID_IBaseFilter, 
    (void**)&pSG_Filter
    );

hr = pGraph->AddFilter(pSG_Filter, L"SampleGrab");

// Add the Null Renderer filter to the graph.
IBaseFilter *pNull;

hr = CoCreateInstance(
    CLSID_NullRenderer, 
    NULL, 
    CLSCTX_INPROC_SERVER,
    IID_IBaseFilter, 
    (void**)&pNull
    );

hr = pGraph->AddFilter(pNull, L"NullRender");
```



<span data-ttu-id="8b024-125">Vous pouvez utiliser la méthode [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) pour connecter les trois filtres dans un appel de méthode, en allant de la goupille continue à la accroche d’échantillon et de l’accrochage de l’échantillon au convertisseur NULL :</span><span class="sxs-lookup"><span data-stu-id="8b024-125">You can use the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method to connect all three filters in one method call, going from the still pin to the Sample Grabber, and from the Sample Grabber to the Null Renderer:</span></span>


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_STILL, // Connect this pin ...
    &MEDIATYPE_Video,    // with this media type ...
    pCap,                // on this filter ...
    pSG_Filter,          // to the Sample Grabber ...
    pNull);              // ... and finally to the Null Renderer.
```



<span data-ttu-id="8b024-126">À présent, utilisez l’interface [**ISampleGrabber**](isamplegrabber.md) pour configurer l’exemple de la accrochage afin de mettre en mémoire tampon des exemples :</span><span class="sxs-lookup"><span data-stu-id="8b024-126">Now use the [**ISampleGrabber**](isamplegrabber.md) interface to configure the Sample Grabber so that it buffers samples:</span></span>


```C++
// Configure the Sample Grabber.
ISampleGrabber *pSG = NULL;

hr = pSG_Filter->QueryInterface(IID_ISampleGrabber, (void**)&pSG);
if (SUCCEEDED(hr))
{
    hr = pSG->SetOneShot(FALSE);
    hr = pSG->SetBufferSamples(TRUE);

    ...
```



<span data-ttu-id="8b024-127">Définissez l’interface de rappel avec un pointeur vers votre objet de rappel :</span><span class="sxs-lookup"><span data-stu-id="8b024-127">Set the callback interface with a pointer to your callback object:</span></span>


```C++
hr = pSG->SetCallback(&g_StillCapCB, 0); // 0 = Use the SampleCB callback method.
```



<span data-ttu-id="8b024-128">Obtient le type de média que le code confidentiel toujours utilisé pour se connecter avec la accroche d’échantillon :</span><span class="sxs-lookup"><span data-stu-id="8b024-128">Get the media type that the still pin used to connect with the Sample Grabber:</span></span>


```C++
// Store the media type for later use.
AM_MEDIA_TYPE g_StillMediaType;

hr = pSG->GetConnectedMediaType(&g_StillMediaType);
pSG->Release();
```



<span data-ttu-id="8b024-129">Ce type de média contient la structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) qui définit le format de l’image fixe.</span><span class="sxs-lookup"><span data-stu-id="8b024-129">This media type will contain the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure that defines the format of the still image.</span></span> <span data-ttu-id="8b024-130">Libérer le type de média avant la fermeture de l’application :</span><span class="sxs-lookup"><span data-stu-id="8b024-130">Free the media type before the application exits:</span></span>


```C++
// On exit, remember to release the media type.
FreeMediaType(g_StillMediaType);
```



<span data-ttu-id="8b024-131">Ce qui suit est un exemple de la classe de rappel.</span><span class="sxs-lookup"><span data-stu-id="8b024-131">What follows is an example of the callback class.</span></span> <span data-ttu-id="8b024-132">Notez que la classe implémente **IUnknown**, dont elle hérite via l’interface [**ISampleGrabber**](isamplegrabber.md) , mais ne conserve pas de décompte de références.</span><span class="sxs-lookup"><span data-stu-id="8b024-132">Note that the class implements **IUnknown**, which it inherits through the [**ISampleGrabber**](isamplegrabber.md) interface, but it does not keep a reference count.</span></span> <span data-ttu-id="8b024-133">Cela est sécurisé, car l’application crée l’objet sur la pile, et l’objet reste dans la portée tout au long de la durée de vie du graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="8b024-133">This is safe because the application creates the object on the stack, and the object remains in scope throughout the lifetime of the filter graph.</span></span>

<span data-ttu-id="8b024-134">Tout le travail se produit dans la méthode [**BufferCB**](isamplegrabbercb-buffercb.md) , qui est appelée par l’exemple de redimensionnement chaque fois qu’il obtient un nouvel exemple.</span><span class="sxs-lookup"><span data-stu-id="8b024-134">All of the work happens in the [**BufferCB**](isamplegrabbercb-buffercb.md) method, which is called by the Sample Grabber whenever it gets a new sample.</span></span> <span data-ttu-id="8b024-135">Dans l’exemple suivant, la méthode écrit l’image bitmap dans un fichier :</span><span class="sxs-lookup"><span data-stu-id="8b024-135">In the following example, the method writes the bitmap to a file:</span></span>


```C++
class SampleGrabberCallback : public ISampleGrabberCB
{
public:
    // Fake referance counting.
    STDMETHODIMP_(ULONG) AddRef() { return 1; }
    STDMETHODIMP_(ULONG) Release() { return 2; }

    STDMETHODIMP QueryInterface(REFIID riid, void **ppvObject)
    {
        if (NULL == ppvObject) return E_POINTER;
        if (riid == __uuidof(IUnknown))
        {
            *ppvObject = static_cast<IUnknown*>(this);
             return S_OK;
        }
        if (riid == __uuidof(ISampleGrabberCB))
        {
            *ppvObject = static_cast<ISampleGrabberCB*>(this);
             return S_OK;
        }
        return E_NOTIMPL;
    }

    STDMETHODIMP SampleCB(double Time, IMediaSample *pSample)
    {
        return E_NOTIMPL;
    }

    STDMETHODIMP BufferCB(double Time, BYTE *pBuffer, long BufferLen)
    {
        if ((g_StillMediaType.majortype != MEDIATYPE_Video) ||
            (g_StillMediaType.formattype != FORMAT_VideoInfo) ||
            (g_StillMediaType.cbFormat < sizeof(VIDEOINFOHEADER)) ||
            (g_StillMediaType.pbFormat == NULL))
        {
            return VFW_E_INVALIDMEDIATYPE;
        }
        HANDLE hf = CreateFile("C:\\Example.bmp", GENERIC_WRITE, 
        FILE_SHARE_WRITE, NULL, CREATE_ALWAYS, 0, NULL);
        if (hf == INVALID_HANDLE_VALUE)
        {
            return E_FAIL;
        }
        long cbBitmapInfoSize = g_StillMediaType.cbFormat - SIZE_PREHEADER;
        VIDEOINFOHEADER *pVideoHeader =
           (VIDEOINFOHEADER*)g_StillMediaType.pbFormat;

        BITMAPFILEHEADER bfh;
        ZeroMemory(&bfh, sizeof(bfh));
        bfh.bfType = 'MB';  // Little-endian for "BM".
        bfh.bfSize = sizeof( bfh ) + BufferLen + cbBitmapInfoSize;
        bfh.bfOffBits = sizeof( BITMAPFILEHEADER ) + cbBitmapInfoSize;
        
        // Write the file header.
        DWORD dwWritten = 0;
        WriteFile( hf, &bfh, sizeof( bfh ), &dwWritten, NULL );
        WriteFile(hf, HEADER(pVideoHeader), cbBitmapInfoSize, &dwWritten, NULL);        
        WriteFile( hf, pBuffer, BufferLen, &dwWritten, NULL );
        CloseHandle( hf );
        return S_OK;

    }
};
```



## <a name="related-topics"></a><span data-ttu-id="8b024-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8b024-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b024-137">Tâches de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="8b024-137">Video Capture Tasks</span></span>](video-capture-tasks.md)
</dt> </dl>

 

 
