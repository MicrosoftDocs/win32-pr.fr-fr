---
title: Message WM_CAP_PAL_PASTE (VFW. h)
description: Le \_ message WM Cap \_ PAL \_ Paste copie la palette à partir du presse-papiers et la transmet à un pilote de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capPalettePaste.
ms.assetid: d49c7fd9-be40-4a07-8339-b85f7c4c331e
keywords:
- message WM_CAP_PAL_PASTE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_PASTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3daf88c69edbb8bad6257456b95a86c8a68df328
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124367975"
---
# <a name="wm_cap_pal_paste-message"></a>\_Coller le message WM capuchon \_ PAL \_

Le message **WM \_ Cap \_ PAL \_ Paste** copie la palette à partir du presse-papiers et la transmet à un pilote de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capPalettePaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) .


```C++
WM_CAP_PAL_PASTE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

Si une erreur se produit et qu’une fonction de rappel d’erreur est définie à l’aide du message d' [**\_ erreur WM Cap \_ Set \_ callback \_**](wm-cap-set-callback-error.md) , la fonction de rappel d’erreur est appelée.

## <a name="remarks"></a>Remarques

Un pilote de capture utilise une palette lorsqu’il est requis par le format vidéo numérisé spécifié.

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

 

 





