---
title: Message WM_CAP_SET_OVERLAY (VFW. h)
description: Le \_ message WM Cap \_ Set \_ Overlay active ou désactive le mode superposition. En mode superposition, la vidéo est affichée à l’aide de la superposition matérielle. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capOverlay.
ms.assetid: b74c0619-2b70-46e0-9acd-43d658529233
keywords:
- message WM_CAP_SET_OVERLAY Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_OVERLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f197ae3a7df9ad1520b84cf27fd15a1c76524ab1
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368023"
---
# <a name="wm_cap_set_overlay-message"></a>\_Message de \_ superposition du jeu de bouchon WM \_

Le message **WM \_ Cap \_ Set \_ Overlay** active ou désactive le mode superposition. En mode superposition, la vidéo est affichée à l’aide de la superposition matérielle. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) .


```C++
WM_CAP_SET_OVERLAY 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="f"></span><span id="F"></span>*FA*
</dt> <dd>

Indicateur de superposition. Spécifiez **true** pour ce paramètre pour activer le mode de superposition ou **false** pour le désactiver.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

L’utilisation d’une superposition ne requiert pas de ressources processeur.

Le membre **fHasOverlay** de la structure [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) indique si l’appareil est en capacité de se superposer. Le membre **fOverlayWindow** de la structure [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) indique si le mode superposition est actuellement activé.

L’activation du mode superposition désactive automatiquement le mode aperçu.

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

 

 





