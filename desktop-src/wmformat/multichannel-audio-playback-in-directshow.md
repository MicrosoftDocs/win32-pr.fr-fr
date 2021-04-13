---
title: Lecture audio multicanal dans DirectShow
description: Lecture audio multicanal dans DirectShow
ms.assetid: 5123854a-0f1f-40f4-bf57-47622b91103f
keywords:
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, lecture audio multicanal
- Windows Media Format SDK, lecture audio
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- ASF (Advanced Systems Format), lecture audio multicanal
- ASF (format de systèmes avancés), lecture audio multicanal
- ASF (Advanced Systems Format), lecture audio
- ASF (format des systèmes avancés), lecture audio
- DirectShow, lecture audio multicanal
- DirectShow, lecture audio
- audio multicanal, lecture
- lecture audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d44c6eec473c8bbbff81d35f4127d5d132d0b6cd
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104381581"
---
# <a name="multichannel-audio-playback-in-directshow"></a><span data-ttu-id="17d5b-116">Lecture audio multicanal dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="17d5b-116">Multichannel Audio Playback in DirectShow</span></span>

<span data-ttu-id="17d5b-117">Pour lire un fichier de Windows Media Audio multicanal dans DirectShow, vous devez définir la \_ propriété « HIRESOUTPUT » directement sur le décodeur une fois qu’il a été connecté au lecteur ASF WM.</span><span class="sxs-lookup"><span data-stu-id="17d5b-117">To play back a multichannel Windows Media Audio file in DirectShow, you must set the "\_HIRESOUTPUT" property directly on the decoder after it has been connected to the WM ASF Reader.</span></span> <span data-ttu-id="17d5b-118">Aucune configuration de l’objet lecteur n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="17d5b-118">No configuration of the Reader Object is necessary.</span></span> <span data-ttu-id="17d5b-119">Toutefois, pour travailler directement avec la solution DMO, vous avez besoin de wmcodecconst. h dans l' [exemple de code pour l’utilisation du package de téléchargement des interfaces de codec vidéo et Windows Media Audio](https://www.microsoft.com/downloads/details.aspx?FamilyId=92490D8A-4F2E-46F1-8835-B1D987B3C985&displaylang=en) .</span><span class="sxs-lookup"><span data-stu-id="17d5b-119">However, to work with the DMO directly, you need wmcodecconst.h from the [Sample Code for Using the Windows Media Audio and Video Codec Interfaces](https://www.microsoft.com/downloads/details.aspx?FamilyId=92490D8A-4F2E-46F1-8835-B1D987B3C985&displaylang=en) download package.</span></span>

<span data-ttu-id="17d5b-120">**Remarque** Cette procédure de configuration est prise en charge uniquement pour les fichiers qui ne sont pas protégés par le Rights Management numérique.</span><span class="sxs-lookup"><span data-stu-id="17d5b-120">**Note** This configuration procedure is supported only for files that are not protected by Digital Rights Management.</span></span>

<span data-ttu-id="17d5b-121">Les étapes de base pour activer la sortie multicanal sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="17d5b-121">The basic steps to enable multichannel output are as follows:</span></span>

1.  <span data-ttu-id="17d5b-122">Appelez RenderFile pour créer le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="17d5b-122">Call RenderFile to create the filter graph.</span></span>
2.  <span data-ttu-id="17d5b-123">Obtenir un pointeur vers le filtre de wrappers DMO</span><span class="sxs-lookup"><span data-stu-id="17d5b-123">Obtain a pointer to the DMO Wrapper filter</span></span>
3.  <span data-ttu-id="17d5b-124">Déconnecter le wrapper DMO du convertisseur audio</span><span class="sxs-lookup"><span data-stu-id="17d5b-124">Disconnect the DMO Wrapper from the Audio Renderer</span></span>
4.  <span data-ttu-id="17d5b-125">Définissez la \_ propriété « HIRESOUTPUT » sur le décodeur.</span><span class="sxs-lookup"><span data-stu-id="17d5b-125">Set the "\_HIRESOUTPUT" property on the decoder.</span></span>
5.  <span data-ttu-id="17d5b-126">Reconnectez le wrapper DMO et le convertisseur audio.</span><span class="sxs-lookup"><span data-stu-id="17d5b-126">Reconnect the DMO Wrapper and the Audio Renderer.</span></span>
6.  <span data-ttu-id="17d5b-127">Exécutez le graphique.</span><span class="sxs-lookup"><span data-stu-id="17d5b-127">Run the graph.</span></span>

<span data-ttu-id="17d5b-128">Les extraits de code suivants illustrent ces étapes.</span><span class="sxs-lookup"><span data-stu-id="17d5b-128">The following code snippets demonstrate these steps.</span></span> <span data-ttu-id="17d5b-129">(Toutes les vérifications d’erreurs ont été omises par souci de simplicité.</span><span class="sxs-lookup"><span data-stu-id="17d5b-129">(All error checking has been omitted for the sake of simplicity.</span></span> <span data-ttu-id="17d5b-130">Si vous utilisez ce code dans une application, vous devez ajouter les routines de gestion des erreurs appropriées.</span><span class="sxs-lookup"><span data-stu-id="17d5b-130">You should add proper error handling routines if you use this code in an application.)</span></span>


```C++
    ...
    //ENABLE MULTICHANNEL OUTPUT
    //Render the file
    hr = m_pGraphBuilder->RenderFile(wFileName, NULL);

    // Get pointers to the two DMO Wrapper interfaces we need.
    // (Function bodies provided at the end of this snippet.)
    hr = GetDMOWrapper(pGB, &m_pDMOBaseFilter, &m_pWrapper); 

    //Disconnect the DMO Wrapper from the Audio Renderer
    CComPtr<IPin> pDMOOut;
    CComPtr<IPin> pRendererIn;
    hr = GetPin(m_pDMOBaseFilter, PINDIR_OUTPUT, &pDMOOut);
    hr = pDMOOut->ConnectedTo(&pRendererIn);
    hr = pDMOOut->Disconnect();
    hr = pRendererIn->Disconnect();

    //Set the property on the DMO
    VARIANT varg;
    ::VariantInit(&varg);
    varg.vt    = VT_BOOL;
    varg.boolVal = TRUE;
    CComQIPtr<IMediaObject, &IID_IMediaObject> pMediaObject(m_pWrapper);
    CComQIPtr<IPropertyBag, &IID_IPropertyBag> pPropertyBag(pMediaObject);
    hr = pPropertyBag->Write(g_wszWMACHiResOutput, &varg);

    // Reconnect the DMO Wrapper and the Audio Renderer
    hr = pGB->Connect(pDMOOut, pRendererIn);
    //END MULTICHANNEL (now the graph can be run)
...

```



<span data-ttu-id="17d5b-131">Les fonctions GetDMOWrapper et GetPin de l’extrait de code précédent sont implémentées comme suit :</span><span class="sxs-lookup"><span data-stu-id="17d5b-131">The GetDMOWrapper and GetPin functions from the previous code snippet are implemented as follows:</span></span>


```C++
// In this example, the IBaseFilter and IDMOWrapperFilter interfaces are
// declared  at global scope
HRESULT GetDMOWrapper (IFilterGraph *pGraph, IBaseFilter** m_pDMOBaseFilter, IDMOWrapperFilter** m_pWrapper) 
{
    CComPtr<IEnumFilters> pEnum;
    CComPtr<IBaseFilter> pFilter;
    ULONG cFetched;

    HRESULT hr = pGraph->EnumFilters(&pEnum);
    if (FAILED(hr)) return hr;

    while(pEnum->Next(1, &pFilter, &cFetched) == S_OK)
    {
        // If we find the IDMOWrapperFilter interface, that means we 
        // have the DMO Wrapper filter. Store both interfaces for future use.
        CComPtr<IDMOWrapperFilter> pWrapper;
        hr = pFilter->QueryInterface(IID_IDMOWrapperFilter, (void**) &pWrapper);
        if (SUCCEEDED(hr))
        {
            *m_pWrapper = pWrapper.Detach();
            *m_pDMOBaseFilter = pFilter.Detach();
            return S_OK;
        }

        pFilter.Release();
    }

    return E_FAIL;
}

HRESULT GetPin(IBaseFilter *pFilter, PIN_DIRECTION PinDir, IPin** ppPin)
{
    CComPtr<IEnumPins>  pEnum;
    CComPtr<IPin>       pPin;

         HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        return hr;
    }
    while(pEnum->Next(1, &pPin, 0) == S_OK)
    {
        PIN_DIRECTION PinDirThis;
        pPin->QueryDirection(&PinDirThis);
        if (PinDir == PinDirThis)
        {
            *ppPin = pPin.Detach();
            return S_OK;
        }
        pPin.Release();
    }
    
    return E_FAIL;
}
```



 

 




