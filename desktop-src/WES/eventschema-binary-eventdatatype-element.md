---
title: Élément Binary (EventDataType)
description: Objet blob de données binaires pour les événements écrits à l’aide de la journalisation des événements.
ms.assetid: aec2557f-6d63-48e7-b4d7-584e99dfcce3
keywords:
- Élément binaire EventLog
topic_type:
- apiref
api_name:
- Binary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 495310a46a314b944b29eeb2433b7c5581136c6923c5630d8f09486a95e47fdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120397"
---
# <a name="binary-eventdatatype-element"></a>Élément Binary (EventDataType)

Objet blob de données binaires pour les événements écrits à l’aide de la [journalisation des événements](/windows/desktop/EventLog/event-logging).

``` syntax
<xs:element name="Binary"
    type="hexBinary"
 />
```

L’élément **binaire** est défini par le type complexe [**EventDataType**](eventschema-eventdatatype-complextype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**EventData (EventType)**](eventschema-eventdata-eventtype-element.md)
</dt> </dl>

 

