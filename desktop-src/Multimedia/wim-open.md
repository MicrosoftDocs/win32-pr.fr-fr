---
title: Message WIM_OPEN (mmsystem. h)
description: Le \_ message Wim Open est envoyé à une fonction de rappel d’entrée Waveform Audio quand un appareil d’entrée Waveform-Audio est ouvert.
ms.assetid: de18e6b2-ea28-46d9-812c-e6dac49838ee
keywords:
- message WIM_OPEN Windows Multimedia
topic_type:
- apiref
api_name:
- WIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57c1661482149c90cf3f2bd6b10620cb32f380be
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124367679"
---
# <a name="wim_open-message"></a>\_Message Wim ouvert

Le message **Wim \_ Open** est envoyé à une fonction de rappel d’entrée Waveform Audio quand un appareil d’entrée Waveform-Audio est ouvert.


```C++
WIM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Réservé doit être égal à zéro.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Réservé doit être égal à zéro.

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

[Sons Waveform](waveform-audio.md)
</dt> <dt>

[Messages de forme d’onde](waveform-messages.md)
</dt> </dl>

 

 





