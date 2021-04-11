---
description: 'Déclenché par une source de média pour demander un nouveau taux de lecture. L’application doit appeler IMFRateControl :: SEDE la vitesse demandée. Une source de média peut déclencher cet événement si elle ne peut pas continuer la lecture à la vitesse actuelle.'
ms.assetid: 705e5a79-836b-417b-a7ed-c733572f6905
title: Événement MESourceRateChangeRequested (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9973a509541f3ec3d4f6a235b8f1277a20f7ed1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201999"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




