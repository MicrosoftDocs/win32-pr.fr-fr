---
description: Déclenché par un récepteur de flux lorsque le flux a reçu suffisamment de données de pré-roll pour commencer le rendu. Cet événement est déclenché par les récepteurs multimédias qui prennent en charge l’interface IMFMediaSinkPreroll.
ms.assetid: 1ecb1805-73ce-4741-b969-6eb88982ee26
title: Événement MEStreamSinkPrerolled (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d46c4c4e076651cb38318bb908df280c503c0880a256087f4192433ecdb5406a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464799"
---
# <a name="mestreamsinkprerolled-event"></a>Événement MEStreamSinkPrerolled

Déclenché par un récepteur de flux lorsque le flux a reçu suffisamment de données de pré-roll pour commencer le rendu. Cet événement est déclenché par les récepteurs multimédias qui prennent en charge l’interface [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) .

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

 

 




