---
title: Message WOM_DONE (mmsystem. h)
description: Le \_ message WOM Done est envoyé à une fonction de rappel de sortie Waveform Audio lorsque la mémoire tampon de sortie donnée est retournée à l’application.
ms.assetid: cac94a44-d1b0-43de-b3ec-ae34547b1fc3
keywords:
- message WOM_DONE Windows Multimedia
topic_type:
- apiref
api_name:
- WOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab64598a2dfdd329615ca116fb6382909bb83b01
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194840"
---
# <a name="wom_done-message"></a>\_Message WOM terminé

Le message **WOM \_ done** est envoyé à une fonction de rappel de sortie Waveform Audio lorsque la mémoire tampon de sortie donnée est retournée à l’application. Les tampons sont retournés à l’application lorsqu’ils ont été lus, ou à la suite d’un appel à la fonction [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) .


```C++
WOM_DONE 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Pointeur vers une structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) identifiant la mémoire tampon.

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

 

