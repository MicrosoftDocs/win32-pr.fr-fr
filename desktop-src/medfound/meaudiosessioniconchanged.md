---
description: Déclenché par le convertisseur audio lorsque l’icône de session audio change.
ms.assetid: 72aae901-e5fe-481d-babb-459038abd629
title: Événement MEAudioSessionIconChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7a12a4e82585c270206d595d32ba82c4e9e594
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531865"
---
# <a name="meaudiosessioniconchanged-event"></a>Événement MEAudioSessionIconChanged

Déclenché par le convertisseur audio lorsque l’icône de session audio change.

La session multimédia transmet cet événement à l’application.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE                | Description                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ vide<br/>   | Aucune donnée d'événement.<br/> <br/>                                                     |
| VT \_ inconnu<br/> | Pointeur vers l’interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .<br/> <br/> |



## <a name="remarks"></a>Notes

Cet événement est envoyé par le récepteur de flux du convertisseur audio. L’événement est déclenché lorsque le convertisseur audio reçoit un événement [**IAudioSessionEvents :: OnIconPathChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-oniconpathchanged) à partir de la session audio.

Pour afficher la nouvelle icône, appelez [**IMFAudioPolicy :: GetIconPath**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFAudioPolicy::GetIconPath**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath)
</dt> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Convertisseur audio de streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 
