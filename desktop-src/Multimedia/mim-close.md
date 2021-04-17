---
title: Message MIM_CLOSE (mmsystem. h)
description: Le \_ message de fermeture MIM est envoyé à une fonction de rappel d’entrée MIDI lorsqu’un périphérique d’entrée MIDI est fermé.
ms.assetid: c19ecd3a-c3a5-4f17-9d44-d0d71eefcb15
keywords:
- Message MIM_CLOSE Windows Multimedia
topic_type:
- apiref
api_name:
- MIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5549d9bef1e802b0b34ab6437b1386519a25d349
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508329"
---
# <a name="mim_close-message"></a>\_Message de fermeture MIM

Le message de **\_ fermeture MIM** est envoyé à une fonction de rappel d’entrée MIDI lorsqu’un périphérique d’entrée MIDI est fermé.


```C++
MIM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Réservé n’utilisez pas.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Réservé n’utilisez pas.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le descripteur d’appareil n’est plus valide une fois que ce message a été envoyé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>MMSYSTEM. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interface MIDI (Musical Instrument Digital Interface)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[Messages MIDI](midi-messages.md)
</dt> </dl>

 

 





