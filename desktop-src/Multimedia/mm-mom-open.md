---
title: Message MM_MOM_OPEN (mmsystem. h)
description: Le \_ \_ message Open MOM de mm est envoyé à une fenêtre lorsqu’un appareil de sortie MIDI est ouvert.
ms.assetid: 1374a07c-02fa-4b43-82df-cbd96302aec5
keywords:
- message MM_MOM_OPEN Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f676dccf532290ab2153b888c20fad7b19d98d
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364515"
---
# <a name="mm_mom_open-message"></a>MM \_ \_ message ouvert MOM

Le **message \_ \_ Open MOM de mm** est envoyé à une fenêtre lorsqu’un appareil de sortie MIDI est ouvert.


```C++
MM_MOM_OPEN 
wParam = (WPARAM) hOutput 
lParam = reserved 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*
</dt> <dd>

Handle sur le périphérique de sortie MIDI.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Réservé n’utilisez pas.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Mmsystem. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Messages MIDI](midi-messages.md)
</dt> </dl>

 

 





