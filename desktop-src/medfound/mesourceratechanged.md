---
description: 'Déclenché par une source de média lorsque la vitesse de lecture change. Cet événement est envoyé une fois que la méthode IMFRateControl :: sesente se termine de façon asynchrone.'
ms.assetid: 68a7fe64-e28a-4c20-830c-9402e1fb57f8
title: Événement MESourceRateChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2af1ca671e09fc8a236ba79b36c1610635989ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113694"
---
# <a name="mesourceratechanged-event"></a>Événement MESourceRateChanged

Déclenché par une source de média lorsque la vitesse de lecture change. Cet événement est envoyé une fois que la méthode [**IMFRateControl ::**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) sesente se termine de façon asynchrone.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE           | Description                                   |
|-------------------|-----------------------------------------------|
| VT \_ R4<br/> | Nouveau taux de lecture.<br/> <br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                     |
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

 

 




