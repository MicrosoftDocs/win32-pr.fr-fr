---
description: Cette rubrique est l’étape 4 de la lecture audio/vidéo du didacticiel dans DirectShow.
ms.assetid: 34f35a95-1981-4467-a581-46db96c05224
title: 'Étape 4 : ajouter le convertisseur vidéo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae2d73dce5bba34f92c8df59cd9730ef1e25b57b9757039d9bda5c2e4432d734
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051409"
---
# <a name="step-4-add-the-video-renderer"></a>Étape 4 : ajouter le convertisseur vidéo

Cette rubrique est l’étape 4 de la [lecture audio/vidéo du didacticiel dans DirectShow](audio-video-playback-in-directshow.md). le code complet est présenté dans la rubrique [exemple de lecture DirectShow](directshow-playback-example.md).

DirectShow fournit plusieurs filtres différents qui restituent la vidéo :

-   [**Filtre de convertisseur vidéo amélioré**](enhanced-video-renderer-filter.md) (EVR)
-   [Filtre de convertisseur de mixage vidéo 9](video-mixing-renderer-filter-9.md) (VMR-9)
-   [Filtre de convertisseur de mixage vidéo 7](video-mixing-renderer-filter-7.md) (VMR-7)

Pour plus d’informations sur les différences entre ces filtres, consultez [choix du convertisseur vidéo approprié](choosing-the-right-renderer.md).

Dans ce didacticiel, chaque filtre de convertisseur vidéo est encapsulé par une classe qui soustrait certaines des différences entre eux. Ces classes dérivent toutes d’une classe de base abstraite nommée `CVideoRenderer` . La déclaration de `CVideoRenderer` est indiquée à l' [étape 2 : déclarer CVideoRenderer et les classes dérivées](step-2--declare-cvideorenderer-and-derived-classes.md).

La méthode suivante tente de créer chaque convertisseur vidéo à son tour, en commençant par EVR, puis VMR-9 et enfin VMR-7.


```C++
HRESULT DShowPlayer::CreateVideoRenderer()
{
    HRESULT hr = E_FAIL;

    enum { Try_EVR, Try_VMR9, Try_VMR7 };

    for (DWORD i = Try_EVR; i <= Try_VMR7; i++)
    {
        switch (i)
        {
        case Try_EVR:
            m_pVideo = new (std::nothrow) CEVR();
            break;

        case Try_VMR9:
            m_pVideo = new (std::nothrow) CVMR9();
            break;

        case Try_VMR7:
            m_pVideo = new (std::nothrow) CVMR7();
            break;
        }

        if (m_pVideo == NULL)
        {
            hr = E_OUTOFMEMORY;
            break;
        }

        hr = m_pVideo->AddToGraph(m_pGraph, m_hwnd);
        if (SUCCEEDED(hr))
        {
            break;
        }

        delete m_pVideo;
        m_pVideo = NULL;
    }
    return hr;
}

```



### <a name="evr-filter"></a>Filtre EVR

Le code suivant crée le filtre EVR et l’ajoute au graphique de filtre. La fonction `AddFilterByCLSID` utilisée dans cet exemple est présentée dans la rubrique [Ajouter un filtre par CLSID](add-a-filter-by-clsid.md).


```C++
HRESULT CEVR::AddToGraph(IGraphBuilder *pGraph, HWND hwnd)
{
    IBaseFilter *pEVR = NULL;

    HRESULT hr = AddFilterByCLSID(pGraph, CLSID_EnhancedVideoRenderer, 
        &pEVR, L"EVR");

    if (FAILED(hr))
    {
        goto done;
    }

    hr = InitializeEVR(pEVR, hwnd, &m_pVideoDisplay);
    if (FAILED(hr))
    {
        goto done;
    }

    // Note: Because IMFVideoDisplayControl is a service interface,
    // you cannot QI the pointer to get back the IBaseFilter pointer.
    // Therefore, we need to cache the IBaseFilter pointer.

    m_pEVR = pEVR;
    m_pEVR->AddRef();

done:
    SafeRelease(&pEVR);
    return hr;
}
```



La `InitializeEVR` fonction initialise le filtre EVR. Cette fonction effectue les étapes suivantes.

1.  Interroge le filtre de l’interface [**IMFGetService**](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) .
2.  Appelle [**IMFGetService :: GetService**](/windows/win32/api/mfidl/nf-mfidl-imfgetservice-getservice) pour obtenir un pointeur vers l’interface [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) .
3.  Appelle [**IMFVideoDisplayControl :: SetVideoWindow**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) pour définir la fenêtre vidéo.
4.  Appelle [**IMFVideoDisplayControl :: SetAspectRatioMode**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setaspectratiomode) pour configurer le EVR afin de conserver les proportions vidéo.

Le code suivant illustre la `InitializeEVR` fonction.


```C++
HRESULT InitializeEVR( 
    IBaseFilter *pEVR,              // Pointer to the EVR
    HWND hwnd,                      // Clipping window
    IMFVideoDisplayControl** ppDisplayControl
    ) 
{ 
    IMFGetService *pGS = NULL;
    IMFVideoDisplayControl *pDisplay = NULL;

    HRESULT hr = pEVR->QueryInterface(IID_PPV_ARGS(&pGS)); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGS->GetService(MR_VIDEO_RENDER_SERVICE, IID_PPV_ARGS(&pDisplay));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the clipping window.
    hr = pDisplay->SetVideoWindow(hwnd);
    if (FAILED(hr))
    {
        goto done;
    }

    // Preserve aspect ratio by letter-boxing
    hr = pDisplay->SetAspectRatioMode(MFVideoARMode_PreservePicture);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the IMFVideoDisplayControl pointer to the caller.
    *ppDisplayControl = pDisplay;
    (*ppDisplayControl)->AddRef();

done:
    SafeRelease(&pGS);
    SafeRelease(&pDisplay);
    return hr; 
} 
```



Une fois le graphique construit, les `DShowPlayer::RenderStreams` appels `CVideoRenderer::FinalizeGraph` . Cette méthode effectue toute initialisation ou nettoyage final. Le code suivant illustre l' `CEVR` implémentation de cette méthode.


```C++
HRESULT CEVR::FinalizeGraph(IGraphBuilder *pGraph)
{
    if (m_pEVR == NULL)
    {
        return S_OK;
    }

    BOOL bRemoved;
    HRESULT hr = RemoveUnconnectedRenderer(pGraph, m_pEVR, &bRemoved);
    if (bRemoved)
    {
        SafeRelease(&m_pEVR);
        SafeRelease(&m_pVideoDisplay);
    }
    return hr;
}
```



Si le EVR n’est connecté à aucun autre filtre, cette méthode supprime le EVR du graphique. Cela peut se produire si le fichier multimédia ne contient pas de flux vidéo.

### <a name="vmr-9-filter"></a>Filtre VMR-9

Le code suivant crée le filtre VMR-9 et l’ajoute au graphique de filtre.


```C++
HRESULT CVMR9::AddToGraph(IGraphBuilder *pGraph, HWND hwnd)
{
    IBaseFilter *pVMR = NULL;

    HRESULT hr = AddFilterByCLSID(pGraph, CLSID_VideoMixingRenderer9, 
        &pVMR, L"VMR-9");
    if (SUCCEEDED(hr))
    {
        // Set windowless mode on the VMR. This must be done before the VMR 
        // is connected.
        hr = InitWindowlessVMR9(pVMR, hwnd, &m_pWindowless);
    }
    SafeRelease(&pVMR);
    return hr;
}
```



La `InitWindowlessVMR9` fonction initialise VMR-9 en mode sans fenêtre. (Pour plus d’informations sur le mode sans fenêtre, consultez [mode sans fenêtre VMR](vmr-windowless-mode.md).) Cette fonction effectue les étapes suivantes.

1.  Interroge le filtre VMR-9 pour l’interface [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) .
2.  Appelle la méthode [**IVMRFilterConfig9 :: SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) pour définir le mode sans fenêtre.
3.  Interroge le filtre VMR-9 pour l’interface [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .
4.  Appelle la méthode [**IVMRWindowlessControl9 :: SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) pour définir la fenêtre vidéo.
5.  Appelle la méthode [**IVMRWindowlessControl9 :: SetAspectRatioMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setaspectratiomode) pour conserver les proportions vidéo.

Le code suivant illustre la `InitWindowlessVMR9` fonction.


```C++
HRESULT InitWindowlessVMR9( 
    IBaseFilter *pVMR,              // Pointer to the VMR
    HWND hwnd,                      // Clipping window
    IVMRWindowlessControl9** ppWC   // Receives a pointer to the VMR.
    ) 
{ 

    IVMRFilterConfig9 * pConfig = NULL; 
    IVMRWindowlessControl9 *pWC = NULL;

    // Set the rendering mode.  
    HRESULT hr = pVMR->QueryInterface(IID_PPV_ARGS(&pConfig)); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pConfig->SetRenderingMode(VMR9Mode_Windowless); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Query for the windowless control interface.
    hr = pVMR->QueryInterface(IID_PPV_ARGS(&pWC));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the clipping window.
    hr = pWC->SetVideoClippingWindow(hwnd);
    if (FAILED(hr))
    {
        goto done;
    }

    // Preserve aspect ratio by letter-boxing
    hr = pWC->SetAspectRatioMode(VMR9ARMode_LetterBox);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the IVMRWindowlessControl pointer to the caller.
    *ppWC = pWC;
    (*ppWC)->AddRef();

done:
    SafeRelease(&pConfig);
    SafeRelease(&pWC);
    return hr; 
} 
```



La `CVMR9::FinalizeGraph` méthode vérifie si le filtre VMR-9 est connecté et, dans le cas contraire, le supprime du graphique de filtre.


```C++
HRESULT CVMR9::FinalizeGraph(IGraphBuilder *pGraph)
{
    if (m_pWindowless == NULL)
    {
        return S_OK;
    }

    IBaseFilter *pFilter = NULL;

    HRESULT hr = m_pWindowless->QueryInterface(IID_PPV_ARGS(&pFilter));
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL bRemoved;
    hr = RemoveUnconnectedRenderer(pGraph, pFilter, &bRemoved);

    // If we removed the VMR, then we also need to release our 
    // pointer to the VMR's windowless control interface.
    if (bRemoved)
    {
        SafeRelease(&m_pWindowless);
    }

done:
    SafeRelease(&pFilter);
    return hr;
}
```



### <a name="vmr-7-filter"></a>Filtre VMR-7

Les étapes pour le filtre VMR-7 sont quasiment identiques à celles de VMR-9, sauf que les interfaces VMR-7 sont utilisées à la place. Le code suivant crée le filtre VMR-7 et l’ajoute au graphique de filtre.


```C++
HRESULT CVMR7::AddToGraph(IGraphBuilder *pGraph, HWND hwnd)
{
    IBaseFilter *pVMR = NULL;

    HRESULT hr = AddFilterByCLSID(pGraph, CLSID_VideoMixingRenderer, 
        &pVMR, L"VMR-7");

    if (SUCCEEDED(hr))
    {
        // Set windowless mode on the VMR. This must be done before the VMR
        // is connected.
        hr = InitWindowlessVMR(pVMR, hwnd, &m_pWindowless);
    }
    SafeRelease(&pVMR);
    return hr;
}
```



La `InitWindowlessVMR` fonction initialise VMR-7 en mode sans fenêtre. Cette fonction effectue les étapes suivantes.

1.  Interroge le filtre VMR-7 pour l’interface [**IVMRFilterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig) .
2.  Appelle la méthode [**IVMRFilterConfig :: SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) pour définir le mode sans fenêtre.
3.  Interroge le filtre VMR-7 pour l’interface [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) .
4.  Appelle la méthode [**IVMRWindowlessControl :: SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) pour définir la fenêtre vidéo.
5.  Appelle la méthode [**IVMRWindowlessControl :: SetAspectRatioMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setaspectratiomode) pour conserver les proportions vidéo.

Le code suivant illustre la `InitWindowlessVMR` fonction.


```C++
HRESULT InitWindowlessVMR( 
    IBaseFilter *pVMR,              // Pointer to the VMR
    HWND hwnd,                      // Clipping window
    IVMRWindowlessControl** ppWC    // Receives a pointer to the VMR.
    ) 
{ 

    IVMRFilterConfig* pConfig = NULL; 
    IVMRWindowlessControl *pWC = NULL;

    // Set the rendering mode.  
    HRESULT hr = pVMR->QueryInterface(IID_PPV_ARGS(&pConfig)); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pConfig->SetRenderingMode(VMRMode_Windowless); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Query for the windowless control interface.
    hr = pVMR->QueryInterface(IID_PPV_ARGS(&pWC));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the clipping window.
    hr = pWC->SetVideoClippingWindow(hwnd);
    if (FAILED(hr))
    {
        goto done;
    }

    // Preserve aspect ratio by letter-boxing
    hr = pWC->SetAspectRatioMode(VMR_ARMODE_LETTER_BOX);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the IVMRWindowlessControl pointer to the caller.
    *ppWC = pWC;
    (*ppWC)->AddRef();

done:
    SafeRelease(&pConfig);
    SafeRelease(&pWC);
    return hr; 
} 
```



La `CVMR7::FinalizeGraph` méthode vérifie si le filtre VMR-7 est connecté et, dans le cas contraire, le supprime du graphique de filtre.


```C++
HRESULT CVMR7::FinalizeGraph(IGraphBuilder *pGraph)
{
    if (m_pWindowless == NULL)
    {
        return S_OK;
    }

    IBaseFilter *pFilter = NULL;

    HRESULT hr = m_pWindowless->QueryInterface(IID_PPV_ARGS(&pFilter));
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL bRemoved;
    hr = RemoveUnconnectedRenderer(pGraph, pFilter, &bRemoved);

    // If we removed the VMR, then we also need to release our 
    // pointer to the VMR's windowless control interface.
    if (bRemoved)
    {
        SafeRelease(&m_pWindowless);
    }

done:
    SafeRelease(&pFilter);
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Exemple de lecture](directshow-playback-example.md)
</dt> <dt>

[utilisation du filtre EVR DirectShow](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[Utilisation du convertisseur de mixage vidéo](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
