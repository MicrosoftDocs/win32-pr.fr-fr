---
title: Type complexe DataType (Journal des événements Windows)
description: Définit un élément de données.
ms.assetid: f3b7de63-1ac1-429d-9e36-1f13c26c9618
keywords:
- Type de données type complexe EventLog
topic_type:
- apiref
api_name:
- DataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d3ac6e545cbe8567bbe041568c442f762743ad0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317398"
---
# <a name="datatype-complex-type"></a>Type complexe DataType

Définit un élément de données.

``` syntax
<xs:complexType name="DataType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="Name"
                type="string"
                use="optional"
             />
            <xs:attribute name="Type"
                type="QName"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributs



| Nom | Type   | Description                                                                                                                                                              |
|------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nom | string | Nom d’un élément de données qui a été défini dans le modèle (consultez le type complexe [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) ).<br/> |
| Type | QName  | Non utilisé.<br/>                                                                                                                                                     |



## <a name="remarks"></a>Notes

L’élément de données peut être un élément de données de niveau supérieur ou un élément de données dans une structure.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





