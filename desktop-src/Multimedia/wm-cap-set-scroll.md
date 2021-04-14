---
title: Message WM_CAP_SET_SCROLL (VFW. h)
description: Le \_ \_ \_ message de défilement WM Cap Set définit la partie de la trame vidéo à afficher dans la fenêtre de capture.
ms.assetid: 545605e4-6b1f-403a-a3ab-0fd6750ae776
keywords:
- Message WM_CAP_SET_SCROLL Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCROLL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812b76bdcad166b9f766957032f232293d4083c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466866"
---
# <a name="wm_cap_set_scroll-message"></a>Message de défilement de l' \_ ensemble de connexions WM \_ \_

Le message de **\_ \_ \_ défilement WM Cap Set** définit la partie de la trame vidéo à afficher dans la fenêtre de capture. Ce message définit l’angle supérieur gauche de la zone cliente de la fenêtre de capture sur les coordonnées d’un pixel spécifié dans le cadre de la vidéo. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) .


```C++
WM_CAP_SET_SCROLL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPPOINT) (lpP); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpP"></span><span id="lpp"></span><span id="LPP"></span>*lpP*
</dt> <dd>

Adresse qui doit contenir la position de défilement souhaitée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

La position de défilement affecte l’image dans les modes d’aperçu et de superposition.

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

 

 





