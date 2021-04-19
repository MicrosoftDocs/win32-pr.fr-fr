---
description: Déclenché par une source de média lorsqu’une présentation se termine. Cet événement signale que tous les flux de la présentation sont terminés. La session multimédia transmet cet événement à l’application.
ms.assetid: 259b00ae-a91b-461b-a12f-f7291ecc04ff
title: Événement MEEndOfPresentation (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e3a904725908d83afd54bbd64012420075037a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544252"
---
# <a name="meendofpresentation-event"></a>Événement MEEndOfPresentation

Déclenché par une source de média lorsqu’une présentation se termine. Cet événement signale que tous les flux de la présentation sont terminés. La session multimédia transmet cet événement à l’application.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="attributes"></a>Attributs

Les attributs suivants sont définis pour cet événement.



| Attribut                                                                                               | Description                                                                               |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**TOPOLOGIE de la \_ source d’événements MF \_ \_ \_ annulée**](mf-event-source-topology-canceled-attribute.md)<br/> | Spécifie si la source de Sequencer a annulé cette présentation.<br/> <br/> |



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

 

 




