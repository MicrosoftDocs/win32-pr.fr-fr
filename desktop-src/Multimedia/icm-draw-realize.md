---
title: Message ICM_DRAW_REALIZE (VFW. h)
description: Le \_ message d’établissement de dessin ICM \_ informe un pilote de rendu de réaliser sa palette de dessin pendant le dessin. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDrawRealize.
ms.assetid: 501540cd-41e2-4f80-abf8-2ec2179970a9
keywords:
- Message ICM_DRAW_REALIZE Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd054c16caae55cba25c30098337e54b0ec4b681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384487"
---
# <a name="icm_draw_realize-message"></a>\_Message d’établissement de dessin ICM \_

Le message d' **établissement de dessin ICM informe \_ \_** un pilote de rendu de réaliser sa palette de dessin pendant le dessin. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawRealize**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) .


```C++
ICM_DRAW_REALIZE 
wParam = (DWORD_PTR) (UINT_PTR) (HDC) hdc; 
lParam = (DWORD_PTR) (BOOL) fBackground; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="hdc"></span><span id="HDC"></span>*HDC*
</dt> <dd>

Handle vers le contrôleur de périphérique utilisé pour réaliser la palette.

</dd> <dt>

<span id="fBackground"></span><span id="fbackground"></span><span id="FBACKGROUND"></span>*fBackground*
</dt> <dd>

Indicateur d’arrière-plan. Spécifiez **true** pour réaliser la palette en tant que tâche en arrière-plan ou **false** pour réaliser la palette au premier plan.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK si la palette de dessin est réalisée ou ICERR \_ non prise en charge si la palette associée aux données décompressées est obtenue.

## <a name="remarks"></a>Notes

Les pilotes doivent répondre à ce message uniquement si la palette de dessin est différente de la palette décompressée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Gestionnaire de compression vidéo](video-compression-manager.md)
</dt> <dt>

[Messages de compression vidéo](video-compression-messages.md)
</dt> </dl>

 

 





