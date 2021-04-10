---
title: Type complexe TemplateListType
description: Définit une liste de modèles qui spécifient les données à inclure avec les événements. | Type complexe TemplateListType
ms.assetid: 7f676746-6773-4ae2-8330-60d432c29e3a
keywords:
- TemplateListType type complexe EventLog
topic_type:
- apiref
api_name:
- TemplateListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a60b31fd88d05f00229f27a616a29483a29bd49d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761779"
---
# <a name="templatelisttype-complex-type"></a>Type complexe TemplateListType

Définit une liste de modèles qui spécifient les données à inclure avec les événements.

``` syntax
<xs:complexType name="TemplateListType">
    <xs:sequence>
        <xs:element name="template"
            type="TemplateItemType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                   | Type                                                                         | Description                                                           |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**modèle**](eventmanifestschema-template-templatelisttype-element.md) | [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) | Modèle qui définit les données à inclure avec un événement.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





