---
title: Message MM_MOM_CLOSE (mmsystem. h)
description: Le message de fermeture de MM \_ MOM \_ est envoyé à une fenêtre lorsqu’un périphérique de sortie MIDI est fermé.
ms.assetid: 4829bbe5-5103-4354-88a7-37def22e926e
keywords:
- message MM_MOM_CLOSE Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae55cbca7c5effc146dee0c5ef9be67469a9201
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364511"
---
# <a name="mm_mom_close-message"></a>Message de fermeture de \_ MOM mm \_

Le message de **\_ \_ fermeture de mm MOM** est envoyé à une fenêtre lorsqu’un périphérique de sortie MIDI est fermé.


```C++
MM_MOM_CLOSE 
wParam = (WPARAM) hOutput 
lParam = reserved 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*
</dt> <dd>

Handle sur le périphérique de sortie MIDI.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Réservé n’utilisez pas.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Le descripteur d’appareil n’est plus valide une fois que ce message a été envoyé.

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

 

 





