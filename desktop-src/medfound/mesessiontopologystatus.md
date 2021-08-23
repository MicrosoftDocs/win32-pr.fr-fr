---
description: Déclenché par la session multimédia lorsque l’état d’une topologie change.
ms.assetid: b45fd598-ab1e-4b12-8d82-c88c96d1f770
title: Événement MESessionTopologyStatus (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42adfd1a86319f65077e87925eb23807253f12b06e977ee1eb9e494a4c7df180
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723719"
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



## <a name="remarks"></a>Remarques

Pour obtenir un exemple de code qui récupère le pointeur [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) à partir de l’événement, consultez événement [MESessionTopologySet](mesessiontopologyset.md) .

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

 

 




