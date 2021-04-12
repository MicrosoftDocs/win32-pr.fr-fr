---
description: Cette rubrique est l’étape 5 de la lecture audio/vidéo du didacticiel dans DirectShow.
ms.assetid: 9d7a40e0-4327-4ca3-b430-2be02f80c16f
title: 'Étape 5 : ajouter la fonctionnalité vidéo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f5ccf1ae3ca24a705506bc41620ac53a13d7e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209730"
---
# <a name="step-5-add-video-functionality"></a><span data-ttu-id="9c833-103">Étape 5 : ajouter la fonctionnalité vidéo</span><span class="sxs-lookup"><span data-stu-id="9c833-103">Step 5: Add Video Functionality</span></span>

<span data-ttu-id="9c833-104">Cette rubrique est l’étape 5 de la [lecture audio/vidéo du didacticiel dans DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="9c833-104">This topic is step 5 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="9c833-105">Le code complet est présenté dans la rubrique [exemple de lecture DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="9c833-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="9c833-106">Pour vous assurer que la vidéo s’affiche correctement, l’application doit répondre aux messages WM [**\_ Paint**](../gdi/wm-paint.md), [**WM \_ Size**](../winmsg/wm-size.md)et [**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md) comme suit.</span><span class="sxs-lookup"><span data-stu-id="9c833-106">To ensure that video displays correctly, the application must respond to [**WM\_PAINT**](../gdi/wm-paint.md), [**WM\_SIZE**](../winmsg/wm-size.md), and [**WM\_DISPLAYCHANGE**](../gdi/wm-displaychange.md) messages as follows.</span></span>

### <a name="handle-wm_paint-messages"></a><span data-ttu-id="9c833-107">Gérer \_ les messages de peinture WM</span><span class="sxs-lookup"><span data-stu-id="9c833-107">Handle WM\_PAINT Messages</span></span>

<span data-ttu-id="9c833-108">Lorsque l’application reçoit un message de [**\_ peinture WM**](../gdi/wm-paint.md) , le convertisseur vidéo peut avoir besoin de redessiner la dernière image vidéo.</span><span class="sxs-lookup"><span data-stu-id="9c833-108">When the application receives a [**WM\_PAINT**](../gdi/wm-paint.md) message, the video renderer might need to redraw the last video frame.</span></span> <span data-ttu-id="9c833-109">Pour le filtre EVR ( [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) ), appelez [**IMFVideoDisplayControl :: RepaintVideo**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="9c833-109">For the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter, call [**IMFVideoDisplayControl::RepaintVideo**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span></span>


```C++
HRESULT CEVR::Repaint(HWND hwnd, HDC hdc)
{
    if (m_pVideoDisplay)
    {
        return m_pVideoDisplay->RepaintVideo();
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="9c833-110">Pour le [filtre de convertisseur de mixage vidéo 9](video-mixing-renderer-filter-9.md) (VMR-9), appelez [**IVMRWindowlessControl9 :: RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="9c833-110">For the [Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9), call [**IVMRWindowlessControl9::RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).</span></span>


```C++
HRESULT CVMR9::Repaint(HWND hwnd, HDC hdc)
{
    if (m_pWindowless)
    {
        return m_pWindowless->RepaintVideo(hwnd, hdc);
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="9c833-111">Pour le [filtre de convertisseur de mixage vidéo 7](video-mixing-renderer-filter-7.md) (VMR-7), appelez [**IVMRWindowlessControl :: RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="9c833-111">For the [Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7), call [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).</span></span>


```C++
HRESULT CVMR7::Repaint(HWND hwnd, HDC hdc)
{
    if (m_pWindowless)
    {
        return m_pWindowless->RepaintVideo(hwnd, hdc);
    }
    else
    {
        return S_OK;
    }
}
```



### <a name="handle-wm_size-messages"></a><span data-ttu-id="9c833-112">Gérer \_ les messages de taille WM</span><span class="sxs-lookup"><span data-stu-id="9c833-112">Handle WM\_SIZE Messages</span></span>

<span data-ttu-id="9c833-113">Si la taille de la fenêtre vidéo change, avertissez le convertisseur vidéo pour redimensionner la vidéo.</span><span class="sxs-lookup"><span data-stu-id="9c833-113">If the size of the video window changes, notify the video renderer to resize the video.</span></span> <span data-ttu-id="9c833-114">Pour EVR, appelez [**IMFVideoDisplayControl :: SetVideoPosition**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="9c833-114">For the EVR, call [**IMFVideoDisplayControl::SetVideoPosition**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>


```C++
HRESULT CEVR::UpdateVideoWindow(HWND hwnd, const LPRECT prc)
{
    if (m_pVideoDisplay == NULL)
    {
        return S_OK; // no-op
    }

    if (prc)
    {
        return m_pVideoDisplay->SetVideoPosition(NULL, prc);
    }
    else
    {

        RECT rc;
        GetClientRect(hwnd, &rc);
        return m_pVideoDisplay->SetVideoPosition(NULL, &rc);
    }
}
```



<span data-ttu-id="9c833-115">Pour VMR-9, appelez [**IVMRWindowlessControl9 :: SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="9c833-115">For the VMR-9, call [**IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition).</span></span>


```C++
HRESULT CVMR9::UpdateVideoWindow(HWND hwnd, const LPRECT prc)
{
    if (m_pWindowless == NULL)
    {
        return S_OK; // no-op
    }

    if (prc)
    {
        return m_pWindowless->SetVideoPosition(NULL, prc);
    }
    else
    {

        RECT rc;
        GetClientRect(hwnd, &rc);
        return m_pWindowless->SetVideoPosition(NULL, &rc);
    }
}
```



<span data-ttu-id="9c833-116">Pour VMR-7, appelez [**IVMRWindowlessControl :: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="9c833-116">For the VMR-7, call [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition).</span></span>


```C++
HRESULT CVMR7::UpdateVideoWindow(HWND hwnd, const LPRECT prc)
{
    if (m_pWindowless == NULL)
    {
        return S_OK; // no-op
    }

    if (prc)
    {
        return m_pWindowless->SetVideoPosition(NULL, prc);
    }
    else
    {
        RECT rc;
        GetClientRect(hwnd, &rc);
        return m_pWindowless->SetVideoPosition(NULL, &rc);
    }
}
```



### <a name="handle-wm_displaychange-messages"></a><span data-ttu-id="9c833-117">Gérer \_ les messages WM DISPLAYCHANGE</span><span class="sxs-lookup"><span data-stu-id="9c833-117">Handle WM\_DISPLAYCHANGE Messages</span></span>

<span data-ttu-id="9c833-118">Si le mode d’affichage change, vous devez notifier le filtre VMR-9 ou VMR-7.</span><span class="sxs-lookup"><span data-stu-id="9c833-118">If the display mode changes, you must notify the VMR-9 or VMR-7 filter.</span></span> <span data-ttu-id="9c833-119">Pour VMR-9, appelez [**IVMRWindowlessControl9 ::D isplaymodechanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="9c833-119">For the VMR-9, call [**IVMRWindowlessControl9::DisplayModeChanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).</span></span>


```C++
HRESULT CVMR9::DisplayModeChanged()
{
    if (m_pWindowless)
    {
        return m_pWindowless->DisplayModeChanged();
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="9c833-120">Pour VMR-7, appelez [**IVMRWindowlessControl ::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="9c833-120">For the VMR-7, call [**IVMRWindowlessControl::DisplayModeChanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span></span>


```C++
HRESULT CVMR7::DisplayModeChanged()
{
    if (m_pWindowless)
    {
        return m_pWindowless->DisplayModeChanged();
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="9c833-121">Le EVR n’a pas besoin d’être notifié lorsque le mode d’affichage change.</span><span class="sxs-lookup"><span data-stu-id="9c833-121">The EVR does not need to be notified when the display mode changes.</span></span>

<span data-ttu-id="9c833-122">[Étape 6 : gérer les événements graphiques](step-6--handle-graph-events.md).</span><span class="sxs-lookup"><span data-stu-id="9c833-122">Next: [Step 6: Handle Graph Events](step-6--handle-graph-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c833-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9c833-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c833-124">Lecture audio/vidéo dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="9c833-124">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="9c833-125">Exemple de lecture DirectShow</span><span class="sxs-lookup"><span data-stu-id="9c833-125">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="9c833-126">Utilisation du filtre DirectShow EVR</span><span class="sxs-lookup"><span data-stu-id="9c833-126">Using the DirectShow EVR Filter</span></span>](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[<span data-ttu-id="9c833-127">Utilisation du convertisseur de mixage vidéo</span><span class="sxs-lookup"><span data-stu-id="9c833-127">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
