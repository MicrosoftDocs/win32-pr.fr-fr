---
title: Message WM_CAP_SET_PREVIEW (VFW. h)
description: Le \_ message WM Cap \_ Set \_ preview active ou désactive le mode aperçu.
ms.assetid: ef6218d6-4fff-469f-b2e0-d7990998a3e5
keywords:
- Message WM_CAP_SET_PREVIEW Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_PREVIEW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4a7e490809efa2e2d9f1ad27bca697c6333e682
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106114"
---
# <a name="wm_cap_set_preview-message"></a>Message d’aperçu de l' \_ ensemble de connexions WM \_ \_

Le message **WM \_ Cap \_ Set \_ preview** active ou désactive le mode aperçu. En mode aperçu, les frames sont transférés du matériel de capture à la mémoire système, puis affichés dans la fenêtre de capture à l’aide des fonctions GDI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) .


```C++
WM_CAP_SET_PREVIEW 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="f"></span><span id="F"></span>*FA*
</dt> <dd>

Indicateur d’aperçu. Spécifiez **true** pour ce paramètre pour activer le mode aperçu ou **false** pour le désactiver.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Le mode aperçu utilise des ressources processeur importantes. Les applications peuvent désactiver l’aperçu ou réduire le taux d’aperçu lorsqu’une autre application a le focus. Le membre **fLiveWindow** de la structure [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) indique si le mode aperçu est actuellement activé.

L’activation du mode aperçu désactive automatiquement le mode superposition.

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

 

 





