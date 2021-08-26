---
title: Message MOM_CLOSE (mmsystem. h)
description: Le \_ message de fermeture MOM est envoyé à une fonction de rappel de sortie MIDI lorsqu’un périphérique de sortie MIDI est fermé.
ms.assetid: 229b3701-16f1-4ec8-920e-cd8231561541
keywords:
- message MOM_CLOSE Windows Multimedia
topic_type:
- apiref
api_name:
- MOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbabd0cae61c1b1ea3d88df3cd2e52524b779eb7cdb5ac2c1e1a371546724f44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038869"
---
# <a name="mom_close-message"></a>\_Message de fermeture MOM

Le message de **\_ fermeture MOM** est envoyé à une fonction de rappel de sortie MIDI lorsqu’un périphérique de sortie MIDI est fermé.


```C++
MOM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Réservé n’utilisez pas.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Réservé n’utilisez pas.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Le descripteur d’appareil n’est plus valide une fois que ce message a été envoyé.

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

 

 





