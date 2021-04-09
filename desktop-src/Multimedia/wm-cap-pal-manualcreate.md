---
title: Message WM_CAP_PAL_MANUALCREATE (VFW. h)
description: Le \_ message WM Cap \_ PAL \_ MANUALCREATE demande que le pilote de capture échantillonne manuellement les images vidéo et crée une nouvelle palette. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capPaletteManual.
ms.assetid: 96b6b2d6-084a-411e-8495-ea27e0c4f04f
keywords:
- Message WM_CAP_PAL_MANUALCREATE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_MANUALCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dfd5b6588381ede0faaae539d3d8418b041f458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740957"
---
# <a name="wm_cap_pal_manualcreate-message"></a>\_Message WM Cap \_ PAL \_ MANUALCREATE

Le message **WM \_ Cap \_ PAL \_ MANUALCREATE** demande que le pilote de capture échantillonne manuellement les images vidéo et crée une nouvelle palette. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capPaletteManual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) .


```C++
WM_CAP_PAL_MANUALCREATE 
wParam = (WPARAM) (fGrab); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="fGrab"></span><span id="fgrab"></span><span id="FGRAB"></span>*fGrab*
</dt> <dd>

Indicateur d’histogramme de la palette. Définissez ce paramètre sur **true** pour chaque frame inclus dans la création de la palette optimale. Après avoir collecté la dernière trame, définissez ce paramètre sur **false** pour calculer la palette optimale et l’envoyer au pilote de capture.

</dd> <dt>

<span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*
</dt> <dd>

Nombre de couleurs dans la palette. La valeur maximale de ce paramètre est 256. Cette valeur est utilisée uniquement pendant la collecte de la première image d’une séquence.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

Si une erreur se produit et qu’une fonction de rappel d’erreur est définie à l’aide du message d' [**\_ erreur WM Cap \_ Set \_ callback \_**](wm-cap-set-callback-error.md) , la fonction de rappel d’erreur est appelée.

## <a name="requirements"></a>Configuration requise



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

 

 





