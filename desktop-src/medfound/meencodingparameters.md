---
description: Envoyé par le pipeline à l’encodeur MFTs en série avec des exemples de supports via IMFTransform ::P rocessEvent.
ms.assetid: D5D4544B-CD8D-4C94-B050-7BA1944800CC
title: Événement MEEncodingParameters (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e193044b25eb1d333182a2593fcf2248fba2366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202008"
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



## <a name="remarks"></a>Notes

La charge utile d’événement est un magasin d’attributs (pointeur IMFAttributes) qui contient les nouveaux paramètres basés sur ICodecAPI///que l’encodeur doit appliquer aux exemples entrants suivants.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




