---
description: 'Déclenché par une source de média pour demander un nouveau taux de lecture. L’application doit appeler IMFRateControl :: SEDE la vitesse demandée. Une source de média peut déclencher cet événement si elle ne peut pas continuer la lecture à la vitesse actuelle.'
ms.assetid: 705e5a79-836b-417b-a7ed-c733572f6905
title: Événement MESourceRateChangeRequested (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7d8a88225fd3a0a95c56d549a712b295ba562cc684c08fe4b762c0169e3637c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974128"
---
# <a name="mesourceratechangerequested-event"></a>Événement MESourceRateChangeRequested

Déclenché par une source de média pour demander un nouveau taux de lecture. L’application doit appeler [**IMFRateControl ::**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) SEDE la vitesse demandée. Une source de média peut déclencher cet événement si elle ne peut pas continuer la lecture à la vitesse actuelle.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE           | Description                                             |
|-------------------|---------------------------------------------------------|
| VT \_ R4<br/> | Nouveau taux de lecture demandé.<br/> <br/> |



## <a name="attributes"></a>Attributs

Les attributs suivants sont définis pour cet événement.



| Attribut                                                                    | Description                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**\_événement MF \_ - \_ éclaircir**](mf-event-do-thinning-attribute.md)<br/> | Spécifie si la source du média demande également une éclaircie.<br/> <br/> |



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

 

 




