---
title: Message MM_MIM_DATA (mmsystem. h)
description: le \_ message de \_ données de MIM MM est envoyé à une fenêtre lorsqu’un message midi complet est reçu par un périphérique d’entrée midi.
ms.assetid: 9c580e48-78f3-4914-bdea-393823fb8482
keywords:
- message MM_MIM_DATA Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2a79a5a4ab6b0422705fe737ba3da4a6fd4f923
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233784"
---
# <a name="mm_mim_data-message"></a>MM \_ MIM \_ message de données

le message de **\_ \_ données de MIM MM** est envoyé à une fenêtre lorsqu’un message midi complet est reçu par un périphérique d’entrée midi.


```C++
MM_MIM_DATA 
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

Message MIDI qui a été reçu. Le message est empaqueté dans une valeur de mot double comme suit :



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

 

 





