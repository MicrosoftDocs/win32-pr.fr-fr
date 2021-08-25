---
description: Déclenché par le convertisseur audio lorsque les paramètres de regroupement changent pour la session audio.
ms.assetid: d6f7757c-fd91-40bd-b2b5-a3e808445250
title: Événement MEAudioSessionGroupingParamChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9a271ebaa4e3a0044dc425de2d6a7f313e17d63c693acede63773e94619c6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957509"
---
# <a name="meaudiosessiongroupingparamchanged-event"></a>Événement MEAudioSessionGroupingParamChanged

Déclenché par le convertisseur audio lorsque les paramètres de regroupement changent pour la session audio.

La session multimédia transmet cet événement à l’application.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE                | Description                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ inconnu<br/> | Pointeur vers l’interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .<br/> <br/> |



## <a name="remarks"></a>Remarques

Cet événement est envoyé par le récepteur de flux du convertisseur audio. L’événement est déclenché lorsque le convertisseur audio reçoit un événement [**IAudioSessionEvents :: OnGroupingParamChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ongroupingparamchanged) à partir de la session audio.

Pour récupérer les nouveaux paramètres de regroupement, appelez [**IMFAudioPolicy :: GetGroupingParam**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> <dt>

[**IMFAudioPolicy::GetGroupingParam**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam)
</dt> <dt>

[Convertisseur audio de streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 
