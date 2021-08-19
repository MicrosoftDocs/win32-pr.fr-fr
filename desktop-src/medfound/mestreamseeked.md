---
description: 'Déclenché par un flux de média après un appel à IMFMediaSource :: START provoque une recherche dans le flux. Un flux de média déclenche cet événement lorsque la source du média déclenche l’événement MESourceSeeked.'
ms.assetid: df06df16-711d-4262-b049-fb29f25934de
title: Événement MEStreamSeeked (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b03e58b11785a7b807f6793ff2ba6b2a4afa5f912d21e626938d7b3c725242f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061334"
---
# <a name="mestreamseeked-event"></a>Événement MEStreamSeeked

Déclenché par un flux de média après un appel à [**IMFMediaSource :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) provoque une recherche dans le flux. Un flux de média déclenche cet événement lorsque la source du média déclenche l’événement [MESourceSeeked](mesourceseeked.md) .

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE           | Description                                                        |
|-------------------|--------------------------------------------------------------------|
| Le \_ i8 VT<br/> | Nouvelle heure de début, en unités de 100 nanosecondes.<br/> <br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




