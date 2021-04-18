---
description: Envoyé par le convertisseur audio de streaming (SAR) lorsque l’état du volume ou du silence de la session audio change.
ms.assetid: 63c37bd2-0289-407a-92f1-169eb5d2e02e
title: Événement MEAudioSessionVolumeChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429edd8a26ed7f4ca1e764c7fbea1c6930c4871c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520384"
---
# <a name="meaudiosessionvolumechanged-event"></a>Événement MEAudioSessionVolumeChanged

Envoyé par le convertisseur audio de streaming (SAR) lorsque l’état du volume ou du silence de la session audio change.

La session multimédia transmet cet événement à l’application.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE                | Description                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ vide<br/>   | Aucune donnée d'événement.<br/> <br/>                                                     |
| VT \_ inconnu<br/> | Pointeur vers l’interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .<br/> <br/> |



## <a name="remarks"></a>Notes

Cet événement est déclenché par le récepteur de flux de la RAS. L’événement est déclenché lorsque le SAR reçoit un événement [**IAudioSessionEvents :: OnSimpleVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) à partir de la session audio. Pour accéder au nouveau niveau de volume et à l’État muet, appelez [**IMFSimpleAudioVolume :: GetMasterVolume**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmastervolume) et [**IMFSimpleAudioVolume :: GetMute**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmute).

Le SAR envoie cet événement si une action externe modifie le volume, par exemple, si l’utilisateur modifie le volume par le biais du programme de contrôle de volume système (SndVol). Le SAR n’envoie pas l’événement si l’application modifie le volume directement sur le SAR.

En outre, le SAR n’envoie pas cet événement lorsque le volume du canal change ([**IAudioSessionEvents :: OnChannelVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Convertisseur audio de streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 
