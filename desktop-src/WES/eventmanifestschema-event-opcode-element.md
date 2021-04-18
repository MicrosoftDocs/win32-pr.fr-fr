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
ms.openlocfilehash: 25f7a7f3a92c07895529d6dad59df22a7389735d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512612"
---
# <a name="event-opcode-element"></a>Élément d’événement (OpCode)

\[À partir du compilateur de messages fourni avec la version Windows 7 du SDK Windows, cet élément n’est plus disponible.\]

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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**opcode (TaskEventDefinitionType)**](eventmanifestschema-opcode-taskeventdefinitiontype-element.md)
</dt> </dl>

 

 





