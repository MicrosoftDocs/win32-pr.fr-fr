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
ms.openlocfilehash: aeb2c0e1b3ac3e29502e7d998305674aaa283371be6a22324dde6d84c4330326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611241"
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
| [**Organismes**](taskschedulerschema-body-showmessagetype-element.md)   | nonEmptyString | Spécifie le texte à afficher dans le corps de la boîte de message. <br/> |
| [**Titre**](taskschedulerschema-title-showmessagetype-element.md) | nonEmptyString | Spécifie le titre de la boîte de message. <br/>                       |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





