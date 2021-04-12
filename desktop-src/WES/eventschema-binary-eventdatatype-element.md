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
ms.openlocfilehash: cdfd00e2d25f3178ab44081f76725b3189f1010b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032370"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**EventData (EventType)**](eventschema-eventdata-eventtype-element.md)
</dt> </dl>

 

