---
description: Déclenché par la source de Sequencer lorsqu’un segment est terminé et qu’il est suivi d’un autre segment. Lorsque le segment final est terminé, la source de Sequencer déclenche un événement MEEndOfPresentation.
ms.assetid: 1be13c9a-d454-4642-b26b-556f2461b705
title: Événement MEEndOfPresentationSegment (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b82f646ca76dbb6cc3cd8dc9e95dbaca2c55c504af261924918dbf790411e7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013699"
---
# <a name="meendofpresentationsegment-event"></a>Événement MEEndOfPresentationSegment

Déclenché par la source de Sequencer lorsqu’un segment est terminé et qu’il est suivi d’un autre segment. Lorsque le segment final est terminé, la source de Sequencer déclenche un événement [MEEndOfPresentation](meendofpresentation.md) .

La session multimédia transmet cet événement à l’application.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="attributes"></a>Attributs

Les attributs suivants sont définis pour cet événement.



| Attribut                                                                                               | Description                                                                          |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**TOPOLOGIE de la \_ source d’événements MF \_ \_ \_ annulée**](mf-event-source-topology-canceled-attribute.md)<br/> | Spécifie si la source de Sequencer a annulé ce segment.<br/> <br/> |



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

[À propos de la source de Sequencer](about-the-sequencer-source.md)
</dt> <dt>

[Événements de source de Sequencer](sequencer-source-events.md)
</dt> </dl>

 

 




