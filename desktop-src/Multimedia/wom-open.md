---
title: Message WOM_OPEN (mmsystem. h)
description: Le \_ message WOM Open est envoyé à une fonction de rappel de sortie Waveform Audio lorsqu’un appareil de sortie Waveform-Audio est ouvert.
ms.assetid: 7fa175d3-7c07-4ca0-a0bd-4526fbc24f8d
keywords:
- message WOM_OPEN Windows Multimedia
topic_type:
- apiref
api_name:
- WOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77d0e145bf533bf9b48b88a87d449679e7728b679e72ed70a787168b5936f5aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940656"
---
# <a name="wom_open-message"></a>WOM \_ ouvrir le message

Le message **WOM \_ Open** est envoyé à une fonction de rappel de sortie Waveform Audio lorsqu’un appareil de sortie Waveform-Audio est ouvert.


```C++
WOM_OPEN 
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

## <a name="requirements"></a>Configuration requise



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

 

 





