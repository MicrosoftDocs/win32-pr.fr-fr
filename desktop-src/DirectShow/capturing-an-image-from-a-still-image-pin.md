---
description: Capture d’une image à partir d’un code confidentiel d’image continue
ms.assetid: cbcb4d6d-dc85-4ae2-b0a8-110f15092733
title: Capture d’une image à partir d’un code confidentiel d’image continue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3510f318f3107dd698dc753704d6c09d70ddd308
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094873"
---
# <a name="capturing-an-image-from-a-still-image-pin"></a>Capture d’une image à partir d’un code confidentiel d’image continue

Certains appareils photo peuvent produire une image toujours distincte du flux de capture, et l’image continue est souvent d’une qualité supérieure à celle des images générées par le flux de capture. L’appareil photo peut avoir un bouton qui agit comme un déclencheur matériel ou peut prendre en charge le déclenchement de logiciels. Une caméra qui prend en charge les images continues expose une broche d’image continue, qui est la catégorie de code confidentiel catégorie \_ \_ toujours.

la méthode recommandée pour l’obtention d’images toujours à partir de l’appareil consiste à utiliser les api d’Acquisition d’images Windows (WIA). pour plus d’informations, consultez « Windows Image Acquisition » dans la documentation du kit de développement platform SDK. toutefois, vous pouvez également utiliser DirectShow pour capturer une image.

Pour déclencher le code confidentiel toujours, utilisez la méthode [**IAMVideoControl :: setMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) lorsque le graphique est en cours d’exécution, comme suit :


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



Interrogez le filtre de capture pour [**IAMVideoControl**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol). Si l’interface est prise en charge, vous pouvez obtenir un pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du code confidentiel, en appelant la méthode [**ICaptureGraphBuilder2 :: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) , comme indiqué dans l’exemple précédent. Appelez ensuite [**IAMVideoControl :: setMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) avec le pointeur **IPIN** et l' \_ indicateur de déclencheur VideoControlFlag.

> [!Note]  
> En fonction de l’appareil photo, vous devrez peut-être afficher le code confidentiel de capture (catégorie ÉPINGLer la \_ \_ capture) avant que le code confidentiel reste connecté.

 

### <a name="example-using-the-sample-grabber-filter"></a>Exemple : utilisation de l’exemple de filtre d’accrochage

L’une des façons de capturer l’image est d’utiliser l’exemple de filtre d' [**accrochage**](sample-grabber-filter.md) . L’exemple de la accroche utilise une fonction de rappel définie par l’application pour traiter l’image. Pour plus d’informations sur l’exemple de filtre d’accrochage, consultez [utilisation de l’exemple de](using-the-sample-grabber.md)collecte.

L’exemple suivant suppose que la broche continue fournit une image RVB non compressée. Tout d’abord, définissez une classe qui implémentera l’interface de rappel de l’exemple de la accroche, [**ISampleGrabberCB**](isamplegrabbercb.md):


```C++
// Class to hold the callback function for the Sample Grabber filter.
class SampleGrabberCallback : public ISampleGrabberCB
{
    // Implementation is described later.
}

// Global instance of the class.
SampleGrabberCallback g_StillCapCB;
```



L’implémentation de la classe est décrite rapidement.

Ensuite, connectez la broche continue à la accroche d’échantillon et connectez l’exemple de la accroche au filtre de [**convertisseur null**](null-renderer-filter.md) . Le convertisseur null ignore simplement les exemples de supports qu’il reçoit. le travail réel sera effectué dans le rappel. (La seule raison pour laquelle le convertisseur null est de connecter la broche de sortie de l’exemple d’accrochage à un élément.) Appelez [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer les filtres de rendu d’exemple et de convertisseur null, puis appelez [**IFilterGraph :: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) pour ajouter les deux filtres au graphique :


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



Vous pouvez utiliser la méthode [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) pour connecter les trois filtres dans un appel de méthode, en allant de la goupille continue à la accroche d’échantillon et de l’accrochage de l’échantillon au convertisseur NULL :


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_STILL, // Connect this pin ...
    &MEDIATYPE_Video,    // with this media type ...
    pCap,                // on this filter ...
    pSG_Filter,          // to the Sample Grabber ...
    pNull);              // ... and finally to the Null Renderer.
```



À présent, utilisez l’interface [**ISampleGrabber**](isamplegrabber.md) pour configurer l’exemple de la accrochage afin de mettre en mémoire tampon des exemples :


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



Définissez l’interface de rappel avec un pointeur vers votre objet de rappel :


```C++
hr = pSG->SetCallback(&g_StillCapCB, 0); // 0 = Use the SampleCB callback method.
```



Obtient le type de média que le code confidentiel toujours utilisé pour se connecter avec la accroche d’échantillon :


```C++
// Store the media type for later use.
AM_MEDIA_TYPE g_StillMediaType;

hr = pSG->GetConnectedMediaType(&g_StillMediaType);
pSG->Release();
```



Ce type de média contient la structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) qui définit le format de l’image fixe. Libérer le type de média avant la fermeture de l’application :


```C++
// On exit, remember to release the media type.
FreeMediaType(g_StillMediaType);
```



Ce qui suit est un exemple de la classe de rappel. Notez que la classe implémente **IUnknown**, dont elle hérite via l’interface [**ISampleGrabber**](isamplegrabber.md) , mais ne conserve pas de décompte de références. Cela est sécurisé, car l’application crée l’objet sur la pile, et l’objet reste dans la portée tout au long de la durée de vie du graphique de filtre.

Tout le travail se produit dans la méthode [**BufferCB**](isamplegrabbercb-buffercb.md) , qui est appelée par l’exemple de redimensionnement chaque fois qu’il obtient un nouvel exemple. Dans l’exemple suivant, la méthode écrit l’image bitmap dans un fichier :


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tâches de capture vidéo](video-capture-tasks.md)
</dt> </dl>

 

 
