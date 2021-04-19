---
title: Type complexe DefinitionType
description: Définit une liste d’événements que votre fournisseur peut journaliser.
ms.assetid: 6d401ced-be1a-409a-8f4d-2d977a33ff8d
keywords:
- DefinitionType type complexe EventLog
topic_type:
- apiref
api_name:
- DefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 82fbf7ec7db6f64f1bac9776376fa8fe89659d9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510319"
---
# <a name="definitiontype-complex-type"></a>Type complexe DefinitionType

Définit une liste d’événements que votre fournisseur peut journaliser.

``` syntax
<xs:complexType name="DefinitionType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="event"
            type="EventDefinitionType"
         />
        <xs:element name="task"
            type="TaskEventDefinitionType"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                           | Type                                                                                       | Description                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**événement**](eventmanifestschema-event-definitiontype-element.md) | [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md)         | Définit un événement que votre fournisseur peut journaliser.<br/>                                                                                                                                                                                                                                 |
| [**tâche**](eventmanifestschema-task-definitiontype-element.md)   | [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) | Non pris en charge.<br/> **Windows Server 2008 et Windows Vista :** Définit un événement spécifique à la tâche que votre fournisseur peut journaliser. (À partir du compilateur de messages fourni avec la version Windows 7 du SDK Windows, les événements spécifiques aux tâches ne sont plus pris en charge.)<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





