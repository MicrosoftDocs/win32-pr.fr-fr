---
description: déclenché par le convertisseur audio lorsque la session audio est déconnectée d’une session Terminal Windowsing Services (WTS). Le convertisseur audio n’est plus valide.
ms.assetid: 08f9844c-f3b1-4d60-990e-9131f3312f6b
title: Événement MEAudioSessionDisconnected (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db2d31349585d26c61cb2940cea70ddaf0617901
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531877"
---
# <a name="meaudiosessiondisconnected-event"></a>Événement MEAudioSessionDisconnected

déclenché par le convertisseur audio lorsque la session audio est déconnectée d’une session Terminal Windowsing Services (WTS). Le convertisseur audio n’est plus valide.

La session multimédia transmet cet événement à l’application.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE                | Description                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ vide<br/>   | Aucune donnée d'événement.<br/> <br/>                                                     |
| VT \_ inconnu<br/> | Pointeur vers l’interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .<br/> <br/> |



## <a name="remarks"></a>Notes

Cet événement est envoyé par le récepteur de flux du convertisseur audio. L’événement est déclenché lorsque le convertisseur audio reçoit un événement [**IAudioSessionEvents :: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) à partir de la session audio avec la raison de la déconnexion égale à DisconnectReasonSessionDisconnected.

Le pointeur [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) , s’il est défini, n’est pas utile, car le flux audio n’est plus valide.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Convertisseur audio de streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 
