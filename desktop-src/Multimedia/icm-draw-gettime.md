---
title: Message ICM_DRAW_GETTIME (VFW. h)
description: Le \_ message ICM Draw \_ GETTIME demande un pilote de rendu qui contrôle le minutage des frames de dessin pour retourner la valeur actuelle de son horloge interne. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDrawGetTime.
ms.assetid: 77f0a322-c0bc-4cfe-a3d0-7633cf8d682a
keywords:
- Message ICM_DRAW_GETTIME Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_GETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f756a76408d01cb72ee1762f14bb8a5eab19e475
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511571"
---
# <a name="icm_draw_gettime-message"></a>\_Message de \_ cogettime de dessin ICM

Le message **ICM \_ Draw \_ GETTIME** demande un pilote de rendu qui contrôle le minutage des frames de dessin pour retourner la valeur actuelle de son horloge interne. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawGetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) .


```C++
ICM_DRAW_GETTIME 
wParam = (DWORD_PTR) (LPVOID) lplTime; 
lParam = 0; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lplTime"></span><span id="lpltime"></span><span id="LPLTIME"></span>*lplTime*
</dt> <dd>

Adresse qui doit contenir l’heure actuelle. La valeur de retour doit être spécifiée dans des exemples.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.

## <a name="remarks"></a>Notes

Ce message est généralement pris en charge par le matériel qui effectue sa propre décompression, son minutage et son dessin asynchrones. Le message peut également être envoyé si le matériel est utilisé en tant que maître de synchronisation.

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

 

 





