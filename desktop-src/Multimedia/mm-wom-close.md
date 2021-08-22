---
title: Message MM_WOM_CLOSE (mmsystem. h)
description: Le \_ message de \_ fermeture de mm WOM est envoyé à une fenêtre lorsqu’un appareil de sortie Waveform-Audio est fermé. Le descripteur d’appareil n’est plus valide une fois que ce message a été envoyé.
ms.assetid: 6505b688-88a1-43b2-ad4e-2f88e496430a
keywords:
- message MM_WOM_CLOSE Windows Multimedia
topic_type:
- apiref
api_name:
- MM_WOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7624c85554fca997ce9542170e370711f8b3c3cefc22cf0e8d2fe9ea3e88687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065449"
---
# <a name="mm_wom_close-message"></a>MM \_ WOM \_ Fermer le message

Le message de **\_ \_ fermeture de mm WOM** est envoyé à une fenêtre lorsqu’un appareil de sortie Waveform-Audio est fermé. Le descripteur d’appareil n’est plus valide une fois que ce message a été envoyé.


```C++
MM_WOM_CLOSE 
wParam = (WPARAM) hOutputDev 
lParam = reserved 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*
</dt> <dd>

Handle vers l’appareil qui a été fermé.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
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

 

 





