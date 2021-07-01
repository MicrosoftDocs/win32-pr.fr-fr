---
title: Message MIM_MOREDATA (mmsystem. h)
description: Le \_ message MIM MOREDATA est envoyé à une fonction de rappel d’entrée MIDI lorsqu’un message MIDI est reçu par un périphérique d’entrée MIDI, mais que l’application ne traite pas les \_ messages de données MIM suffisamment rapidement pour suivre le pilote de périphérique d’entrée.
ms.assetid: 74ed46ab-a18e-4df5-bf36-ab3dec7fafa5
keywords:
- Message MIM_MOREDATA Windows Multimedia
topic_type:
- apiref
api_name:
- MIM_MOREDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6342823e13a085b377a3e71f28a0f9ff016681c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119404"
---
# <a name="mim_moredata-message"></a>\_Message MIM MOREDATA

Le message **MIM \_ MOREDATA** est envoyé à une fonction de rappel d’entrée MIDI lorsqu’un message MIDI est reçu par un périphérique d’entrée MIDI, mais que l’application ne traite pas les messages de [**\_ données MIM**](mim-data.md) suffisamment rapidement pour suivre le pilote de périphérique d’entrée. La fonction de rappel reçoit ce message uniquement lorsque l’application spécifie l' \_ État des e/s midi \_ dans l’appel à la fonction [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .


```C++
MIM_MOREDATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*
</dt> <dd>

Spécifie le message MIDI qui a été reçu. Le message est compressé dans une valeur **DWORD** comme suit :



| Condition requise | Value | Description |
|-----------|-----------------|-----------------------------------------------------|
| Mot haut | Octet de poids fort | Non utilisé.                                           |
|           | Octet de poids faible  | Contient un deuxième octet de données MIDI (si nécessaire).  |
| Mot bas  | Octet de poids fort | Contient le premier octet des données MIDI (si nécessaire). |
|           | Octet de poids faible  | Contient l’État MIDI.                           |



 

Les deux octets de données MIDI sont facultatifs, en fonction de l’octet d’État MIDI.

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*
</dt> <dd>

Spécifie l’heure à laquelle le message a été reçu par le pilote de périphérique d’entrée. L’horodatage est spécifié en millisecondes, en commençant à 0 lorsque la fonction [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) a été appelée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Une application ne doit effectuer qu’une quantité minime de traitement des \_ messages MIM MOREDATA. (En particulier, les applications ne doivent pas appeler la fonction [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) lors du traitement de MIM \_ MOREDATA.) Au lieu de cela, l’application doit placer les données d’événement dans une mémoire tampon, puis retourner.

Lorsqu’une application reçoit un message de [**\_ données MIM**](mim-data.md) après une série de \_ messages MIM MOREDATA, elle a détecté des événements MIDI entrants et peut appeler en toute sécurité des fonctions nécessitant beaucoup de temps.

L’état d’exécution des messages MIDI reçus d’un port d’entrée MIDI est désactivé ; chaque message est développé pour inclure l’octet d’État MIDI.

Ce message n’est pas envoyé lorsqu’un message MIDI système exclusif est reçu.

## <a name="requirements"></a>Spécifications



| Condition requise | Value |
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

 

