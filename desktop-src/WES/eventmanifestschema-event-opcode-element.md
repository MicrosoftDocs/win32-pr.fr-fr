---
title: Élément d’événement (OpCode)
description: Définit un événement pour un opcode spécifique à une tâche.
ms.assetid: 7ca8fff2-ef1a-45c4-b082-e4745330bf0b
keywords:
- Event, élément EventLog
topic_type:
- apiref
api_name:
- event
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 987bf0b8b84e574a83211e90dffcd1f636920b1ced0c34b9d1d239515d16cdd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055997"
---
# <a name="event-opcode-element"></a>Élément d’événement (OpCode)

\[à partir du compilateur de messages fourni avec la version Windows 7 du SDK Windows, cet élément n’est plus disponible.\]

Définit un événement pour un opcode spécifique à une tâche.

``` syntax
<xs:element name="event"
    type="EventDefinitionType"
 />
```

L’élément **Event** est défini par l’élément [**opcode**](eventmanifestschema-opcode-taskeventdefinitiontype-element.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**opcode (TaskEventDefinitionType)**](eventmanifestschema-opcode-taskeventdefinitiontype-element.md)
</dt> </dl>

 

 





