---
description: 'Déclenché par la session multimédia lorsque la méthode IMFMediaSession :: ClearTopologies se termine de façon asynchrone.'
ms.assetid: 2017d13b-8dc2-48f9-a21e-7b826e174edf
title: Événement MESessionTopologiesCleared (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 551e98607a8d23d9333527337bbd7d038ed0b340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114618"
---
# <a name="mesessiontopologiescleared-event"></a>Événement MESessionTopologiesCleared

Déclenché par la session multimédia lorsque la méthode [**IMFMediaSession :: ClearTopologies**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-cleartopologies) se termine de façon asynchrone.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



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

 

 




