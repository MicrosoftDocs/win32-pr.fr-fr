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
# <a name="step-5-add-video-functionality"></a>Étape 5 : ajouter la fonctionnalité vidéo

Cette rubrique est l’étape 5 de la [lecture audio/vidéo du didacticiel dans DirectShow](audio-video-playback-in-directshow.md). Le code complet est présenté dans la rubrique [exemple de lecture DirectShow](directshow-playback-example.md).

Pour vous assurer que la vidéo s’affiche correctement, l’application doit répondre aux messages WM [**\_ Paint**](../gdi/wm-paint.md), [**WM \_ Size**](../winmsg/wm-size.md)et [**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md) comme suit.

### <a name="handle-wm_paint-messages"></a>Gérer \_ les messages de peinture WM

Lorsque l’application reçoit un message de [**\_ peinture WM**](../gdi/wm-paint.md) , le convertisseur vidéo peut avoir besoin de redessiner la dernière image vidéo. Pour le filtre EVR ( [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) ), appelez [**IMFVideoDisplayControl :: RepaintVideo**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).


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



Pour le [filtre de convertisseur de mixage vidéo 9](video-mixing-renderer-filter-9.md) (VMR-9), appelez [**IVMRWindowlessControl9 :: RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).


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



Pour le [filtre de convertisseur de mixage vidéo 7](video-mixing-renderer-filter-7.md) (VMR-7), appelez [**IVMRWindowlessControl :: RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).


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



### <a name="handle-wm_size-messages"></a>Gérer \_ les messages de taille WM

Si la taille de la fenêtre vidéo change, avertissez le convertisseur vidéo pour redimensionner la vidéo. Pour EVR, appelez [**IMFVideoDisplayControl :: SetVideoPosition**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).


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



Pour VMR-9, appelez [**IVMRWindowlessControl9 :: SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition).


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



Pour VMR-7, appelez [**IVMRWindowlessControl :: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition).


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



### <a name="handle-wm_displaychange-messages"></a>Gérer \_ les messages WM DISPLAYCHANGE

Si le mode d’affichage change, vous devez notifier le filtre VMR-9 ou VMR-7. Pour VMR-9, appelez [**IVMRWindowlessControl9 ::D isplaymodechanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).


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



Pour VMR-7, appelez [**IVMRWindowlessControl ::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).


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



Le EVR n’a pas besoin d’être notifié lorsque le mode d’affichage change.

[Étape 6 : gérer les événements graphiques](step-6--handle-graph-events.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lecture audio/vidéo dans DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[Exemple de lecture DirectShow](directshow-playback-example.md)
</dt> <dt>

[Utilisation du filtre DirectShow EVR](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[Utilisation du convertisseur de mixage vidéo](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
