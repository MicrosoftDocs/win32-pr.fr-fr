---
description: Signale qu’une source de média a cessé de mettre en mémoire tampon des données.
ms.assetid: 11b1290d-d462-4aa0-a358-b3f6447c99d8
title: Événement MEBufferingStopped (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e953ae5d7a79c04c33f4d0b4f9c87faa1e5798ed95d2d3bae29dbd0fab8b12a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878080"
---
# <a name="mebufferingstopped-event"></a>Événement MEBufferingStopped

Signale qu’une source de média a cessé de mettre en mémoire tampon des données.

Une source de média l’envoie lorsqu’elle arrête la mise en mémoire tampon des données après l’envoi de l’événement [MEBufferingStarted](mebufferingstarted.md) .

Les flux d’octets qui implémentent l’interface [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) envoient également cet événement.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="remarks"></a>Remarques

Lorsque la session multimédia reçoit cet événement, elle redémarre l’horloge de la présentation. La session multimédia transmet également l’événement à l’application.

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

 

 




