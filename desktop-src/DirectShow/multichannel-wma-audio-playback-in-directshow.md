---
description: Lecture audio WMA Multichannel dans DirectShow
ms.assetid: 99c69290-545a-4368-8f51-74e547c9466d
title: Lecture audio WMA Multichannel dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 400ee9f0cede6c7268bcd3632365db1b423d114e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317726"
---
# <a name="multichannel-wma-audio-playback-in-directshow"></a><span data-ttu-id="e9693-103">Lecture audio WMA Multichannel dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="e9693-103">Multichannel WMA Audio Playback in DirectShow</span></span>

<span data-ttu-id="e9693-104">Pour lire un fichier de Windows Media Audio multicanal dans DirectShow, vous devez définir la propriété **MFPKEY \_ WMADEC \_ HIRESOUTPUT** directement sur le décodeur une fois qu’il a été connecté au lecteur ASF WM.</span><span class="sxs-lookup"><span data-stu-id="e9693-104">To play back a multichannel Windows Media Audio file in DirectShow, you must set the **MFPKEY\_WMADEC\_HIRESOUTPUT** property directly on the decoder after it has been connected to the WM ASF Reader.</span></span> <span data-ttu-id="e9693-105">Cette propriété est définie dans le fichier d’en-tête wmcodecdsp. h, qui est disponible dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="e9693-105">This property is defined in the header file wmcodecdsp.h, which is available in the Windows SDK.</span></span>

> [!Note]  
> <span data-ttu-id="e9693-106">Cette procédure de configuration est prise en charge uniquement pour les fichiers qui ne sont pas protégés par le Rights Management numérique.</span><span class="sxs-lookup"><span data-stu-id="e9693-106">This configuration procedure is supported only for files that are not protected by Digital Rights Management.</span></span>

 

<span data-ttu-id="e9693-107">Les étapes de base pour activer la sortie multicanal sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e9693-107">The basic steps to enable multichannel output are as follows:</span></span>

1.  <span data-ttu-id="e9693-108">Appelez **RenderFile** pour créer le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="e9693-108">Call **RenderFile** to create the filter graph.</span></span>
2.  <span data-ttu-id="e9693-109">Obtenez un pointeur vers le filtre de wrappers DMO.</span><span class="sxs-lookup"><span data-stu-id="e9693-109">Obtain a pointer to the DMO Wrapper filter.</span></span>
3.  <span data-ttu-id="e9693-110">Déconnectez le wrapper DMO du convertisseur audio.</span><span class="sxs-lookup"><span data-stu-id="e9693-110">Disconnect the DMO Wrapper from the Audio Renderer.</span></span>
4.  <span data-ttu-id="e9693-111">Utilisez l’interface **IPropertyBag** pour définir la **propriété \_ \_ HIRESOUTPUT WMADEC MFPKEY** sur le décodeur.</span><span class="sxs-lookup"><span data-stu-id="e9693-111">Use the **IPropertyBag** interface to set the **MFPKEY\_WMADEC\_HIRESOUTPUT** property on the decoder.</span></span> <span data-ttu-id="e9693-112">Le nom de la propriété est défini par la constante globale **g \_ wszWMACHiResOutput**.</span><span class="sxs-lookup"><span data-stu-id="e9693-112">The property name is defined by the global constant **g\_wszWMACHiResOutput**.</span></span>
5.  <span data-ttu-id="e9693-113">Reconnectez le wrapper DMO et le convertisseur audio.</span><span class="sxs-lookup"><span data-stu-id="e9693-113">Reconnect the DMO Wrapper and the Audio Renderer.</span></span>
6.  <span data-ttu-id="e9693-114">Exécutez le graphique.</span><span class="sxs-lookup"><span data-stu-id="e9693-114">Run the graph.</span></span>

<span data-ttu-id="e9693-115">Les extraits de code suivants illustrent ces étapes.</span><span class="sxs-lookup"><span data-stu-id="e9693-115">The following code snippets demonstrate these steps.</span></span> <span data-ttu-id="e9693-116">Ce code suppose que le fichier source contient un flux audio et aucun flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="e9693-116">This code assumes that the source file contains an audio stream and no video stream.</span></span> <span data-ttu-id="e9693-117">Le codec vidéo DMO ne prend pas en charge la propriété **MFPKEY \_ WMADEC \_ HIRESOUTPUT** .</span><span class="sxs-lookup"><span data-stu-id="e9693-117">The video codec DMO does not support the **MFPKEY\_WMADEC\_HIRESOUTPUT** property.</span></span>


```C++
HRESULT BuildGraph(IGraphBuilder *pGraph, const WCHAR *wFileName)
{
    HRESULT hr = S_OK;
    IBaseFilter       *pDmoWrapper = NULL;
    IPin              *pDmoOut = NULL;
    IPin              *pRendererIn = NULL;
    IPropertyBag      *pPropBag = NULL;

    hr = pGraph->RenderFile(wFileName, NULL);

    // Get pointers to the two DMO Wrapper interfaces we need.
    // (Function bodies provided at the end of this snippet.)
    if (SUCCEEDED(hr))
    {
        hr = GetDMOWrapper(pGraph, &pDmoWrapper); 
    }

    //Disconnect the DMO Wrapper from the Audio Renderer.
    if (SUCCEEDED(hr))
    {
        hr = GetPin(pDmoWrapper, PINDIR_OUTPUT, &pDmoOut);
    }
    if (SUCCEEDED(hr))
    {
        hr = DisconnectPin(pGraph, pDmoOut, &pRendererIn);
    }

    //Set the property on the DMO.
    VARIANT varg;
    ::VariantInit(&varg);
    varg.vt    = VT_BOOL;
    varg.boolVal = TRUE;

    if (SUCCEEDED(hr))
    {
        hr = pDmoWrapper->QueryInterface(IID_IPropertyBag, (void**)&pPropBag);
    }
    if (SUCCEEDED(hr))
    {
        hr = pPropBag->Write(g_wszWMACHiResOutput, &varg);
    }

    // Reconnect the DMO Wrapper and the Audio Renderer
    if (SUCCEEDED(hr))
    {
        hr = pGraph->Connect(pDmoOut, pRendererIn);
    }

    SAFE_RELEASE(pDmoWrapper);
    SAFE_RELEASE(pDmoOut);
    SAFE_RELEASE(pRendererIn);
    SAFE_RELEASE(pPropBag);
    return hr;
}
```



<span data-ttu-id="e9693-118">Les fonctions d’assistance de l’extrait de code précédent sont implémentées comme suit :</span><span class="sxs-lookup"><span data-stu-id="e9693-118">The helper functions from the previous code snippet are implemented as follows:</span></span>


```C++
HRESULT GetDMOWrapper (IFilterGraph *pGraph, IBaseFilter** ppFilter) 
{
    BOOL bFound = FALSE;

    IEnumFilters *pEnum = NULL;
    IBaseFilter *pFilter = NULL;
    IDMOWrapperFilter *pWrapper = NULL;

    HRESULT hr = pGraph->EnumFilters(&pEnum);
    if (SUCCEEDED(hr))
    {
        while(pEnum->Next(1, &pFilter, NULL) == S_OK)
        {
            // If we find the IDMOWrapperFilter interface, that means we 
            // have the DMO Wrapper filter. 
            hr = pFilter->QueryInterface(IID_IDMOWrapperFilter, (void**) &pWrapper);
            if (SUCCEEDED(hr))
            {
                bFound = TRUE;
                break;
            }
            SAFE_RELEASE(pFilter);
        }
    }

    if (bFound)
    {
        *ppFilter = pFilter;
        (*ppFilter)->AddRef();
    }
    else
    {
        hr = E_FAIL;
    }

    SAFE_RELEASE(pEnum);
    SAFE_RELEASE(pFilter);
    SAFE_RELEASE(pWrapper);
    return hr;
}

HRESULT GetPin(IBaseFilter *pFilter, PIN_DIRECTION PinDir, IPin** ppPin)
{
    BOOL bFound = FALSE;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;

    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (SUCCEEDED(hr))
    {
        while(pEnum->Next(1, &pPin, 0) == S_OK)
        {
            PIN_DIRECTION PinDirThis;
            hr = pPin->QueryDirection(&PinDirThis);
            if (FAILED(hr))
            {
                break;
            }
            if (PinDir == PinDirThis)
            {
                bFound = TRUE;
                break;
            }
            SAFE_RELEASE(pPin);
        }
    }

    if (bFound)
    {
        *ppPin = pPin;
        (*ppPin)->AddRef();
    }
    else
    {
        hr = E_FAIL;
    }

    SAFE_RELEASE(pPin);
    SAFE_RELEASE(pEnum);
    return hr;
}

HRESULT DisconnectPin(IGraphBuilder *pGraph, IPin *pPin, IPin **ppConnected)
{
    IPin *pConnected = NULL;

    HRESULT hr = pPin->ConnectedTo(&pConnected);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->Disconnect(pPin);
    }
    if (SUCCEEDED(hr))
    {
        hr = pGraph->Disconnect(pConnected);
    }
    if (SUCCEEDED(hr))
    {
        *ppConnected = pConnected;
        (*ppConnected)->AddRef();
    }

    SAFE_RELEASE(pConnected);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="e9693-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e9693-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9693-120">Lecture de fichiers ASF dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="e9693-120">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



