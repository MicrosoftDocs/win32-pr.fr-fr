---
title: Type complexe comHandlerType
description: Définit les éléments enfants et les informations de séquencement pour l’élément comgérer.
ms.assetid: 688e79f3-8b7e-4892-8119-b0a457ce9c7f
keywords:
- Planificateur de tâches de type complexe comHandlerType
topic_type:
- apiref
api_name:
- comHandlerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d36a92651fc46c0a1950ecff00fa59fe56e1d758
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011050"
---
# <a name="comhandlertype-complex-type"></a>Type complexe comHandlerType

Définit les éléments enfants et les informations de séquencement pour l’élément [**comgérer**](taskschedulerschema-comhandler-actiongroup-element.md) .

``` syntax
<xs:complexType name="comHandlerType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="ClassId"
                    type="guidType"
                 />
                <xs:element name="Data"
                    type="dataType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                               | Type                                                         | Description                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------|
| [**ClassId**](taskschedulerschema-classid-comhandlertype-element.md) | [**guidType**](taskschedulerschema-guidtype-simpletype.md)  | Spécifie l’identificateur de la classe de gestionnaire.<br/>          |
| [**Données**](taskschedulerschema-data-comhandlertype-element.md)       | [**dataType**](taskschedulerschema-datatype-complextype.md) | Spécifie des données supplémentaires associées au gestionnaire. <br/> |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types complexes de schéma Planificateur de tâches](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





