---
title: Message WIM_DATA (mmsystem. h)
description: Le \_ message de données Wim est envoyé à la fonction de rappel d’entrée Wave-Audio donnée quand des données Waveform-Audio sont présentes dans la mémoire tampon d’entrée et que la mémoire tampon est retournée à l’application.
ms.assetid: 94cc02b8-61c4-44b9-9f8e-041fe989c1a6
keywords:
- Message WIM_DATA Windows Multimedia
topic_type:
- apiref
api_name:
- WIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28bcfdd249dda5621d4914d75d3ffc7b13e4d767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510167"
---
# <a name="wim_data-message"></a>\_Message de données Wim

Le message de **\_ données Wim** est envoyé à la fonction de rappel d’entrée Wave-Audio donnée quand des données Waveform-Audio sont présentes dans la mémoire tampon d’entrée et que la mémoire tampon est retournée à l’application. Le message peut être envoyé lorsque la mémoire tampon est saturée ou après l’appel de la fonction [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) .


```C++
WIM_DATA 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Pointeur vers une structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) qui identifie la mémoire tampon contenant les données.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Réservé doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La mémoire tampon retournée n’est peut-être pas pleine. Utilisez le membre **dwBytesRecorded** de la structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) spécifiée par *lpwvhdr* pour déterminer le nombre d’octets enregistrés dans la mémoire tampon retournée.

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

 

