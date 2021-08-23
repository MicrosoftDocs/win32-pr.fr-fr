---
description: Déclenché par un récepteur de flux lorsqu’il termine la transition à l’état arrêté. La transition à Stopped se produit lorsque la méthode Stop IMFPresentationClock est appelée sur l’horloge de présentation des récepteurs.
ms.assetid: 1a8c7faa-4d4a-4458-ad08-a760a15dc347
title: Événement MEStreamSinkStopped (Mfobjects. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7bf6a39dca8f50fed8fdd1d0137405225624999fab42771e485174ba4f0afa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715099"
---
# <a name="mestreamsinkstopped-event"></a>Événement MEStreamSinkStopped

Déclenché par un récepteur de flux lorsqu’il termine la transition à l’état arrêté. La transition à Stopped se produit lorsque la méthode [**IMFPresentationClock :: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop) est appelée sur l’horloge de présentation du récepteur.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



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
</dt> </dl>

 

 




