---
description: envoyé par une source de capture audio lorsque la dession audio est déconnectée, car l’utilisateur s’est déconnecté d’une session Terminal Windowsing Services (WTS).
ms.assetid: 88B24E79-FEB8-46AF-9A6C-3FB426089584
title: Événement MECaptureAudioSessionDisconnected (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 567df4839776ecacb5e25992f5f8cef4795186cffc53fb8abb433418066f3c40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114169"
---
# <a name="mecaptureaudiosessiondisconnected-event"></a>Événement MECaptureAudioSessionDisconnected

envoyé par une source de capture audio lorsque la dession audio est déconnectée, car l’utilisateur s’est déconnecté d’une session Terminal Windowsing Services (WTS).

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE               | Description                           |
|-----------------------|---------------------------------------|
| VT \_ vide <br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="remarks"></a>Remarques

Cet événement est envoyé par le flux multimédia de la source de capture audio.

La source de capture envoie cet événement lorsqu’il reçoit un événement [**IAudioSessionEvents :: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) à partir de la session audio avec la raison de la déconnexion égale à **DisconnectReasonSessionDisconnected**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 
