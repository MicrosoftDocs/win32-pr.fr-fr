---
description: déclenché par le convertisseur audio lorsque l’Windows système du serveur audio est arrêté. Le convertisseur audio n’est plus valide.
ms.assetid: 8e80903c-d6ce-4fa2-87db-552c7fba3c6a
title: Événement MEAudioSessionServerShutdown (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca1f9a4aa9e2ba0e9c57b21a45aa3806a8538e3e81cb16a2f208677d78cbacf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118062431"
---
# <a name="meaudiosessionservershutdown-event"></a>Événement MEAudioSessionServerShutdown

déclenché par le convertisseur audio lorsque l’Windows système du serveur audio est arrêté. Le convertisseur audio n’est plus valide.

La session multimédia transmet cet événement à l’application.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE                | Description                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ vide<br/>   | Aucune donnée d'événement.<br/> <br/>                                                     |
| VT \_ inconnu<br/> | Pointeur vers l’interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .<br/> <br/> |



## <a name="remarks"></a>Remarques

Cet événement est envoyé par le récepteur de flux du convertisseur audio. L’événement est déclenché lorsque le convertisseur audio reçoit un événement [**IAudioSessionEvents :: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) à partir de la session audio avec la raison de la déconnexion égale à **DisconnectReasonServerShutdown**.

Le pointeur [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) , s’il est défini, n’est pas utile, car le flux audio n’est plus valide.

## <a name="requirements"></a>Conditions requises



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

 

 
