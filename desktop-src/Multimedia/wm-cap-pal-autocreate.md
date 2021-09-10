---
title: Message WM_CAP_PAL_AUTOCREATE (VFW. h)
description: Le \_ message de \_ création automatique WM Cap PAL \_ demande que le pilote de capture échantillonne les images vidéo et crée automatiquement une nouvelle palette. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capPaletteAuto.
ms.assetid: b94d245d-adf4-4fe0-b053-87109ef5fd2f
keywords:
- message WM_CAP_PAL_AUTOCREATE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_AUTOCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ba70de46167121aa9a83959c6d9e202039f65cd
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124367956"
---
# <a name="wm_cap_pal_autocreate-message"></a>Message de création d’un \_ \_ message d’attente PAL PAC \_

Le message de **création automatique WM \_ Cap \_ PAL \_** demande que le pilote de capture échantillonne les images vidéo et crée automatiquement une nouvelle palette. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) .


```C++
WM_CAP_PAL_AUTOCREATE 
wParam = (WPARAM) (iFrames); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*
</dt> <dd>

Nombre d’images à échantillonner.

</dd> <dt>

<span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*
</dt> <dd>

Nombre de couleurs dans la palette. La valeur maximale de ce paramètre est 256.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

Si une erreur se produit et qu’une fonction de rappel d’erreur est définie à l’aide du message d' [**\_ erreur WM Cap \_ Set \_ callback \_**](wm-cap-set-callback-error.md) , la fonction de rappel d’erreur est appelée.

## <a name="remarks"></a>Remarques

La séquence vidéo échantillonnée doit inclure toutes les couleurs souhaitées dans la palette. Pour obtenir la meilleure palette, vous devrez peut-être échantillonner l’intégralité de la séquence plutôt qu’une partie de celle-ci.

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

 

 





