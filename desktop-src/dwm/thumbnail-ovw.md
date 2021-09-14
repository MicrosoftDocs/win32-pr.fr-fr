---
title: Vue d’ensemble des miniatures DWM
description: Gestionnaire de fenêtrage (DWM) permet d’afficher les représentations miniatures des fenêtres d’application.
ms.assetid: 6d71fcda-0cf0-463c-8c60-0415109d154f
keywords:
- Gestionnaire de fenêtrage (DWM), miniatures
- DWM (Gestionnaire de fenêtrage), miniatures
- Gestionnaire de fenêtrage (DWM), relations de miniatures
- DWM (Gestionnaire de fenêtrage), relations de miniatures
- miniatures
- relations de miniatures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3e0f1e6875e447a18ff5e63d703460ff909b25
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012660"
---
# <a name="dwm-thumbnail-overview"></a>Vue d’ensemble des miniatures DWM

Gestionnaire de fenêtrage (DWM) permet d’afficher les représentations miniatures des fenêtres d’application. Il ne s’agit pas d’instantanés statiques d’une fenêtre, mais qui sont plutôt dynamiques, des connexions constantes entre une fenêtre source de miniatures et un emplacement sur une fenêtre de destination qui reçoit le rendu de miniatures dynamiques. Cela permet d’obtenir un aperçu rapide des applications en cours d’exécution en pointant sur l’application dans la barre des tâches ou en utilisant le mouvement de touche ALT-TAB pour voir et basculer rapidement vers une application.

l’illustration suivante montre la miniature de Windows Vista en direct qui s’affiche lorsque vous pointez sur l’application dans la barre des tâches.

![Capture d’écran montrant la miniature D W M affichée lorsque vous pointez sur une application dans la barre des tâches.](images/dwm-livethumbnail.png)

l’image suivante illustre le retournement Windows Vista (onglet ALT) activé par DWM.

![capture d’écran de l’onglet Alt activé pour DWM](images/dwm-flip.png)

> [!Note]  
> les miniatures DWM n’autorisent pas les développeurs à créer des applications telles que la fonctionnalité Windows Vista Flip3D (onglet touche de fonction). Les miniatures sont rendues directement dans la fenêtre de destination en 2D.

 

## <a name="dwm-thumbnail-relationships"></a>Relations des miniatures DWM

Pour afficher des miniatures dans votre application, vous devez d’abord établir une relation entre une fenêtre source et une fenêtre de destination. Pour ce faire, appelez la fonction [**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) .

[**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) n’affiche pas de miniature sur la fenêtre de destination, mais crée simplement la relation et fournit la poignée de miniature. La miniature est rendue une fois que les [**\_ \_ Propriétés de miniature DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) ont été définies et que la fonction [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) a été appelée. Les appels suivants à **DwmUpdateThumbnailProperties** mettent à jour la miniature avec un nouvel ensemble de propriétés. Le DWM fournit également la fonction d’assistance [**DwmQueryThumbnailSourceSize**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize) pour obtenir la taille de la fenêtre source à partir de la miniature.

Pour mettre fin à une relation de miniatures, appelez la fonction [**DwmUnregisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail) .

l’exemple suivant montre comment créer un releationship avec le Windows desktop et l’afficher dans une application.


```
HRESULT hr = S_OK;
HTHUMBNAIL thumbnail = NULL;

// Register the thumbnail
hr = DwmRegisterThumbnail(hwnd, FindWindow(_T("Progman"), NULL), &thumbnail);
if (SUCCEEDED(hr))
{
    // Specify the destination rectangle size
    RECT dest = {0,50,100,150};

    // Set the thumbnail properties for use
    DWM_THUMBNAIL_PROPERTIES dskThumbProps;
    dskThumbProps.dwFlags = DWM_TNP_SOURCECLIENTAREAONLY | DWM_TNP_VISIBLE | DWM_TNP_OPACITY | DWM_TNP_RECTDESTINATION;
    dskThumbProps.fSourceClientAreaOnly = FALSE; 
    dskThumbProps.fVisible = TRUE;
    dskThumbProps.opacity = (255 * 70)/100;
    dskThumbProps.rcDestination = dest;

    // Display the thumbnail
    hr = DwmUpdateThumbnailProperties(thumbnail,&dskThumbProps);
    if (SUCCEEDED(hr))
    {
        // ...
    }
}
return hr;
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble du Gestionnaire de fenêtres du Bureau](dwm-overview.md)
</dt> <dt>

[Activer et contrôler la composition du Gestionnaire de fenêtrage](composition-ovw.md)
</dt> <dt>

[Considérations sur les performances et meilleures pratiques](bestpractices-ovw.md)
</dt> </dl>

 

 




