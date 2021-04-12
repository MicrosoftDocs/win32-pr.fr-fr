---
title: Message MOM_DONE (Mciapi. h)
description: Le \_ message de travail effectué par MOM est envoyé à une fonction de rappel de sortie MIDI lorsque la mémoire tampon de flux ou l’exclusivité système spécifiée a été lue et est retournée à l’application.
ms.assetid: 0b9bd0e1-c87d-4f21-912e-5ac9f5c04192
keywords:
- Message MOM_DONE Windows Multimedia
topic_type:
- apiref
api_name:
- MOM_DONE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af3f58f7d8f4625971dde5d7ec807c9f963d40f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384395"
---
# <a name="mom_done-message"></a>Message de fin de MOM \_

Le message de **\_ travail effectué par MOM** est envoyé à une fonction de rappel de sortie MIDI lorsque la mémoire tampon de flux ou l’exclusivité système spécifiée a été lue et est retournée à l’application.


```C++
MOM_DONE 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = reserved 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Pointeur vers une structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) identifiant la mémoire tampon.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Réservé n’utilisez pas.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Messages MIDI](midi-messages.md)
</dt> </dl>

 

