---
title: Message MM_MIM_ERROR (mmsystem. h)
description: le \_ \_ message d’erreur MM MIM est envoyé à une fenêtre lorsqu’un message MIDI non valide est reçu.
ms.assetid: 03760bfc-a4ef-48cd-97a9-1b93b56fc641
keywords:
- message MM_MIM_ERROR Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIM_ERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b45988259601b40a804f9eb8acfbb085bddcda
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364423"
---
# <a name="mm_mim_error-message"></a>MM \_ MIM \_ message d’erreur

le message d' **\_ \_ erreur MM MIM** est envoyé à une fenêtre lorsqu’un message MIDI non valide est reçu.


```C++
MM_MIM_ERROR 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*
</dt> <dd>

Handle vers l’appareil d’entrée MIDI qui a reçu le message non valide.

</dd> <dt>

<span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*
</dt> <dd>

Message MIDI non valide. Le message est empaqueté dans une valeur **DWORD** avec le premier octet du message dans l’octet de poids faible.

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

 

 





