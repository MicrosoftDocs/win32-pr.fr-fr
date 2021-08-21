---
title: Type complexe TaskEventDefinitionType
description: Définit un événement spécifique à la tâche que votre fournisseur peut journaliser. | Type complexe TaskEventDefinitionType
ms.assetid: f0329728-e7b5-4161-a30f-78b81a7b6812
keywords:
- TaskEventDefinitionType type complexe EventLog
topic_type:
- apiref
api_name:
- TaskEventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44a4fc7ca8784b3472fea3b0d4f4e657ce615fae05a8cc7372aa3cca0fedb431
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055837"
---
# <a name="taskeventdefinitiontype-complex-type"></a>Type complexe TaskEventDefinitionType

\[à partir du compilateur de messages fourni avec la version Windows 7 du SDK Windows, le type complexe TaskEventDefinitionType n’est plus disponible. Utilisez plutôt des OpCodes spécifiques à la tâche pour fournir les mêmes fonctionnalités.\]

Définit un événement spécifique à la tâche que votre fournisseur peut journaliser.

``` syntax
<xs:complexType name="TaskEventDefinitionType">
    <xs:sequence>
        <xs:element name="opcode"
            maxOccurs="unbounded"
        >
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
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                      | Type                                                                               | Description                                             |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------|
| **event**                                                                    | [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md) | Événement spécifique à une tâche publié à l’aide d’une tâche.<br/> |
| [**opcode**](eventmanifestschema-opcode-taskeventdefinitiontype-element.md) |                                                                                    | Opcode spécifique à une tâche qui est utilisé pour un événement. <br/>   |



## <a name="attributes"></a>Attributs



| Nom | Type      | Description                                      |
|------|-----------|--------------------------------------------------|
| name | **QName** | Nom de l’opcode spécifique à la tâche.<br/> |
| name | anyURI    | Nom de la tâche.<br/>                 |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





