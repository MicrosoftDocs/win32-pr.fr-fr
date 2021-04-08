---
description: 'Déclenché par la session multimédia lorsque la vitesse de lecture change. Cet événement est envoyé une fois que la méthode IMFRateControl :: sesente se termine de façon asynchrone.'
ms.assetid: 6bef923f-4083-46e1-9a2e-49a6825467ec
title: Événement MESessionRateChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4cbbd8254dfb988c94cf2016164726d578d8906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863613"
---
# <a name="mesessionratechanged-event"></a>Événement MESessionRateChanged

Déclenché par la session multimédia lorsque la vitesse de lecture change. Cet événement est envoyé une fois que la méthode [**IMFRateControl ::**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) sesente se termine de façon asynchrone.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE           | Description                                                                                     |
|-------------------|-------------------------------------------------------------------------------------------------|
| VT \_ R4<br/> | Nouvelle vitesse de lecture, exprimée sous forme de rapport de la vitesse de lecture normale.<br/> <br/> |



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

 

 




