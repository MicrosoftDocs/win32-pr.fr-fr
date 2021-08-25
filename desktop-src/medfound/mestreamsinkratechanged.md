---
description: Déclenché par un récepteur de flux lorsque le taux a changé.
ms.assetid: c61c71de-fd3c-429b-a29f-f9d2bbfcb531
title: Événement MEStreamSinkRateChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43a3a4cbff4464f78e71d3047e2b9ccaddfcbf38adcb5e84bab8f5ae49c5d80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827139"
---
# <a name="mestreamsinkratechanged-event"></a>Événement MEStreamSinkRateChanged

Déclenché par un récepteur de flux lorsque le taux a changé.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="remarks"></a>Remarques

Si un récepteur de flux prend en charge les changements de taux, il envoie cet événement une fois que la modification du taux est terminée. L’événement est envoyé une fois pour chaque appel à la méthode [**IMFClockStateSink :: OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) du récepteur. Si la modification du taux échoue, la valeur de l’état de l’événement est un code d’erreur.

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

 

 




