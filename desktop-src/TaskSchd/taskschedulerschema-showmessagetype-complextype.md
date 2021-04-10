---
title: Type complexe showMessageType
description: Définit les éléments qui représentent une action qui affiche une boîte de message.
ms.assetid: eb841d9f-0be2-433b-9002-5e41c6ee78f9
keywords:
- Planificateur de tâches de type complexe showMessageType
topic_type:
- apiref
api_name:
- showMessageType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d65ed893bce63c95fffcf237d3a3a95ebb1550d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942420"
---
# <a name="showmessagetype-complex-type"></a>Type complexe showMessageType

Définit les éléments qui représentent une action qui affiche une boîte de message.

``` syntax
<xs:complexType name="showMessageType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Title"
                    type="nonEmptyString"
                 />
                <xs:element name="Body"
                    type="nonEmptyString"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                            | Type           | Description                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [**Corps**](taskschedulerschema-body-showmessagetype-element.md)   | nonEmptyString | Spécifie le texte à afficher dans le corps de la boîte de message. <br/> |
| [**Intitulé**](taskschedulerschema-title-showmessagetype-element.md) | nonEmptyString | Spécifie le titre de la boîte de message. <br/>                       |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





