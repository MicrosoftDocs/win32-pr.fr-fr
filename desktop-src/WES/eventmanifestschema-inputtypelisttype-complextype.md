---
title: Type complexe InputTypeListType
description: Définit une liste de types d’entrée.
ms.assetid: e6bba894-7c17-411e-92e5-9276728a5e4b
keywords:
- InputTypeListType type complexe EventLog
topic_type:
- apiref
api_name:
- InputTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 156ee19a90cdbb64e742d9876a39741155a3d5172f8da05f38f666cc077fc47c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118343740"
---
# <a name="inputtypelisttype-complex-type"></a>Type complexe InputTypeListType

Définit une liste de types d’entrée.

``` syntax
<xs:complexType name="InputTypeListType">
    <xs:sequence>
        <xs:element name="inType"
            type="InputType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                | Type                                                           | Description                       |
|------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------|
| [**InType**](eventmanifestschema-intype-inputtypelisttype-element.md) | [**InputType**](eventmanifestschema-inputtype-complextype.md) | Définit un type d’entrée.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





