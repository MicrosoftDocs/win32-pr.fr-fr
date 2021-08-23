---
description: Envoyé par le pipeline à l’encodeur MFTs en série avec des exemples de supports via IMFTransform ::P rocessEvent.
ms.assetid: D5D4544B-CD8D-4C94-B050-7BA1944800CC
title: Événement MEEncodingParameters (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2230640adf1f92111569a39558f2959271a23ea2b5dbe5d0d915b6a2b989d371
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723829"
---
# <a name="meencodingparameters-event"></a>Événement MEEncodingParameters

Envoyé par le pipeline à l’encodeur MFTs en série avec des exemples de supports via [**IMFTransform ::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="attributes"></a>Attributs

Les attributs suivants sont définis pour cet événement.



| Attribut                                         | Description                                                                                                                    |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)<br/> | Contient les nouveaux paramètres basés sur un ICodecAPI que l’encodeur doit appliquer aux exemples entrants suivants.<br/> <br/> |



## <a name="remarks"></a>Remarques

La charge utile d’événement est un magasin d’attributs (pointeur IMFAttributes) qui contient les nouveaux paramètres basés sur ICodecAPI///que l’encodeur doit appliquer aux exemples entrants suivants.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




