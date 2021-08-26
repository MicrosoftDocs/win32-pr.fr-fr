---
description: L’exemple de filtre d’accrochage est un filtre de transformation qui peut être utilisé pour récupérer des échantillons de média à partir d’un flux lorsqu’ils passent par le graphique de filtre.
ms.assetid: ec0e367e-9ef9-4de6-9132-b462c233bc98
title: Utilisation de l’exemple d’accrochage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47318b7bd4dbbad57fb82bec11e0a1293a0284c906c78fc7175d8a758ad477f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083559"
---
# <a name="using-the-sample-grabber"></a>Utilisation de l’exemple d’accrochage

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

L’exemple de filtre d' [**accrochage**](sample-grabber-filter.md) est un filtre de transformation qui peut être utilisé pour récupérer des échantillons de média à partir d’un flux lorsqu’ils passent par le graphique de filtre.

Si vous souhaitez simplement récupérer une image bitmap à partir d’un fichier vidéo, il est plus facile d’utiliser l’objet [MediaDet (Media DETECTER)](media-detector--mediadet.md) . Pour plus d’informations, consultez [saisie d’un cadre d’affiche](grabbing-a-poster-frame.md) . Toutefois, cette accroche est plus souple, car elle fonctionne avec presque n’importe quel type de média (consultez [**ISampleGrabber :: SetMediaType**](isamplegrabber-setmediatype.md) pour les rares exceptions) et offre davantage de contrôle à l’application.

-   [créer le gestionnaire de Graph de filtre](#create-the-filter-graph-manager)
-   [Ajoutez l’exemple d’accrochage au filtre Graph](#add-the-sample-grabber-to-the-filter-graph)
-   [Définir le type de média](#set-the-media-type)
-   [Générer le filtre Graph](#build-the-filter-graph)
-   [Exécuter le Graph](#run-the-graph)
-   [Extraire l’exemple](#grab-the-sample)
-   [Exemple de code](#example-code)
-   [Rubriques connexes](#related-topics)

## <a name="create-the-filter-graph-manager"></a>créer le gestionnaire de Graph de filtre

pour commencer, créez le [filtre Graph Manager](filter-graph-manager.md) et la requête pour les interfaces [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) et [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) .


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





## <a name="add-the-sample-grabber-to-the-filter-graph"></a>Ajoutez l’exemple d’accrochage au filtre Graph

Créez une instance de l’exemple de filtre d’accrochage et Addit dans le graphique de filtre. Interrogez l’exemple de filtre d’accrochage pour l’interface [**ISampleGrabber**](isamplegrabber.md) .


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





## <a name="set-the-media-type"></a>Définir le type de média

Lorsque vous créez pour la première fois la accroche, elle n’a pas de type de média préféré. Cela signifie que vous pouvez vous connecter à presque n’importe quel filtre dans le graphique, mais que vous n’avez aucun contrôle sur le type de données qu’il a reçu. Avant de générer le reste du graphique, par conséquent, vous devez définir un type de média pour la accroche d’échantillon, en appelant la méthode [**ISampleGrabber :: SetMediaType**](isamplegrabber-setmediatype.md) .

Lorsque l’accrochage de l’exemple se connecte, il compare ce type de média au type de média proposé par l’autre filtre. Les seuls champs qu’il vérifie sont le type, le sous-type et le type de format principaux. Pour l’une de ces valeurs, la valeur de GUID \_ null signifie « accepter n’importe quelle valeur ». La plupart du temps, vous voudrez définir le type et le sous-type principaux. Par exemple, le code suivant spécifie une vidéo RGB 24 bits non compressée :


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



## <a name="build-the-filter-graph"></a>Générer le filtre Graph

Vous pouvez maintenant créer le reste du graphique de filtre. étant donné que l’exemple d’accrochage se connecte uniquement à l’aide du type de média que vous avez spécifié, vous pouvez ainsi tirer parti des mécanismes de [Connecter intelligents](intelligent-connect.md) du gestionnaire Graph Manager lorsque vous générez le graphique.

par exemple, si vous avez spécifié une vidéo non compressée, vous pouvez connecter un filtre source à la accroche d’échantillon, et le gestionnaire de Graph de filtre ajoutera automatiquement l’analyseur de fichiers et le décodeur. l’exemple suivant utilise la fonction d’assistance ConnectFilters, qui est indiquée dans [Connecter deux filtres](connect-two-filters.md):


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





L’échantillon est un filtre de transformation, donc la broche de sortie doit être connectée à un autre filtre. Souvent, vous pouvez simplement ignorer les exemples une fois que vous avez fini de les utiliser. Dans ce cas, connectez l’exemple d’accrochage au [**filtre de convertisseur null**](null-renderer-filter.md), qui ignore les données qu’il reçoit.

L’exemple suivant connecte l’exemple d’accrochage au filtre de convertisseur NULL :


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





Sachez que le placement de l’échantillon entre un décodeur vidéo et le convertisseur vidéo peut considérablement nuire aux performances de rendu. L’exemple d’accrochage est un filtre de transfert sur place, ce qui signifie que la mémoire tampon de sortie est la même que la mémoire tampon d’entrée. Pour le rendu vidéo, la mémoire tampon de sortie est susceptible de se trouver sur la carte graphique, où les opérations de lecture sont beaucoup plus lentes, par rapport aux opérations de lecture dans la mémoire principale.

## <a name="run-the-graph"></a>Exécuter le Graph

L’exemple de la accroche fonctionne dans l’un des deux modes suivants :

-   Le mode de mise en mémoire tampon effectue une copie de chaque exemple avant de transmettre l’exemple en aval.
-   Le mode de rappel appelle une fonction de rappel définie par l’application sur chaque échantillon.

Cet article décrit le mode de mise en mémoire tampon. (Avant d’utiliser le mode rappel, sachez que la fonction de rappel doit être assez limitée. Dans le cas contraire, elle peut réduire considérablement les performances, voire entraîner des interblocages. Pour plus d’informations, consultez [**ISampleGrabber :: SetCallback**](isamplegrabber-setcallback.md).) Pour activer le mode de mise en mémoire tampon, appelez la méthode [**ISampleGrabber :: SetBufferSamples**](isamplegrabber-setbuffersamples.md) avec la valeur **true**.

Si vous le souhaitez, appelez la méthode [**ISampleGrabber :: SetOneShot**](isamplegrabber-setoneshot.md) avec la valeur **true**. Cela provoque l’arrêt de la capture de l’exemple après avoir reçu le premier exemple de support, ce qui est utile si vous souhaitez récupérer une image unique à partir du flux. Recherchez l’heure souhaitée, exécutez le graphique et attendez la [**\_ fin**](ec-complete.md) de l’événement ce. Notez que le niveau de précision du frame dépend de la source. Par exemple, la recherche d’un fichier MPEG n’est souvent pas correcte.

pour exécuter le graphique aussi rapidement que possible, activez l’horloge du graphique comme décrit dans [définition de l’horloge du Graph](setting-the-graph-clock.md).

L’exemple suivant active le mode de mise en mémoire tampon et le mode à une seule capture, exécute le graphique de filtre et attend la fin de l’exécution.


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



## <a name="grab-the-sample"></a>Extraire l’exemple

En mode de mise en mémoire tampon, l’exemple de la accroche stocke une copie de chaque exemple. La méthode [**ISampleGrabber :: GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) copie la mémoire tampon dans un tableau alloué par l’appelant. Pour déterminer la taille du tableau nécessaire, appelez d’abord **GetCurrentBuffer** avec un pointeur **null** pour l’adresse du tableau. Allouez ensuite le tableau et appelez la méthode une deuxième fois pour copier la mémoire tampon. L'exemple suivant affiche ces étapes.


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



Vous devez connaître le format exact des données dans la mémoire tampon. Pour récupérer ces informations, appelez la méthode [**ISampleGrabber :: GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) . Cette méthode remplit une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) avec le format.

Pour un flux vidéo non compressé, les informations de format sont contenues dans une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) . L’exemple suivant montre comment obtenir les informations de mise en forme d’un flux vidéo non compressé.


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
> L’exemple de la accroche ne prend pas en charge [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).

 

## <a name="example-code"></a>Exemple de code

Voici le code complet pour les exemples précédents.

> [!Note]  
> Cet exemple utilise la fonction [SafeRelease](../medfound/saferelease.md) pour libérer des pointeurs d’interface.

 


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





## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[utilisation des Services de modification DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 
