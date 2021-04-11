---
description: 'Déclenché par un flux de média après un appel à IMFMediaSource :: START provoque une recherche dans le flux. Un flux de média déclenche cet événement lorsque la source du média déclenche l’événement MESourceSeeked.'
ms.assetid: df06df16-711d-4262-b049-fb29f25934de
title: Événement MEStreamSeeked (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7b66e2176b08c04b01fc487aac4b8218536b615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201997"
---
# <a name="mestreamseeked-event"></a>Événement MEStreamSeeked

Déclenché par un flux de média après un appel à [**IMFMediaSource :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) provoque une recherche dans le flux. Un flux de média déclenche cet événement lorsque la source du média déclenche l’événement [MESourceSeeked](mesourceseeked.md) .

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE           | Description                                                        |
|-------------------|--------------------------------------------------------------------|
| Le \_ i8 VT<br/> | Nouvelle heure de début, en unités de 100 nanosecondes.<br/> <br/> |



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

 

 




