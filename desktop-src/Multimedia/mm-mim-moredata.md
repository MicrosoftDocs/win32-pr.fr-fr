---
title: Message MM_MIM_MOREDATA (mmsystem. h)
description: le \_ message MM MIM \_ MOREDATA est envoyé à une fenêtre de rappel lorsqu’un message midi est reçu par un périphérique d’entrée midi, mais que l’application ne traite pas MIM des \_ messages de données suffisamment rapidement pour suivre le pilote de périphérique d’entrée.
ms.assetid: 25d507f9-01d4-4a9a-afdd-693d74e3bd22
keywords:
- message MM_MIM_MOREDATA Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIM_MOREDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3079c537ddca056ca690537c27edd95826de1189
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233747"
---
# <a name="mm_mim_moredata-message"></a>MM \_ MIM \_ message MOREDATA

le message **MM \_ MIM \_ MOREDATA** est envoyé à une fenêtre de rappel lorsqu’un message midi est reçu par un périphérique d’entrée midi, mais que l’application ne traite pas MIM des messages de [**\_ données**](mim-data.md) suffisamment rapidement pour suivre le pilote de périphérique d’entrée. La fenêtre reçoit ce message uniquement lorsque l’application spécifie l' \_ État des e/s midi \_ dans l’appel à la fonction [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .


```C++
MM_MIM_MOREDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*
</dt> <dd>

Handle vers l’appareil d’entrée MIDI qui a reçu le message MIDI.

</dd> <dt>

<span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*
</dt> <dd>

Spécifie le message MIDI qui a été reçu. Le message est empaqueté dans une valeur de mot double comme suit :



| Condition requise | Valeur | Description |
|-----------|-----------------|-----------------------------------------------------|
| Mot haut | Octet de poids fort | Non utilisé.                                           |
|           | Octet de poids faible  | Contient un deuxième octet de données MIDI (si nécessaire).  |
| Mot bas  | Octet de poids fort | Contient le premier octet des données MIDI (si nécessaire). |
|           | Octet de poids faible  | Contient l’État MIDI.                           |



 

Les deux octets de données MIDI sont facultatifs, en fonction de l’octet d’État MIDI.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si votre application reçoit des données MIDI plus rapidement qu’elle ne peut les traiter, vous ne devez pas utiliser un mécanisme de rappel de fenêtre. pour optimiser la vitesse, utilisez une fonction de rappel et utilisez le message [**MIM \_ MOREDATA**](mim-moredata.md) au lieu de MM \_ MIM \_ MOREDATA.

une application doit effectuer uniquement une quantité minimale de traitement de MM \_ MIM \_ messages MOREDATA. (En particulier, les applications ne doivent pas appeler la fonction [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) pendant le traitement de mm \_ MIM \_ MOREDATA.) Au lieu de cela, l’application doit placer les données d’événement dans une mémoire tampon, puis retourner.

lorsqu’une application reçoit un message de [**\_ \_ données de MIM mm**](mm-mim-data.md) après une série de messages de mm \_ MIM \_ MOREDATA, elle a détecté des événements MIDI entrants et peut appeler en toute sécurité des fonctions nécessitant beaucoup de temps.

L’état d’exécution des messages MIDI reçus d’un port d’entrée MIDI est désactivé ; chaque message est développé pour inclure l’octet d’État MIDI.

Ce message n’est pas envoyé lorsqu’un message MIDI système exclusif est reçu. Aucun horodatage n’est disponible avec ce message. Pour les données d’entrée horodatées, vous devez utiliser les messages envoyés aux fonctions de rappel.

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

 

