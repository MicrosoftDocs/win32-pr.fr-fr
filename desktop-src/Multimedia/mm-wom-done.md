---
title: Message MM_WOM_DONE (mmsystem. h)
description: Le \_ message mm WOM \_ done est envoyé à une fenêtre lorsque la mémoire tampon de sortie donnée est retournée à l’application. Les tampons sont retournés à l’application lorsqu’ils ont été lus, ou à la suite d’un appel à la fonction waveOutReset.
ms.assetid: bbdebb68-82e5-4963-90bb-f93f8a91a8cf
keywords:
- Message MM_WOM_DONE Windows Multimedia
topic_type:
- apiref
api_name:
- MM_WOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7198aa2f60a7f5a0e6d839a3ee5b453a3a4d3f59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743916"
---
# <a name="mm_wom_done-message"></a>MM \_ \_ message terminé WOM

Le message **mm \_ WOM \_ done** est envoyé à une fenêtre lorsque la mémoire tampon de sortie donnée est retournée à l’application. Les tampons sont retournés à l’application lorsqu’ils ont été lus, ou à la suite d’un appel à la fonction [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) .


```C++
MM_WOM_DONE 
wParam = (WPARAM) hOutputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*
</dt> <dd>

Handle sur le périphérique de sortie Waveform-Audio qui a joué la mémoire tampon.

</dd> <dt>

<span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*
</dt> <dd>

Pointeur vers une structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) identifiant la mémoire tampon.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>MMSYSTEM. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Sons Waveform](waveform-audio.md)
</dt> <dt>

[Messages de forme d’onde](waveform-messages.md)
</dt> </dl>

 

