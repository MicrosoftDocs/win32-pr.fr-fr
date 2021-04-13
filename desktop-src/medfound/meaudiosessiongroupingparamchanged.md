---
description: Déclenché par le convertisseur audio lorsque les paramètres de regroupement changent pour la session audio.
ms.assetid: d6f7757c-fd91-40bd-b2b5-a3e808445250
title: Événement MEAudioSessionGroupingParamChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ac115bb30a4c01247da537f3255e9bc40099e3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201678"
---
# <a name="meaudiosessiongroupingparamchanged-event"></a>Événement MEAudioSessionGroupingParamChanged

Déclenché par le convertisseur audio lorsque les paramètres de regroupement changent pour la session audio.

La session multimédia transmet cet événement à l’application.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE                | Description                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ inconnu<br/> | Pointeur vers l’interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .<br/> <br/> |



## <a name="remarks"></a>Notes

Cet événement est envoyé par le récepteur de flux du convertisseur audio. L’événement est déclenché lorsque le convertisseur audio reçoit un événement [**IAudioSessionEvents :: OnGroupingParamChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ongroupingparamchanged) à partir de la session audio.

Pour récupérer les nouveaux paramètres de regroupement, appelez [**IMFAudioPolicy :: GetGroupingParam**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam).

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

[**IMFAudioPolicy::GetGroupingParam**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam)
</dt> <dt>

[Convertisseur audio de streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 
