---
title: Message MM_MOM_DONE (mmsystem. h)
description: Le message de fin de la \_ \_ configuration MOM est envoyé à une fenêtre lorsque la mémoire tampon de flux ou exclusive système midi spécifiée a été lue et est retournée à l’application.
ms.assetid: 4651d5b4-3c98-4fa7-b761-dafb30e0d31e
keywords:
- message MM_MOM_DONE Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4fcbcde545c7d29a313e729761c2e565db3405b10faf3156d9ef7dd0585b16b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807139"
---
# <a name="mm_mom_done-message"></a>MM \_ \_ message terminé MOM

Le message de **\_ \_ fin** de la configuration MOM est envoyé à une fenêtre lorsque la mémoire tampon de flux ou exclusive système midi spécifiée a été lue et est retournée à l’application.


```C++
MM_MOM_DONE 
wParam = (WPARAM) hOutput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*
</dt> <dd>

Handle sur le périphérique de sortie MIDI qui a joué la mémoire tampon.

</dd> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Pointeur vers une structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) identifiant la mémoire tampon.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Mmsystem. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Messages MIDI](midi-messages.md)
</dt> </dl>

 

