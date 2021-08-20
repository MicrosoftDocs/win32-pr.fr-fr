---
title: Message MIM_LONGDATA (mmsystem. h)
description: le \_ message MIM LONGDATA est envoyé à une fonction de rappel d’entrée MIDI lorsqu’un tampon système exclusif a été rempli de données et est retourné à l’application.
ms.assetid: 3a11ed21-e7c5-4b78-9536-f0d862e26a02
keywords:
- message MIM_LONGDATA Windows Multimedia
topic_type:
- apiref
api_name:
- MIM_LONGDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82605835ce8ac231346014215c854abfe9ae7a55fd81e81b8d6214fb8a230327
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137210"
---
# <a name="mim_longdata-message"></a>MIM \_ Message LONGDATA

le message **MIM \_ LONGDATA** est envoyé à une fonction de rappel d’entrée MIDI lorsqu’un tampon système exclusif a été rempli de données et est retourné à l’application.


```C++
MIM_LONGDATA 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Pointeur vers une structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) identifiant la mémoire tampon d’entrée.

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*
</dt> <dd>

Heure à laquelle les données ont été reçues par le pilote de périphérique d’entrée. L’horodatage est spécifié en millisecondes, en commençant à zéro lorsque la fonction [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) a été appelée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La mémoire tampon retournée n’est peut-être pas pleine. Pour déterminer le nombre d’octets enregistrés dans la mémoire tampon retournée, utilisez le membre **dwBytesRecorded** de la structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) spécifiée par *lpMidiHdr*.

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

 

