---
title: Message MM_MIM_LONGDATA (mmsystem. h)
description: le \_ message MM MIM \_ LONGDATA est envoyé à une fenêtre lorsqu’un message complet du système MIDI est reçu ou lorsqu’une mémoire tampon a été remplie avec des données système exclusives.
ms.assetid: 72b9eade-4224-436f-bfef-32204eaf51ae
keywords:
- message MM_MIM_LONGDATA Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIM_LONGDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4748381500f42a5dc4f2bceae8ad862a64f237c9d5024e4b0b7cc96a694e5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065519"
---
# <a name="mm_mim_longdata-message"></a>MM \_ MIM \_ message LONGDATA

le message **MM \_ MIM \_ LONGDATA** est envoyé à une fenêtre lorsqu’un message complet du système MIDI est reçu ou lorsqu’une mémoire tampon a été remplie avec des données système exclusives.


```C++
MM_MIM_LONGDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*
</dt> <dd>

Handle vers l’appareil d’entrée MIDI qui a reçu les données.

</dd> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Pointeur vers une structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) identifiant la mémoire tampon.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La mémoire tampon retournée n’est peut-être pas pleine. Pour déterminer le nombre d’octets enregistrés dans la mémoire tampon retournée, utilisez le membre **dwBytesRecorded** de la structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) vers laquelle pointe *lpMidiHdr*.

Aucun horodatage n’est disponible avec ce message. Pour les données d’entrée horodatées, vous devez utiliser les messages envoyés aux fonctions de rappel.

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

 

