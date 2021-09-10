---
title: Message MOM_POSITIONCB (mmsystem. h)
description: Le \_ message de position MOM est envoyé lorsqu’un \_ \_ événement de rappel MEVT F est atteint dans le flux de sortie MIDI.
ms.assetid: 0464d74d-7d1f-4aab-a9e7-03397872f3c0
keywords:
- message MOM_POSITIONCB Windows Multimedia
topic_type:
- apiref
api_name:
- MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c9528e8f91778c53ed4761c98bb67d405ec14
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364555"
---
# <a name="mom_positioncb-message"></a>\_Message MOM POSITIONCB

Le message de **\_ position MOM** est envoyé lorsqu’un événement de **\_ \_ rappel MEVT F** est atteint dans le flux de sortie MIDI.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Pointeur vers une structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) identifiant la mémoire tampon d’entrée.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Non utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La lecture de la mémoire tampon de flux continue même pendant l’exécution de la fonction de rappel. Les événements qui se trouvent après l’événement de **\_ \_ rappel MEVT F** dans la mémoire tampon sont planifiés et envoyés à temps, quel que soit le temps passé dans la fonction de rappel.

Si les rappels de position sont générés plus rapidement que votre application ne peut les traiter, le membre **dwOffset** de la structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) peut faire référence à un événement que votre application n’a pas encore traitée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Mmsystem. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Messages MIDI](midi-messages.md)
</dt> </dl>

 

