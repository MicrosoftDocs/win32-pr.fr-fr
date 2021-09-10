---
title: Message MM_WIM_CLOSE (mmsystem. h)
description: Le \_ message de \_ fermeture de fichier WIM mm est envoyé à une fenêtre lorsqu’un périphérique d’entrée Waveform-Audio est fermé. Le descripteur d’appareil n’est plus valide une fois que ce message a été envoyé.
ms.assetid: 4ea35b66-6bfa-41f0-9d52-a8cf2b0a69dd
keywords:
- message MM_WIM_CLOSE Windows Multimedia
topic_type:
- apiref
api_name:
- MM_WIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d9934ef7045debbcac2f5baf1c2f750d22dad5
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124367580"
---
# <a name="mm_wim_close-message"></a>MM \_ \_ message de fermeture Wim

Le message de **\_ \_ fermeture de fichier WIM mm** est envoyé à une fenêtre lorsqu’un périphérique d’entrée Waveform-Audio est fermé. Le descripteur d’appareil n’est plus valide une fois que ce message a été envoyé.


```C++
MM_WIM_CLOSE 
wParam = (WPARAM) hInputDev 
lParam = reserved 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*
</dt> <dd>

Handle sur le périphérique d’entrée Waveform-Audio qui a été fermé.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
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

 

 





