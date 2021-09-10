---
title: Message ICM_DRAW_GETTIME (VFW. h)
description: le ICM \_ dessiner le \_ message GETTIME demande un pilote de rendu qui contrôle le minutage des frames de dessin pour retourner la valeur actuelle de son horloge interne. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDrawGetTime.
ms.assetid: 77f0a322-c0bc-4cfe-a3d0-7633cf8d682a
keywords:
- message ICM_DRAW_GETTIME Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364191"
---
# <a name="icm_draw_gettime-message"></a>ICM \_ DESSINER le \_ message GETTIME

le **ICM \_ dessiner \_** le message GETTIME demande un pilote de rendu qui contrôle le minutage des frames de dessin pour retourner la valeur actuelle de son horloge interne. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawGetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) .


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

## <a name="remarks"></a>Remarques

Ce message est généralement pris en charge par le matériel qui effectue sa propre décompression, son minutage et son dessin asynchrones. Le message peut également être envoyé si le matériel est utilisé en tant que maître de synchronisation.

## <a name="requirements"></a>Spécifications



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

 

 





