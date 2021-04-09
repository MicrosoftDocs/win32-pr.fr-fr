---
description: Déclenché par la source de Sequencer lorsqu’un segment est terminé et qu’il est suivi d’un autre segment. Lorsque le segment final est terminé, la source de Sequencer déclenche un événement MEEndOfPresentation.
ms.assetid: 1be13c9a-d454-4642-b26b-556f2461b705
title: Événement MEEndOfPresentationSegment (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d3608f51f3ff66e21261cc40d1f8cf690c92c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863621"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> <dt>

[À propos de la source de Sequencer](about-the-sequencer-source.md)
</dt> <dt>

[Événements de source de Sequencer](sequencer-source-events.md)
</dt> </dl>

 

 




