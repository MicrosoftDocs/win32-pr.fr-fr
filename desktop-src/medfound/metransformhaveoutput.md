---
description: Envoyé par une transformation de Media Foundation asynchrone (MFT) quand de nouvelles données de sortie sont disponibles à partir de la table MFT.
ms.assetid: a9403ad3-81bf-4cd7-ba7f-816b901bb02c
title: Événement METransformHaveOutput (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de6ee70f21c0edcf65a8090feaf90d310839749e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517543"
---
# <a name="metransformhaveoutput-event"></a>Événement METransformHaveOutput

Envoyé par une transformation de Media Foundation asynchrone (MFT) quand de nouvelles données de sortie sont disponibles à partir de la table MFT.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description               |
|----------------------|---------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> |



## <a name="attributes"></a>Attributs

Aucun attribut n’est défini pour cet événement.

## <a name="remarks"></a>Notes

Les MFTs asynchrones envoient cet événement par le biais de l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Les MFTs synchrones n’envoient jamais cet événement.

Lorsque le client de la MFT reçoit cet événement, il doit appeler [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) pour récupérer la sortie.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> <dt>

[MFTs asynchrone](asynchronous-mfts.md)
</dt> </dl>

 

 




