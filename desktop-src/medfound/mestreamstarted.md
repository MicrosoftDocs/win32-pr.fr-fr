---
description: Déclenché par un flux de média lorsque la source démarre sans recherche. Un flux de média déclenche cet événement lorsque la source du média déclenche l’événement MESourceStarted.
ms.assetid: 6652e440-5de9-4767-b7a6-9d919ceece38
title: Événement MEStreamStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a385516a6f0f973dd5bd0453d6c9751a0f7411a8ea43cb6acb936d8601c5272
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113939"
---
# <a name="mestreamstarted-event"></a>Événement MEStreamStarted

Déclenché par un flux de média lorsque la source démarre sans recherche. Un flux de média déclenche cet événement lorsque la source du média déclenche l’événement [MESourceStarted](mesourcestarted.md) .

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/>                                                                          |
| Le \_ i8 VT<br/>    | Heure de début, en unités de 100 nanosecondes, par rapport aux horodatages sur les échantillons.<br/> <br/> |



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

 

 




