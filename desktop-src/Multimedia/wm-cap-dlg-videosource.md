---
title: Message WM_CAP_DLG_VIDEOSOURCE (VFW. h)
description: Le \_ message WM Cap \_ DLG \_ VIDEOSOURCE affiche une boîte de dialogue dans laquelle l’utilisateur peut contrôler la source vidéo.
ms.assetid: 8dc2f271-1f48-4e63-badf-9f3322063018
keywords:
- message WM_CAP_DLG_VIDEOSOURCE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOSOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e8ae7e3d619964a547fbe0db4517fd1e7d277f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413858"
---
# <a name="wm_cap_dlg_videosource-message"></a>\_Message WM Cap \_ DLG \_ VIDEOSOURCE

Le message **WM \_ Cap \_ DLG \_ VIDEOSOURCE** affiche une boîte de dialogue dans laquelle l’utilisateur peut contrôler la source vidéo. La boîte de dialogue source vidéo peut contenir des contrôles qui sélectionnent des sources d’entrée. Modifiez la teinte, le contraste et la luminosité de l’image. et modifiez la qualité vidéo avant de numériser les images dans la mémoire tampon de trame. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) .


```C++
WM_CAP_DLG_VIDEOSOURCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

La boîte de dialogue source vidéo est unique pour chaque pilote de capture. Certains pilotes de capture peuvent ne pas prendre en charge une boîte de dialogue source vidéo. Les applications peuvent déterminer si le pilote de capture prend en charge ce message en vérifiant le membre **fHasDlgVideoSource** de la structure [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Capture vidéo](video-capture.md)
</dt> <dt>

[Messages de capture vidéo](video-capture-messages.md)
</dt> </dl>

 

 





