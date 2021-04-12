---
description: Signale un événement à partir d’un récepteur multimédia qui restitue des données multimédias.
ms.assetid: bb7db7c9-c39f-4bf4-9412-42525c4f2ea3
title: Événement MERendererEvent (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c52e15bfbe97743e8af10a79cf3ef1d94626a877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202004"
---
# <a name="merendererevent-event"></a>Événement MERendererEvent

Signale un événement à partir d’un récepteur multimédia qui restitue des données multimédias.

Le [convertisseur vidéo amélioré](enhanced-video-renderer.md) (EVR) envoie cet événement lorsqu’il reçoit un événement utilisateur du présentateur EVR.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE           | Description                        |
|-------------------|------------------------------------|
| VT \_<br/> | Code d’événement.<br/> <br/> |



## <a name="remarks"></a>Notes

Si le présenteur appelle la méthode **IMediaEventSink :: Notify** du EVR à l’aide d’un code d’événement dans la plage EC \_ ou supérieure, le EVR envoie cet événement. Les données d’événement sont le code d’événement qui a été passé à la méthode **Notify** .

Les paramètres d’événement d’origine (*EventParam1* et *EventParam2* dans la méthode **IMediaEventSink :: Notify** ) sont ignorés, donc le présenteur doit définir ces valeurs sur **null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




