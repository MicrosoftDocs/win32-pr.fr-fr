---
description: 'Déclenché par la session multimédia lorsque la méthode IMFMediaSession :: ClearTopologies se termine de façon asynchrone.'
ms.assetid: 2017d13b-8dc2-48f9-a21e-7b826e174edf
title: Événement MESessionTopologiesCleared (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee6b9107f6584de3f9621aeaecc95ffb6bf7bbb8741e59d5e32d3efe33d5ae6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119357119"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




