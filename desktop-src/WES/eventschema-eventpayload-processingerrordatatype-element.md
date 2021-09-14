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
ms.openlocfilehash: 4dd20f95924282ae8cb0f1b0604c0e77d07766ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324326"
---
# <a name="eventpayload-processingerrordatatype-element"></a>Élément EventPayload (ProcessingErrorDataType)

Contient des données d’événement binaires pour l’événement qui a provoqué une erreur lors du traitement des données d’événement.

``` syntax
<xs:element name="EventPayload"
    type="hexBinary"
 />
```

L’élément **EventPayload** est défini par le type complexe [**ProcessingErrorDataType**](eventschema-processingerrordatatype-complextype.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**ProcessingErrorData (EventType)**](eventschema-processingerrordata-eventtype-element.md)
</dt> </dl>

 

 





