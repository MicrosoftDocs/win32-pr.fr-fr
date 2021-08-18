---
description: Envoyé par une source de capture audio lorsque le volume change.
ms.assetid: 4A525D5F-9226-4277-BDB7-174BF65FE320
title: Événement MECaptureAudioSessionVolumeChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78f2e83bdf03f61abac733a5e06310ff12c0797664d6a2405aed97210bf5ff42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878079"
---
# <a name="mecaptureaudiosessionvolumechanged-event"></a>Événement MECaptureAudioSessionVolumeChanged

Envoyé par une source de capture audio lorsque le volume change.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE               | Description                           |
|-----------------------|---------------------------------------|
| VT \_ vide <br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="remarks"></a>Remarques

Cet événement est envoyé par le flux multimédia de la source de capture audio.

La source de capture audio envoie cet événement si une action externe modifie le volume, par exemple, si l’utilisateur modifie le volume par le biais du panneau de configuration. La source de capture n’envoie pas l’événement si l’application modifie le volume directement sur la source.

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

 

 




