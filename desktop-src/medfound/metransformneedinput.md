---
description: Envoyé par une transformation de Media Foundation asynchrone (MFT) pour demander un nouvel exemple d’entrée.
ms.assetid: 5d5c50d9-fe4e-47ff-ae09-980911ebfb22
title: Événement METransformNeedInput (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cc15bdffebfd22b4aecac2818da85e39379f681aec0e12fe92f895824edb78f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013499"
---
# <a name="metransformneedinput-event"></a>Événement METransformNeedInput

Envoyé par une transformation de Media Foundation asynchrone (MFT) pour demander un nouvel exemple d’entrée.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description               |
|----------------------|---------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> |



## <a name="attributes"></a>Attributs

Les attributs suivants sont définis pour cet événement.



| Attribut                                                                        | Description                                                                           |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [\_ID de \_ \_ flux d’entrée MFT \_ \_ de l’événement MF](mf-event-mft-input-stream-id.md)<br/> | Identificateur du flux qui a besoin de données d’entrée.<br/>*Souhaitée*<br/> |



## <a name="remarks"></a>Remarques

Les MFTs asynchrones envoient cet événement par le biais de l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Les MFTs synchrones n’envoient jamais cet événement.

Lorsque le client de la MFT reçoit cet événement, il doit appeler [**IMFTransform ::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) pour fournir l’exemple suivant. L’attribut d' [ \_ \_ \_ \_ \_ ID de flux d’entrée MFT de l’événement MF](mf-event-mft-input-stream-id.md) de l’objet d’événement spécifie le flux d’entrée qui requiert des données.

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

 

 




