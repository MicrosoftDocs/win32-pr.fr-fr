---
title: Message MM_MOM_POSITIONCB (mmsystem. h)
description: Le \_ message de \_ POSITIONCB MOM mm est envoyé à une fenêtre lorsqu’un \_ \_ événement de rappel MEVT F est atteint dans le flux de sortie MIDI.
ms.assetid: afd2ba4c-ff6a-4e47-a7e8-a0da62650963
keywords:
- message MM_MOM_POSITIONCB Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f68afecddd9b6ca8a0e5f6305b430b059b93db5a2abb966c0a7aed9ab350f7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807159"
---
# <a name="mm_mom_positioncb-message"></a>\_Message POSITIONCB MOM de mm \_

Le message de **\_ \_ POSITIONCB MOM mm** est envoyé à une fenêtre lorsqu’un \_ \_ événement de rappel MEVT F est atteint dans le flux de sortie MIDI.


```C++
MM_MOM_POSITIONCB 
wParam = (WPARAM) lpMidiHdr 
lParam = reserved 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Pointeur vers une structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) qui identifie l’événement qui a provoqué le rappel. Le membre **dwOffset** donne le décalage de l’événement.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Réservé n’utilisez pas.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La lecture de la mémoire tampon de flux continue même pendant l’exécution de la fonction de rappel. Les événements qui se trouvent après l' \_ \_ événement de rappel MEVT F dans la mémoire tampon sont planifiés et envoyés à temps, quel que soit le temps passé dans la fonction de rappel.

Si les rappels de position sont générés plus rapidement que votre application ne peut les traiter, le membre **dwOffset** de la structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) peut faire référence à un événement que votre application n’a pas encore traitée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Mmsystem. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Messages MIDI](midi-messages.md)
</dt> </dl>

 

