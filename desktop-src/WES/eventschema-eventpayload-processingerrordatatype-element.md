---
title: Élément EventPayload (ProcessingErrorDataType)
description: Contient des données d’événement binaires pour l’événement qui a provoqué une erreur lors du traitement des données d’événement.
ms.assetid: 0ba72d72-8f43-40ca-b3ee-89fe27a4dd07
keywords:
- EventLog, élément EventPayload
topic_type:
- apiref
api_name:
- EventPayload
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 131869f9c54143f32780ff2ad1133b2c9ddf113c990b13be497a554caec30ba0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589012"
---
# <a name="eventpayload-processingerrordatatype-element"></a>Élément EventPayload (ProcessingErrorDataType)

Contient des données d’événement binaires pour l’événement qui a provoqué une erreur lors du traitement des données d’événement.

``` syntax
<xs:element name="EventPayload"
    type="hexBinary"
 />
```

L’élément **EventPayload** est défini par le type complexe [**ProcessingErrorDataType**](eventschema-processingerrordatatype-complextype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Value |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**ProcessingErrorData (EventType)**](eventschema-processingerrordata-eventtype-element.md)
</dt> </dl>

 

 





