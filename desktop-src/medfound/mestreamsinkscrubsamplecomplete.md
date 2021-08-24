---
description: Déclenché par un récepteur de flux lorsqu’il termine une demande de nettoyage.
ms.assetid: 451c7e09-868e-4c05-b970-d222b97223f2
title: Événement MEStreamSinkScrubSampleComplete (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ae6e0ea7a90db33fe21d39017ac99908ace86bb263e0ad6e2047f70e70f5de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715169"
---
# <a name="mestreamsinkscrubsamplecomplete-event"></a>Événement MEStreamSinkScrubSampleComplete

Déclenché par un récepteur de flux lorsqu’il termine une demande de nettoyage.

Le nettoyage se produit lorsque la vitesse de lecture est égale à zéro et que l’horloge de la présentation est démarrée avec une heure de srubbing spécifiée. Si un récepteur multimédia prend en charge le nettoyage, chaque flux du récepteur déclenche cet événement chaque fois que la méthode [**IMFClockStateSink :: OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) est appelée alors que la vitesse de lecture est égale à zéro.

Si le flux restitue des données lors du nettoyage, il envoie l’événement dès que les données sont restituées. Si le flux ne rend pas les données, il envoie l’événement immédiatement après l’appel de [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) .

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="attributes"></a>Attributs

Les attributs suivants sont définis pour cet événement.



| Attribut                                                                              | Description                                                                                                                                                   |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ heure SCRUBSAMPLE de l’événement MF \_**](mf-event-scrubsample-time-attribute.md)<br/> | Heure de présentation pour laquelle les données ont été rendues. Si le récepteur multimédia ne rend pas les données lors du nettoyage, il ne définit pas cet attribut.<br/> <br/> |



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

[Récepteurs de médias](media-sinks.md)
</dt> <dt>

[MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md)
</dt> </dl>

 

 




