---
title: Message MIM_ERROR (mmsystem. h)
description: le MIM \_ message d’erreur est envoyé à une fonction de rappel d’entrée midi lorsqu’un message midi non valide est reçu.
ms.assetid: ea720da5-1f18-4d0d-ac9d-45cd1c3219d6
keywords:
- message MIM_ERROR Windows Multimedia
topic_type:
- apiref
api_name:
- MIM_ERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: add5b675a557ab25d41e79d99864e090364d384c
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364408"
---
# <a name="mim_error-message"></a>MIM \_ Message d’erreur

le **MIM \_** message d’erreur est envoyé à une fonction de rappel d’entrée midi lorsqu’un message midi non valide est reçu.


```C++
MIM_ERROR 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*
</dt> <dd>

Message MIDI non valide reçu. Le message est empaqueté dans une valeur de type double, avec le premier octet du message dans l’octet de poids faible.

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*
</dt> <dd>

Heure à laquelle le message a été reçu par le pilote de périphérique d’entrée. L’horodatage est spécifié en millisecondes, en commençant à zéro lorsque la fonction [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) a été appelée.

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

[Interface MIDI (Musical Instrument Digital Interface)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[Messages MIDI](midi-messages.md)
</dt> </dl>

 

