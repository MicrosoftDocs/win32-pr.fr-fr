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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512783"
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



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**ProcessingErrorData (EventType)**](eventschema-processingerrordata-eventtype-element.md)
</dt> </dl>

 

 





