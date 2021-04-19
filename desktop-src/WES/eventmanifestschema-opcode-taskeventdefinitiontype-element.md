---
title: Élément opcode (TaskEventDefinitionType)
description: Contient un opcode spécifique à une tâche pour un événement. Toutes les définitions opcode sont supposées être spécifiques à la tâche pour la tâche qui contient les définitions d’événement.
ms.assetid: c7192772-401b-4602-918d-0e0bc4b65ca7
keywords:
- OpCode, élément EventLog
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d9f3b58353163e1ee5b9abeb04007a4a9d449e5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518118"
---
# <a name="opcode-taskeventdefinitiontype-element"></a>Élément opcode (TaskEventDefinitionType)

\[À partir du compilateur de messages fourni avec la version Windows 7 du SDK Windows, cet élément n’est plus disponible.\]

Contient un opcode spécifique à une tâche pour un événement. Toutes les définitions opcode sont supposées être spécifiques à la tâche pour la tâche qui contient les définitions d’événement.

``` syntax
<xs:element name="opcode">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="event"
                type="EventDefinitionType"
                maxOccurs="unbounded"
             />
        </xs:sequence>
        <xs:attribute name="name"
            type="QName"
            use="required"
         />
    </xs:complexType>
</xs:element>
```

L’élément **opcode** est défini par le type complexe [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) .

## <a name="child-elements"></a>Éléments enfants



| Élément                                                   | Type                                                                               | Description                                        |
|-----------------------------------------------------------|------------------------------------------------------------------------------------|----------------------------------------------------|
| [**événement**](eventmanifestschema-event-opcode-element.md) | [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md) | Événement qui est publié avec une tâche.<br/> |



## <a name="attributes"></a>Attributs



| Nom | Type      | Description                                      |
|------|-----------|--------------------------------------------------|
| name | **QName** | Nom de l’opcode spécifique à la tâche.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**tâche (DefinitionType)**](eventmanifestschema-task-definitiontype-element.md)
</dt> </dl>

 

 





