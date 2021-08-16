---
description: Envoyé par une transformation de Media Foundation asynchrone (MFT) lorsqu’une opération de drainage est terminée.
ms.assetid: 923055e5-a09a-402e-983b-6fa3cebb1b3a
title: Événement METransformDrainComplete (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd5ab03ac5027d1dc7549e7b7f0b8494cd8066b07afb64c5df17415a4986866e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974028"
---
# <a name="metransformdraincomplete-event"></a>Événement METransformDrainComplete

Envoyé par une transformation de Media Foundation asynchrone (MFT) lorsqu’une opération de drainage est terminée.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description               |
|----------------------|---------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> |



## <a name="attributes"></a>Attributs

Les attributs suivants sont définis pour cet événement.



| Attribut                                                                        | Description                                                                      |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [\_ID de \_ \_ flux d’entrée MFT \_ \_ de l’événement MF](mf-event-mft-input-stream-id.md)<br/> | Identificateur du flux qui a été vidé.<br/>*Souhaitée*<br/> |



## <a name="remarks"></a>Remarques

Les MFTs asynchrones envoient cet événement par le biais de l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Les MFTs synchrones n’envoient jamais cet événement.

Pour vider une table MFT, appelez [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) avec le message de **drainage de \_ \_ commande \_ de message MFT** . Spécifiez le flux d’entrée à purger dans le paramètre *ulParam* . Lorsque l’opération de drainage est terminée, une table MFT asynchrone envoie l’événement METransformDrainComplete. L’attribut d' [ \_ \_ \_ \_ \_ ID de flux d’entrée MFT d’événement MF](mf-event-mft-input-stream-id.md) de l’événement contient l’identificateur de flux fourni dans le paramètre *ulParam* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> <dt>

[MFTs asynchrone](asynchronous-mfts.md)
</dt> </dl>

 

 




