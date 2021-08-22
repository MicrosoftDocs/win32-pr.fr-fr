---
description: Envoyé par une source de capture audio lorsque la session audio de capture est déconnectée en raison de l’arrêt du serveur audio.
ms.assetid: 43284B3E-3018-44F3-8D6C-8C3041DCCD3E
title: Événement MECaptureAudioSessionServerShutdown (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb19d72a207866ceb405baacd11dbb3f91f059abb3d3855feba159040c27760
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974258"
---
# <a name="mecaptureaudiosessionservershutdown-event"></a>Événement MECaptureAudioSessionServerShutdown

Envoyé par une source de capture audio lorsque la session audio de capture est déconnectée en raison de l’arrêt du serveur audio.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE               | Description                           |
|-----------------------|---------------------------------------|
| VT \_ vide <br/> | Aucune donnée d'événement.<br/> <br/> |



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

 

 




