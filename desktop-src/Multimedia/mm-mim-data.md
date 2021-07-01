---
title: Message MM_MIM_DATA (mmsystem. h)
description: Le \_ message de \_ données MIM mm est envoyé à une fenêtre lorsqu’un message MIDI complet est reçu par un périphérique d’entrée MIDI.
ms.assetid: 9c580e48-78f3-4914-bdea-393823fb8482
keywords:
- Message MM_MIM_DATA Windows Multimedia
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
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119694"
---
# <a name="mm_mim_data-message"></a>MM \_ \_ message de données MIM

Le message de **\_ \_ données MIM mm** est envoyé à une fenêtre lorsqu’un message MIDI complet est reçu par un périphérique d’entrée MIDI.


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



| Condition requise | Value | Description |
|-----------|-----------------|-----------------------------------------------------|
| Mot haut | Octet de poids fort | Non utilisé.                                           |
|           | Octet de poids faible  | Contient un deuxième octet de données MIDI (si nécessaire).  |
| Mot bas  | Octet de poids fort | Contient le premier octet des données MIDI (si nécessaire). |
|           | Octet de poids faible  | Contient l’État MIDI.                           |



 

Les deux octets de données MIDI sont facultatifs, en fonction de l’octet d’État MIDI.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

L’état d’exécution des messages MIDI reçus d’un port d’entrée MIDI est désactivé ; chaque message est développé pour inclure l’octet d’État MIDI.

Ce message n’est pas envoyé lorsqu’un message MIDI système exclusif est reçu. Aucun horodatage n’est disponible avec ce message. Pour les données d’entrée horodatées, vous devez utiliser les messages envoyés aux fonctions de rappel.

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

 

 





