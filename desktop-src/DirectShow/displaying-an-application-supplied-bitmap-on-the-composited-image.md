---
title: Afficher un bitmap fourni par une application sur l’image composite
description: Affichage d’un bitmap Application-Supplied sur l’image composite
ms.assetid: c51329d3-e814-4ef9-aad8-a3e60f9fa2a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ecd8ac931d0a0bb83eafba09d8ca7dc8263f0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520575"
---
# <a name="display-an-app-supplied-bitmap-on-the-composited-image"></a>Afficher un bitmap fourni par une application sur l’image composite

Les applications peuvent utiliser le mode de mixage de VMR pour afficher des logos de canal à contrôle alpha, une interface utilisateur ou des publications, partiellement ou complètement dans le rectangle vidéo. Étant donné que la fusion est effectuée sur le matériel par le processeur graphique, l’impact est minime sur les performances de lecture du flux vidéo et il n’y a pas d’artefacts de scintillement ou de destruction détectables. Les applications peuvent modifier l’image affichée aussi souvent qu’elles le souhaitent. Notez que les modifications sont reflétées uniquement à l’écran lorsque le graphique de filtre DirectShow est à l’État en cours d’exécution.

VMR utilise son composant mixer pour superposer l’image bitmap sur l’image composite. Avec VMR-7, l’application doit forcer VMR à charger son mélangeur, même s’il n’y a qu’un seul flux vidéo. Cela n’est pas nécessaire avec VMR-9 puisqu’il charge son mélangeur par défaut.

Pour fusionner une image bitmap statique avec le flux vidéo, l’application crée le VMR et l’ajoute au graphique, puis appelle [**IVMRFilterConfig :: SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams). La valeur transmise à cette fonction identifie le nombre de broches d’entrée que VMR doit créer. Les applications peuvent spécifier n’importe quelle valeur comprise entre 1 et MAX \_ \_ , les flux de mixage ; la valeur 1 est valide si l’application ne souhaite afficher qu’un seul flux vidéo. Même si VMR-7 a une seule broche d’entrée par défaut, cette méthode doit être appelée pour forcer le chargement de son composant mixer. (Le VMR-9 charge son mélangeur et configure quatre codes PIN par défaut.)

Pour définir l’image bitmap, utilisez l’interface [**IVMRMixerBitmap**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap) sur l’interface VMR-7 ou [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) sur VMR-9.

La bitmap peut être spécifiée par un handle vers un contexte de périphérique GDI (hDC) ou par une interface de surface DirectDraw. Si l’application souhaite que l’image contienne des informations alpha incorporées (également appelées par pixel alpha), elle doit placer les données d’image dans une interface de surface DirectDraw. Cela est dû au fait qu’il n’est pas possible actuellement de placer des informations alpha par pixel avec un contexte de périphérique GDI. La surface DirectDraw doit être RGB32 ou ARGB32 et doit être de préférence une surface de mémoire système. Il n’est pas nécessaire que les dimensions de surface soient une puissance de 2.

VMR permet aux applications de spécifier l’emplacement et une valeur de transparence globale pour l’image. Le code suivant montre comment passer des données d’image à VMR pour la fusion suivante :


```C++
HRESULT BlendApplicationImage( 
  HWND hwndApp,
  IVMRWindowlessControl* pWc,
  HBITMAP hbm
)
{
    LONG cx, cy;
    HRESULT hr;
    hr = pWc->GetNativeVideoSize(&cx, &cy, NULL, NULL);
    if (FAILED(hr))
        return hr;
    
    HDC hdc = GetDC(hwndApp);
    if (hdc == NULL)
    {
        return E_FAIL;
    }
    
    HDC hdcBmp = CreateCompatibleDC(hdc);
    ReleaseDC(hwndApp, hdc);
    
    if (hdcBmp == NULL)
    {
        return E_FAIL;
    }
    
    BITMAP bm;
    if (0 == GetObject(hbm, sizeof(bm), &bm))
    {
        DeleteDC(hdcBmp);
        return E_FAIL;
    }
    
    HBITMAP hbmOld = (HBITMAP)SelectObject(hdcBmp, hbm);
    if (hbmOld == 0)
    {
        DeleteDC(hdcBmp);
        return E_FAIL;
    }
    
    VMRALPHABITMAP bmpInfo;
    ZeroMemory(&bmpInfo, sizeof(bmpInfo) );
    bmpInfo.dwFlags = VMRBITMAP_HDC;
    bmpInfo.hdc = hdcBmp;
    
    // Show the entire bitmap in the top-left corner of the video image.
    SetRect(&bmpInfo.rSrc, 0, 0, bm.bmWidth, bm.bmHeight);
    bmpInfo.rDest.left = 0.f;
    bmpInfo.rDest.top = 0.f;
    bmpInfo.rDest.right = (float)bm.bmWidth / (float)cx;
    bmpInfo.rDest.bottom = (float)bm.bmHeight / (float)cy;
    
    // Set the transparency value (1.0 is opaque, 0.0 is transparent).
    bmpInfo.fAlpha = 0.2f;
    
    IVMRMixerBitmap* pBmp;
    hr = pWc->QueryInterface(IID_IVMRMixerBitmap, (LPVOID *)&pBmp);
    if (SUCCEEDED(hr)) 
    {
        pBmp->SetAlphaBitmap(&bmpInfo);
        pBmp->Release();
    }
    
    DeleteObject(SelectObject(hdcBmp, hbmOld));
    DeleteDC(hdcBmp);
    return hr;
}
```



Les concepts abordés dans cette rubrique sont illustrés dans l’exemple d’application [VMRPlayer](vmrplayer-sample.md) .

**Création d’animations simples avec l’image bitmap**

Pour créer un logo simple animé simple, placez tous les « frames » bitmap dans une seule image, comme indiqué dans l’illustration suivante.

![bande d’images VMR](images/vmr-image-strip.png)

Lorsque vous définissez initialement la bitmap à l’aide de [**IVMRMixerBitmap :: SetAlphaBitmap**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap), si la bitmap se trouve dans un HDC, définissez le champ **rSrc** de la structure **VMRALPHABITMAP** pour spécifier la taille de l’image bitmap entière au sein du HDC. Les membres **supérieur** et **gauche** de la structure ont la valeur 0, et les membres de **droite** et **inférieurs** sont la largeur et la hauteur de la bitmap. Si la bitmap se trouve dans une surface DirectDraw, la taille de la surface est connue. il n’est donc pas nécessaire de spécifier rSrc dans cette méthode.

Quand vous appelez [**IVMRMixerBitmap :: UpdateAlphaBitmapParameters**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-updatealphabitmapparameters), utilisez le membre **rSrc** pour les bitmaps HDC et DirectDraw, pour spécifier le cadre ou le rectangle particulier dans l’image que vous souhaitez afficher, et définir l’indicateur **VMRBITMAP \_ SRCRECT** dans le membre **dwFlags** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du mode de mixage VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



