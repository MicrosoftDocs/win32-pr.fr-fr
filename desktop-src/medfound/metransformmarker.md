---
description: Envoyé par une transformation de Media Foundation asynchrone (MFT) en réponse à un \_ message de marque de commande de message MFT \_ \_ .
ms.assetid: d0c0d62d-9133-4d4b-8606-c2ae1d4c9f0a
title: Événement METransformMarker (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7029119b30314e56531c0afb29accadb67e1efb343a906c2558af2157c0b1f82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827039"
---
# <a name="metransformmarker-event"></a>Événement METransformMarker

Envoyé par une transformation de Media Foundation asynchrone (MFT) en réponse à un message de **\_ marque de \_ commande \_ de message MFT** .

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description               |
|----------------------|---------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> |



## <a name="attributes"></a>Attributs

Les attributs suivants sont définis pour cet événement.



| Attribut                                                      | Description                                                                                                                |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [\_ \_ contexte MFT de l’événement MF \_](mf-event-mft-context.md)<br/> | Valeur du paramètre *ulParam* du message de **\_ \_ \_ marqueur de commande du message MFT** .<br/>*Souhaitée*<br/> |



## <a name="remarks"></a>Remarques

Les MFTs asynchrones envoient cet événement par le biais de l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Les MFTs synchrones n’envoient jamais cet événement.

Le client d’une table MFT asynchrone peut placer un marqueur dans le flux en appelant [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) avec le message de **\_ \_ \_ marqueur de commande de message MFT** . Le paramètre *ulParam* contient des données définies par l’application.

Lorsque la table MFT termine le traitement de toutes les données d’entrée qui étaient disponibles au moment de l’appel de [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) , la MFT met en file d’attente un événement METransformMarker. L’attribut de [ \_ \_ \_ contexte MFT](mf-event-mft-context.md) de l’événement MF de l’événement contient la valeur du paramètre *ulParam* . Pour plus d’informations, consultez [MFTS asynchrone](asynchronous-mfts.md).

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

 

 




