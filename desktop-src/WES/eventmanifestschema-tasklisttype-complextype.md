---
title: Type complexe TaskListType
description: Définit une liste de tâches utilisées pour identifier les composants d’une application.
ms.assetid: 41a46967-7c5b-4555-9f65-bd9582c0c492
keywords:
- TaskListType type complexe EventLog
topic_type:
- apiref
api_name:
- TaskListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ad427743242ada8901e904fc4e03620ccc72f405
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383807"
---
# <a name="tasklisttype-complex-type"></a>Type complexe TaskListType

Définit une liste de tâches utilisées pour identifier les composants d’une application.

``` syntax
<xs:complexType name="TaskListType">
    <xs:sequence>
        <xs:element name="task"
            type="TaskType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                       | Type                                                         | Description                                                       |
|---------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [**tâche**](eventmanifestschema-task-tasklisttype-element.md) | [**TaskType**](eventmanifestschema-tasktype-complextype.md) | Définit un composant ou un sous-composant d’une application.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





