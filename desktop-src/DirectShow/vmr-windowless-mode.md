---
description: Mode sans fenêtre VMR
ms.assetid: 0dc871d2-79c4-4bf8-96ef-13c4d1ab4497
title: Mode sans fenêtre VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193f672e0fc1e3dced4bdff16da0e85123079eb94f2ac3c5fdb302b67c9432b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830582"
---
# <a name="vmr-windowless-mode"></a>Mode sans fenêtre VMR

Le mode sans fenêtre est la méthode recommandée pour que les applications affichent des vidéos dans une fenêtre d’application. En mode sans fenêtre, le convertisseur de mixage vidéo ne charge pas son composant de gestionnaire de fenêtres et ne prend donc pas en charge les interfaces [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) ou [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) . Au lieu de cela, l’application fournit la fenêtre de lecture et définit un rectangle de destination dans la zone cliente pour que VMR dessine la vidéo. VMR utilise un objet DirectDraw Clipper pour s’assurer que la vidéo est tronquée à la fenêtre de l’application et qu’elle n’apparaît pas sur les autres fenêtres. VMR ne sous-classe pas la fenêtre de l’application ou n’installe pas de raccordements système/processus.

En mode sans fenêtre, la séquence d’événements pendant la connexion et la transition à l’état d’exécution sont les suivantes :

-   Le filtre amont propose un type de média, que VMR accepte ou rejette.
-   Si le type de média est accepté, VMR appelle l’Allocator-Presenter pour obtenir une surface DirectDraw. Si la surface est créée avec succès, les codes confidentiels se connectent et le VMR est prêt à passer à l’état d’exécution.
-   Lorsque le graphique de filtre s’exécute, le décodeur appelle **GetBuffer** pour obtenir un échantillon de support à partir de l’allocateur. VMR interroge l’Allocator-Presenter pour s’assurer que la profondeur de pixel, la taille du rectangle et d’autres paramètres sur sa surface DirectDraw sont compatibles avec la vidéo entrante. S’ils sont compatibles, VMR retourne la surface DirectDraw au décodeur. Une fois que le décodeur a décodé dans la surface, l’unité de synchronisation principale de VMR valide les horodatages. Cette unité bloque l’appel de **réception** jusqu’à ce que l’heure de la présentation arrive. À ce stade, VMR appelle **PresentImage** sur l’Allocator-Presenter, qui présente la surface à la carte graphique.

L’illustration suivante montre le VMR en mode sans fenêtre avec plusieurs flux d’entrée.

![VMR en mode sans fenêtre](images/vmr-windowless-mult-streams.png)

**Configuration de VMR-7 en mode sans fenêtre**

Pour configurer VMR-7 en mode sans fenêtre, effectuez toutes les étapes suivantes avant de connecter les broches d’entrée de VMR :

1.  Créez le filtre et ajoutez-le au graphique.
2.  Appelez la méthode [**IVMRFilterConfig :: SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) avec l' \_ indicateur sans fenêtre VMRMode.
3.  Éventuellement, configurez le VMR pour plusieurs flux d’entrée en appelant [**IVMRFilterConfig :: SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams). VMR crée une broche d’entrée pour chaque flux. Utilisez l’interface [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) pour définir l’ordre de plan et d’autres paramètres pour le flux. pour plus d’informations, consultez [VMR avec plusieurs Flux (Mode de mixage)](vmr-with-multiple-streams--mixing-mode.md).

    Si vous n’appelez pas **SetNumberOfStreams**, VMR-7 est défini par défaut sur une seule broche d’entrée. Une fois les broches d’entrée connectées, le nombre de broches ne peut pas être modifié.

4.  Appelez [**IVMRWindowlessControl :: SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) pour spécifier la fenêtre dans laquelle la vidéo rendue s’affichera.

Une fois ces étapes terminées, vous pouvez connecter les broches d’entrée du filtre VMR. il existe plusieurs façons de générer le graphique, par exemple en connectant des broches directement, à l’aide de méthodes de Connecter intelligentes telles que [**IGraphBuilder :: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), ou à l’aide de la méthode [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) du générateur de Capture Graph. Pour plus d’informations, consultez [General Graph-Building techniques](general-graph-building-techniques.md).

Pour définir la position de la vidéo dans la fenêtre de l’application, appelez la méthode [**IVMRWindowlessControl :: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) . La méthode [**IVMRWindowlessControl :: GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) retourne la taille de la vidéo native. pendant la lecture, l’application doit notifier VMR des messages Windows suivants :

-   WM \_ Paint : appelez [**IVMRWindowlessControl :: RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo) pour redessiner l’image.
-   WM \_ DISPLAYCHANGE : appelez [**IVMRWindowlessControl ::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged). VMR effectue toutes les actions nécessaires pour afficher la vidéo au niveau de la nouvelle résolution ou de la profondeur de couleurs.
-   \_Taille du WM : recalcule la position de la vidéo et appelle à nouveau [**SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) si nécessaire.

> [!Note]  
> Les applications MFC doivent définir un \_ Gestionnaire de messages WM ERASEBKGND vide ou la zone d’affichage vidéo ne se redessinera pas correctement.

 

**Configuration de VMR-9 en mode sans fenêtre**

Pour configurer VMR-9 en mode sans fenêtre, suivez les étapes décrites pour VMR-7 en mode sans fenêtre, mais utilisez les interfaces [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) et [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) . La seule différence significative est que VMR-9 crée par défaut quatre broches d’entrée au lieu d’une seule broche d’entrée. Par conséquent, il vous suffit d’appeler **SetNumberOfStreams** si vous mélangez plus de quatre flux vidéo.

**Exemple de code**

le code suivant montre comment créer un filtre vmr-7, l’ajouter au DirectShow graphique de filtre, puis mettre le VMR en mode sans fenêtre. Pour VMR-9, utilisez le CLSID \_ VideoMixingRenderer9 dans **CoCreateInstance** et les interfaces VMR-9 correspondantes.


```C++
HRESULT InitializeWindowlessVMR(
    HWND hwndApp,         // Application window.
    IFilterGraph* pFG,    // Pointer to the Filter Graph Manager.
    IVMRWindowlessControl** ppWc,  // Receives the interface.
    DWORD dwNumStreams,  // Number of streams to use.
    BOOL fBlendAppImage  // Are we alpha-blending a bitmap?
    )
{
    IBaseFilter* pVmr = NULL;
    IVMRWindowlessControl* pWc = NULL;
    *ppWc = NULL;

    // Create the VMR and add it to the filter graph.
    HRESULT hr = CoCreateInstance(CLSID_VideoMixingRenderer, NULL,
       CLSCTX_INPROC, IID_IBaseFilter, (void**)&pVmr);
    if (FAILED(hr))
    {
        return hr;
    }
    hr = pFG->AddFilter(pVmr, L"Video Mixing Renderer");
    if (FAILED(hr))
    {
        pVmr->Release();
        return hr;
    }

    // Set the rendering mode and number of streams.  
    IVMRFilterConfig* pConfig;
    hr = pVmr->QueryInterface(IID_IVMRFilterConfig, (void**)&pConfig);
    if (SUCCEEDED(hr)) 
    {
        pConfig->SetRenderingMode(VMRMode_Windowless);

        // Set the VMR-7 to mixing mode if you want more than one video
        // stream, or you want to mix a static bitmap over the video.
        // (The VMR-9 defaults to mixing mode with four inputs.)
        if (dwNumStreams > 1 || fBlendAppImage) 
        {
            pConfig->SetNumberOfStreams(dwNumStreams);
        }
        pConfig->Release();

        hr = pVmr->QueryInterface(IID_IVMRWindowlessControl, (void**)&pWc);
        if (SUCCEEDED(hr)) 
        {
            pWc->SetVideoClippingWindow(hwndApp);
            *ppWc = pWc;  // The caller must release this interface.
        }
    }
    pVmr->Release();

    // Now the VMR can be connected to other filters.
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du mode sans fenêtre](using-windowless-mode.md)
</dt> </dl>

 

 



