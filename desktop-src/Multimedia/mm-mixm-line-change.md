---
title: Message MM_MIXM_LINE_CHANGE (mmsystem. h)
description: Le \_ \_ message de modification de la ligne mm MIXM \_ est envoyé par un appareil de mixage pour avertir une application que l’état d’une ligne audio sur l’appareil spécifié a changé. L’application doit actualiser ses valeurs d’affichage et de mise en cache pour la ligne audio spécifiée.
ms.assetid: 68ada0be-9dc5-4edf-b924-ef0d10a1b79a
keywords:
- Message MM_MIXM_LINE_CHANGE Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIXM_LINE_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92c4aa10d9934f8cf5f5747ecb4e4eb736af2655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509731"
---
# <a name="mm_mixm_line_change-message"></a>Message de modification de la \_ ligne mm MIXM \_ \_

Le message de modification de la **\_ \_ ligne \_ mm MIXM** est envoyé par un appareil de mixage pour avertir une application que l’état d’une ligne audio sur l’appareil spécifié a changé. L’application doit actualiser ses valeurs d’affichage et de mise en cache pour la ligne audio spécifiée.


```C++
MM_MIXM_LINE_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwLineID 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*
</dt> <dd>

Handle vers le périphérique de mixage qui a envoyé le message de notification.

</dd> <dt>

<span id="dwLineID"></span><span id="dwlineid"></span><span id="DWLINEID"></span>*dwLineID*
</dt> <dd>

Identificateur de ligne pour la ligne audio dont l’État a changé. Cet identificateur est le même que le membre **dwLineID** de la structure **MIXERLINE** retournée par la fonction **mixerGetLineInfo**.

</dd> </dl>

## <a name="remarks"></a>Notes

Une application doit ouvrir un dispositif de mixage et spécifier une fenêtre de rappel pour recevoir le message de modification de la **\_ \_ ligne \_ mm MIXM** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>MMSYSTEM. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Mixages audio](audio-mixers.md)
</dt> <dt>

[Messages de mixage audio](audio-mixer-messages.md)
</dt> </dl>

 

 





