---
description: 'Déclenché par une source de média lorsque la vitesse de lecture change. Cet événement est envoyé une fois que la méthode IMFRateControl :: sesente se termine de façon asynchrone.'
ms.assetid: 68a7fe64-e28a-4c20-830c-9402e1fb57f8
title: Événement MESourceRateChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b89e88086d1e836ae3efa676bead25a4fd2cd413ce6b7f287efee7d5cc33439
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061570"
---
# <a name="mesourceratechanged-event"></a>Événement MESourceRateChanged

Déclenché par une source de média lorsque la vitesse de lecture change. Cet événement est envoyé une fois que la méthode [**IMFRateControl ::**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) sesente se termine de façon asynchrone.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE           | Description                                   |
|-------------------|-----------------------------------------------|
| VT \_ R4<br/> | Nouveau taux de lecture.<br/> <br/> |



## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Mise en œuvre du contrôle de taux](implementing-rate-control.md)
</dt> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Contrôle de la fréquence](rate-control.md)
</dt> <dt>

[**IMFRateControl :: setraverse**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)
</dt> </dl>

 

 




