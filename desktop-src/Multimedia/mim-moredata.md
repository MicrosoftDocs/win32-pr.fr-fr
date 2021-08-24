---
title: Message MIM_MOREDATA (mmsystem. h)
description: le message d’MIM \_ MOREDATA est envoyé à une fonction de rappel d’entrée midi lorsqu’un message midi est reçu par un périphérique d’entrée midi, mais que l’application ne traite pas MIM des \_ messages de données suffisamment rapidement pour suivre le pilote de périphérique d’entrée.
ms.assetid: 74ed46ab-a18e-4df5-bf36-ab3dec7fafa5
keywords:
- message MIM_MOREDATA Windows Multimedia
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
ms.openlocfilehash: 130a07d1d205e9944c7be6ab9ad1294e09d0ebdcdb81d5befc5468ff5a65218f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119782969"
---
# <a name="mim_moredata-message"></a>MIM \_ Message MOREDATA

le message d' **MIM \_ MOREDATA** est envoyé à une fonction de rappel d’entrée midi lorsqu’un message midi est reçu par un périphérique d’entrée midi, mais que l’application ne traite pas MIM des messages de [**\_ données**](mim-data.md) suffisamment rapidement pour suivre le pilote de périphérique d’entrée. La fonction de rappel reçoit ce message uniquement lorsque l’application spécifie l' \_ État des e/s midi \_ dans l’appel à la fonction [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .


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



| Condition requise | Valeur | Description |
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

une application ne doit effectuer qu’une quantité minime de traitement des \_ messages de MIM MOREDATA. (En particulier, les applications ne doivent pas appeler la fonction [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) lors du traitement des MIM \_ MOREDATA.) Au lieu de cela, l’application doit placer les données d’événement dans une mémoire tampon, puis retourner.

lorsqu’une application reçoit un message de [**\_ données de MIM**](mim-data.md) après une série de messages de MIM \_ MOREDATA, elle a détecté des événements MIDI entrants et peut appeler en toute sécurité des fonctions nécessitant beaucoup de temps.

L’état d’exécution des messages MIDI reçus d’un port d’entrée MIDI est désactivé ; chaque message est développé pour inclure l’octet d’État MIDI.

Ce message n’est pas envoyé lorsqu’un message MIDI système exclusif est reçu.

## <a name="requirements"></a>Configuration requise



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

 

