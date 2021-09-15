---
description: Envoyé par une source de capture audio lorsqu’un autre programme ouvre le périphérique audio en mode exclusif.
ms.assetid: E9CC8507-38AB-4049-8DAC-767EC0ECE270
title: Événement MECaptureAudioSessionExclusiveModeOverride (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2051e6073b06f62823b95c80d7d4cfaf21de2f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530813"
---
# <a name="mecaptureaudiosessionexclusivemodeoverride-event"></a>Événement MECaptureAudioSessionExclusiveModeOverride

Envoyé par une source de capture audio lorsqu’un autre programme ouvre le périphérique audio en mode exclusif.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE               | Description                           |
|-----------------------|---------------------------------------|
| VT \_ vide <br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="remarks"></a>Notes

Cet événement est envoyé par le flux multimédia de la source de capture audio.

La source de capture envoie cet événement lorsqu’il reçoit un événement [**IAudioSessionEvents :: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) à partir de la session audio avec la raison de la déconnexion égale à **DisconnectReasonExclusiveModeOverride**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 
