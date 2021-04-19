---
title: Message MM_WIM_DATA (mmsystem. h)
description: Le \_ message de \_ données Wim mm est envoyé à une fenêtre quand des données Waveform-Audio sont présentes dans la mémoire tampon d’entrée et que la mémoire tampon est retournée à l’application. Le message peut être envoyé lorsque la mémoire tampon est saturée ou après l’appel de la fonction waveInReset.
ms.assetid: 14298153-ea2f-40b7-bca7-196f4e6c1155
keywords:
- Message MM_WIM_DATA Windows Multimedia
topic_type:
- apiref
api_name:
- MM_WIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c663d669635116500bc8aa7e7fdc994cdccd6dfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106517325"
---
# <a name="mm_wim_data-message"></a>\_Message de données Wim de mm \_

Le message de **\_ \_ données Wim mm** est envoyé à une fenêtre quand des données Waveform-Audio sont présentes dans la mémoire tampon d’entrée et que la mémoire tampon est retournée à l’application. Le message peut être envoyé lorsque la mémoire tampon est saturée ou après l’appel de la fonction [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) .


```C++
MM_WIM_DATA 
wParam = (WPARAM) hInputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*
</dt> <dd>

Handle sur le périphérique d’entrée Waveform-Audio qui a reçu les données.

</dd> <dt>

<span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*
</dt> <dd>

Pointeur vers une structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) qui identifie la mémoire tampon contenant les données.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La mémoire tampon retournée n’est peut-être pas pleine. Utilisez le membre **dwBytesRecorded** de la structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) spécifiée par *lParam* pour déterminer le nombre d’octets enregistrés dans la mémoire tampon retournée.

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

 

