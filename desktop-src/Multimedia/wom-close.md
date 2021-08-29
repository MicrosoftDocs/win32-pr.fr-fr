---
title: Message WOM_CLOSE (mmsystem. h)
description: Le \_ message WOM Close est envoyé à une fonction de rappel de sortie Waveform Audio lorsqu’un appareil de sortie Waveform-Audio est fermé. Le descripteur d’appareil n’est plus valide une fois que ce message a été envoyé.
ms.assetid: ac20216a-6a60-4e62-8241-3ca6f33567f1
keywords:
- message WOM_CLOSE Windows Multimedia
topic_type:
- apiref
api_name:
- WOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90ba0187638ec4bc0406066c9a50ee4ce53ca150e4dabc918a829cfaa08733b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803479"
---
# <a name="wom_close-message"></a>WOM \_ Fermer le message

Le message **WOM \_ Close** est envoyé à une fonction de rappel de sortie Waveform Audio lorsqu’un appareil de sortie Waveform-Audio est fermé. Le descripteur d’appareil n’est plus valide une fois que ce message a été envoyé.


```C++
WOM_CLOSE 
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

 

 





