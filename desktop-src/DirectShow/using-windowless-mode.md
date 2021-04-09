---
description: Utilisation du mode sans fenêtre
ms.assetid: f53cecaa-dee7-4b02-a4ac-ffbd917f73aa
title: Utilisation du mode sans fenêtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393b112c6d340c3440521876da08111dd4bb0e81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866449"
---
# <a name="using-windowless-mode"></a>Utilisation du mode sans fenêtre

Le [filtre de convertisseur de mixage vidéo 7](video-mixing-renderer-filter-7.md) (VMR-7) et le [filtre de conversion vidéo Filter 9](video-mixing-renderer-filter-9.md) (VMR-9) prennent en charge le *mode sans fenêtre*, qui représente une amélioration majeure par rapport à l’interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) . Cette rubrique décrit les différences entre le mode sans fenêtre et le mode fenêtre, et l’utilisation du mode sans fenêtre.

Pour garantir une compatibilité descendante avec les applications existantes, VMR est par défaut en mode fenêtre. En mode fenêtre, le convertisseur crée sa propre fenêtre pour afficher la vidéo. En général, l’application définit la fenêtre vidéo en tant qu’enfant de la fenêtre d’application. L’existence d’une fenêtre vidéo distincte provoque certains problèmes, toutefois :

-   Plus important encore, il existe un risque de blocages si les messages de fenêtre sont envoyés entre les threads.
-   Le gestionnaire de graphique de filtre doit transférer certains messages de fenêtre, tels que WM \_ Paint, au convertisseur vidéo. L’application doit utiliser l’implémentation de [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) par le gestionnaire de graphique de filtre (et non pas les convertisseurs vidéo), afin que le gestionnaire de graphique de filtre conserve l’état interne correct.
-   Pour recevoir des événements de souris ou de clavier à partir de la fenêtre vidéo, l’application doit définir un *drain de message*, ce qui amène la fenêtre vidéo à transférer ces messages à l’application.
-   Pour éviter les problèmes de découpage, la fenêtre vidéo doit avoir les styles de fenêtre appropriés.

Le mode sans fenêtre permet d’éviter ces problèmes en faisant en sorte que VMR dessine directement dans la zone cliente de la fenêtre d’application, à l’aide de DirectDraw pour découper le rectangle vidéo. Le mode sans fenêtre réduit considérablement le risque d’interblocages. En outre, l’application n’a pas besoin de définir la fenêtre propriétaire ou les styles de fenêtre. En fait, quand VMR est en mode sans fenêtre, il n’expose même pas l’interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) , qui n’est plus nécessaire.

Pour utiliser le mode sans fenêtre, vous devez configurer explicitement VMR. Toutefois, vous constaterez que est plus flexible et plus facile à utiliser que le mode fenêtre.

Le filtre VMR-7 et le filtre VMR-9 exposent des interfaces différentes, mais les étapes sont équivalentes à chacune d’elles.

## <a name="configure-the-vmr-for-windowless-mode"></a>Configurer VMR pour le mode sans fenêtre

Pour remplacer le comportement par défaut de VMR, configurez le VMR avant de générer le graphique de filtre :

**VMR-7**

1.  Créez le gestionnaire de graphe de filtre.
2.  Créez VMR-7 et ajoutez-le au graphique de filtre.
3.  Appelez [**IVMRFilterConfig :: SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) sur VMR-7 avec l’indicateur **\_ sans fenêtre VMRMode** .
4.  Interrogez VMR-7 pour l’interface [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) .
5.  Appelez [**IVMRWindowlessControl :: SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) sur VMR-7. Spécifiez un handle vers la fenêtre dans laquelle la vidéo doit apparaître.

**VMR-9**

1.  Créez le gestionnaire de graphe de filtre.
2.  Créez VMR-9 et ajoutez-le au graphique de filtre.
3.  Appelez [**IVMRFilterConfig9 :: SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) sur VMR-9 avec l’indicateur **\_ sans fenêtre VMR9Mode** .
4.  Interrogez VMR-9 pour l’interface [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .
5.  Appelez [**IVMRWindowlessControl9 :: SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) sur VMR-9. Spécifiez un handle vers la fenêtre dans laquelle la vidéo doit apparaître.

Maintenant, générez le reste du graphique de filtre en appelant [**IGraphBuilder :: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) ou d’autres méthodes de création de graphiques. Le gestionnaire de graphique de filtre utilise automatiquement l’instance de VMR que vous avez ajoutée au graphique. (Pour plus d’informations sur la cause de ce problème, consultez [connexion intelligente](intelligent-connect.md).)

Le code suivant illustre une fonction d’assistance qui crée VMR-7, l’ajoute au graphique et configure le mode sans fenêtre.


```C++
HRESULT InitWindowlessVMR( 
    HWND hwndApp,                  // Window to hold the video. 
    IGraphBuilder* pGraph,         // Pointer to the Filter Graph Manager. 
    IVMRWindowlessControl** ppWc   // Receives a pointer to the VMR.
    ) 
{ 
    if (!pGraph || !ppWc) 
    {
        return E_POINTER;
    }
    IBaseFilter* pVmr = NULL; 
    IVMRWindowlessControl* pWc = NULL; 
    // Create the VMR. 
    HRESULT hr = CoCreateInstance(CLSID_VideoMixingRenderer, NULL, 
        CLSCTX_INPROC, IID_IBaseFilter, (void**)&pVmr); 
    if (FAILED(hr))
    {
        return hr;
    }
    
    // Add the VMR to the filter graph.
    hr = pGraph->AddFilter(pVmr, L"Video Mixing Renderer"); 
    if (FAILED(hr)) 
    {
        pVmr->Release();
        return hr;
    }
    // Set the rendering mode.  
    IVMRFilterConfig* pConfig; 
    hr = pVmr->QueryInterface(IID_IVMRFilterConfig, (void**)&pConfig); 
    if (SUCCEEDED(hr)) 
    { 
        hr = pConfig->SetRenderingMode(VMRMode_Windowless); 
        pConfig->Release(); 
    }
    if (SUCCEEDED(hr))
    {
        // Set the window. 
        hr = pVmr->QueryInterface(IID_IVMRWindowlessControl, (void**)&pWc);
        if( SUCCEEDED(hr)) 
        { 
            hr = pWc->SetVideoClippingWindow(hwndApp); 
            if (SUCCEEDED(hr))
            {
                *ppWc = pWc; // Return this as an AddRef'd pointer. 
            }
            else
            {
                // An error occurred, so release the interface.
                pWc->Release();
            }
        } 
    } 
    pVmr->Release(); 
    return hr; 
} 
```



Cette fonction suppose que n’affiche qu’un seul flux vidéo et ne combine pas une image bitmap statique sur la vidéo. Pour plus d’informations, consultez [mode sans fenêtre VMR](vmr-windowless-mode.md). Vous appelez cette fonction comme suit :


```C++
IVMRWindowlessControl *pWc = NULL;
hr = InitWindowlessVMR(hwnd, pGraph, &g_pWc);
if (SUCCEEDED(hr))
{
    // Build the graph. For example:
    pGraph->RenderFile(wszMyFileName, 0);
    // Release the VMR interface when you are done.
    pWc->Release();
}
```



## <a name="position-the-video"></a>Positionner la vidéo

Après avoir configuré VMR, l’étape suivante consiste à définir la position de la vidéo. Il y a deux rectangles à prendre en compte, le rectangle *source* et le rectangle de *destination* . Le rectangle source définit la partie de la vidéo à afficher. Le rectangle de destination spécifie la région dans la zone cliente de la fenêtre qui contiendra la vidéo. VMR découpe l’image vidéo dans le rectangle source et étire l’image rognée pour l’ajuster au rectangle de destination.

**VMR-7**

1.  Appelez la méthode [**IVMRWindowlessControl :: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) pour spécifier les deux rectangles.
2.  Le rectangle source doit être inférieur ou égal à la taille de la vidéo Native ; vous pouvez utiliser la méthode [**IVMRWindowlessControl :: GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) pour accéder à la taille vidéo native.

**VMR-9**

1.  Appelez la méthode [**IVMRWindowlessControl9 :: SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) pour spécifier les deux rectangles.
2.  Le rectangle source doit être inférieur ou égal à la taille de la vidéo Native ; vous pouvez utiliser la méthode [**IVMRWindowlessControl9 :: GetNativeVideoSize**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-getnativevideosize) pour accéder à la taille vidéo native.

Par exemple, le code suivant définit les rectangles source et de destination pour VMR-7. Il définit le rectangle source comme étant la totalité de l’image vidéo et le rectangle de destination sur la totalité de la zone cliente de la fenêtre :


```C++
// Find the native video size.
long lWidth, lHeight; 
HRESULT hr = g_pWc->GetNativeVideoSize(&lWidth, &lHeight, NULL, NULL); 
if (SUCCEEDED(hr))
{
    RECT rcSrc, rcDest; 
    // Set the source rectangle.
    SetRect(&rcSrc, 0, 0, lWidth, lHeight); 
    
    // Get the window client area.
    GetClientRect(hwnd, &rcDest); 
    // Set the destination rectangle.
    SetRect(&rcDest, 0, 0, rcDest.right, rcDest.bottom); 
    
    // Set the video position.
    hr = g_pWc->SetVideoPosition(&rcSrc, &rcDest); 
}
```



Si vous souhaitez que vidéo occupe une plus petite partie de la zone cliente, modifiez le paramètre *rcDest* . Si vous souhaitez rogner l’image vidéo, modifiez le paramètre *rcSrc* .

## <a name="handle-window-messages"></a>Gérer les messages de fenêtre

Dans la mesure où VMR n’a pas sa propre fenêtre, il doit être notifié s’il doit redessiner ou redimensionner la vidéo. Répondez aux messages de fenêtre suivants en appelant les méthodes VMR listées.

**VMR-7**

1.  [**WM \_ PEINDRE**](../gdi/wm-paint.md). Appelez [**IVMRWindowlessControl :: RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo). Cette méthode fait en sorte que VMR-7 redessine la trame vidéo la plus récente.
2.  [**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md): appelez [**IVMRWindowlessControl ::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged). Cette méthode indique à VMR-7 que la vidéo doit être affichée à une nouvelle résolution ou profondeur de couleur.
3.  [**WM \_ SIZE**](../winmsg/wm-size.md) ou [**WM \_ WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): recalcule la position de la vidéo et appelle [**IVMRWindowlessControl :: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) pour mettre à jour la position, si nécessaire.

**VMR-9**

1.  [**WM \_ PEINDRE**](../gdi/wm-paint.md). Appelez [**IVMRWindowlessControl9 :: RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo). Cette méthode oblige VMR-9 à redessiner l’image vidéo la plus récente.
2.  [**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md): appelez [**IVMRWindowlessControl9 ::D isplaymodechanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged). Cette méthode indique à VMR-9 que la vidéo doit être affichée à une nouvelle résolution ou profondeur de couleur.
3.  [**WM \_ SIZE**](../winmsg/wm-size.md) ou [**WM \_ WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): recalcule la position de la vidéo et appelle [**IVMRWindowlessControl9 :: SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) pour mettre à jour la position, si nécessaire.

> [!Note]  
> Le gestionnaire par défaut pour le message [**WM \_ WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md) envoie un message de [**\_ taille WM**](../winmsg/wm-size.md) . Toutefois, si votre application intercepte **WM \_ WINDOWPOSCHANGED** et ne le transmet pas [**à DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), vous devez appeler **SetVideoPosition** dans votre gestionnaire **WM \_ WINDOWPOSCHANGED** , en plus de votre gestionnaire de **\_ taille WM** .

 

L’exemple suivant illustre un gestionnaire de messages de [**\_ peinture WM**](../gdi/wm-paint.md) . Il peint une région définie par le rectangle client moins le rectangle vidéo. Ne dessinez pas sur le rectangle vidéo, car VMR la dessinera, provoquant le scintillement. Pour la même raison, ne définissez pas de pinceau d’arrière-plan dans votre classe de fenêtre.


```C++
void OnPaint(HWND hwnd) 
{ 
    PAINTSTRUCT ps; 
    HDC         hdc; 
    RECT        rcClient; 
    GetClientRect(hwnd, &rcClient); 
    hdc = BeginPaint(hwnd, &ps); 
    if (g_pWc != NULL) 
    { 
        // Find the region where the application can paint by subtracting 
        // the video destination rectangle from the client area.
        // (Assume that g_rcDest was calculated previously.)
        HRGN rgnClient = CreateRectRgnIndirect(&rcClient); 
        HRGN rgnVideo  = CreateRectRgnIndirect(&g_rcDest);  
        CombineRgn(rgnClient, rgnClient, rgnVideo, RGN_DIFF);  
        
        // Paint on window.
        HBRUSH hbr = GetSysColorBrush(COLOR_BTNFACE); 
        FillRgn(hdc, rgnClient, hbr); 

        // Clean up.
        DeleteObject(hbr); 
        DeleteObject(rgnClient); 
        DeleteObject(rgnVideo); 

        // Request the VMR to paint the video.
        HRESULT hr = g_pWc->RepaintVideo(hwnd, hdc);  
    } 
    else  // There is no video, so paint the whole client area. 
    { 
        FillRect(hdc, &rc2, (HBRUSH)(COLOR_BTNFACE + 1)); 
    } 
    EndPaint(hwnd, &ps); 
} 
```



Bien que vous deviez répondre aux messages de [**\_ peinture WM**](../gdi/wm-paint.md) , vous n’avez rien à faire entre les messages de **\_ peinture WM** pour mettre à jour la vidéo. Comme le montre cet exemple, le mode sans fenêtre vous permet de traiter l’image vidéo simplement comme une zone de dessin automatique sur la fenêtre.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du convertisseur de mixage vidéo](using-the-video-mixing-renderer.md)
</dt> <dt>

[Rendu vidéo](video-rendering.md)
</dt> </dl>

 

 
