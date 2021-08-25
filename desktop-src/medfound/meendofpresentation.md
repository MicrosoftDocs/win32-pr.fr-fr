---
description: Déclenché par une source de média lorsqu’une présentation se termine. Cet événement signale que tous les flux de la présentation sont terminés. La session multimédia transmet cet événement à l’application.
ms.assetid: 259b00ae-a91b-461b-a12f-f7291ecc04ff
title: Événement MEEndOfPresentation (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e97a2689b8d0e2ae156daa84f27f0e10fb31b828ffedf027a7be47a6c330b7b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941458"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




