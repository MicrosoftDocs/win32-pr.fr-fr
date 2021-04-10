---
title: Message ICM_DRAW_START_PLAY (VFW. h)
description: Le \_ \_ \_ message de début de dessin ICM fournit les heures de début et de fin d’une opération de lecture à un pilote de rendu. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDrawStartPlay.
ms.assetid: 27c4c06e-6510-43dc-a754-fe44144796f5
keywords:
- Message ICM_DRAW_START_PLAY Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_START_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefea0f6344fb598fac1f0413bba5c377c5914e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103449"
---
# <a name="icm_draw_start_play-message"></a>Message de début de la \_ \_ \_ lecture ICM

Le message de **début de dessin ICM fournit les \_ \_ \_** heures de début et de fin d’une opération de lecture à un pilote de rendu. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawStartPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstartplay) .


```C++
ICM_DRAW_START_PLAY 
wParam = (DWORD_PTR) lFrom; 
lParam = (DWORD_PTR) lTo; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lFrom"></span><span id="lfrom"></span><span id="LFROM"></span>*lFrom*
</dt> <dd>

Heure de début

</dd> <dt>

<span id="lTo"></span><span id="lto"></span><span id="LTO"></span>*Supports*
</dt> <dd>

Heure de fin.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Ce message précède toutes les données de frame envoyées au pilote de rendu.

Les unités pour *lFrom* et *lTo* sont spécifiées avec le message [**ICM \_ Draw \_ Begin**](icm-draw-begin.md) . Pour les données vidéo, il s’agit généralement d’un nombre de trames. Pour plus d’informations sur la vitesse de lecture, consultez les membres **dwRate** et **dwScale** de la structure [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) .

Si l’heure de fin est inférieure à l’heure de début, la direction de la lecture est inversée.

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

 

 





