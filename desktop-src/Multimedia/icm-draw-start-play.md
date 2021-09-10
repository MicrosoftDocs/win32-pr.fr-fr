---
title: Message ICM_DRAW_START_PLAY (VFW. h)
description: le \_ message ICM DRAW \_ START \_ PLAY fournit les heures de début et de fin d’une opération de lecture à un pilote de rendu. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDrawStartPlay.
ms.assetid: 27c4c06e-6510-43dc-a754-fe44144796f5
keywords:
- message ICM_DRAW_START_PLAY Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364204"
---
# <a name="icm_draw_start_play-message"></a>ICM \_ DESSINER le \_ message de début de \_ lecture

le message **ICM \_ DRAW \_ START \_ PLAY** fournit les heures de début et de fin d’une opération de lecture à un pilote de rendu. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawStartPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstartplay) .


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

## <a name="remarks"></a>Remarques

Ce message précède toutes les données de frame envoyées au pilote de rendu.

les unités pour *lFrom* et *lTo* sont spécifiées avec le message [**ICM \_ DRAW \_ BEGIN**](icm-draw-begin.md) . Pour les données vidéo, il s’agit généralement d’un nombre de trames. Pour plus d’informations sur la vitesse de lecture, consultez les membres **dwRate** et **dwScale** de la structure [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) .

Si l’heure de fin est inférieure à l’heure de début, la direction de la lecture est inversée.

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

 

 





