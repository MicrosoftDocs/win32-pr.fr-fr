---
description: Déclenché par la session multimédia lorsque l’état d’une topologie change.
ms.assetid: b45fd598-ab1e-4b12-8d82-c88c96d1f770
title: Événement MESessionTopologyStatus (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11948e27997037c1e875e192fd712a2f8a132b44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951549"
---
# <a name="mesessiontopologystatus-event"></a>Événement MESessionTopologyStatus

Déclenché par la session multimédia lorsque l’état d’une topologie change.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE                | Description                                                                                         |
|------------------------|-----------------------------------------------------------------------------------------------------|
| VT \_ inconnu<br/> | Pointeur vers l’interface [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) de la topologie.<br/> <br/> |



## <a name="attributes"></a>Attributs

Les attributs suivants sont définis pour cet événement.



| Attribut                                                                            | Description                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**État de la \_ topologie des événements MF \_ \_**](mf-event-topology-status-attribute.md)<br/> | Spécifie le nouvel état de la topologie.<br/> <br/> |



## <a name="remarks"></a>Notes

Pour obtenir un exemple de code qui récupère le pointeur [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) à partir de l’événement, consultez événement [MESessionTopologySet](mesessiontopologyset.md) .

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

 

 




