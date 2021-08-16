---
title: Type complexe StringTableType
description: Définit une liste de chaînes localisées que vous pouvez référencer dans votre manifeste. | Type complexe StringTableType
ms.assetid: 47a59ff7-aaf6-4200-805b-0a8b5f57f101
keywords:
- StringTableType type complexe EventLog
topic_type:
- apiref
api_name:
- StringTableType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5d52f19ca01a926c82fcc1e13cc7191866722ba5e0e6eef81e916e244744783
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342983"
---
# <a name="stringtabletype-complex-type"></a>Type complexe StringTableType

Définit une liste de chaînes localisées que vous pouvez référencer dans votre manifeste.

``` syntax
<xs:complexType name="StringTableType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="string">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="id"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="value"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="stringType"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
    </xs:choice>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                              | Type | Description                            |
|----------------------------------------------------------------------|------|----------------------------------------|
| [**chaîne**](eventmanifestschema-string-stringtabletype-element.md) |      | Définit une chaîne localisée.<br/> |



## <a name="attributes"></a>Attributs



| Nom       | Type   | Description                                                                                                              |
|------------|--------|--------------------------------------------------------------------------------------------------------------------------|
| id         | string | Identificateur qui identifie de façon unique la chaîne dans la table de chaînes. Par exemple, « Printer. Connection ».<br/> |
| stringType | string | Non utilisé.<br/>                                                                                                     |
| value      | string | La chaîne localisée.<br/>                                                                                         |



## <a name="remarks"></a>Remarques

Vous pouvez référencer les chaînes à partir de n’importe quel type de manifeste contenant l’attribut de message. Pour faire référence à une chaîne avec un stringType « String » et un ID « Printer. Connection », utilisez $ (String. Printer. Connection) comme valeur de l’attribut de message.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





