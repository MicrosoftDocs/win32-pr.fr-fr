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
ms.openlocfilehash: a9964c51524f7401afdfdd8a2da10cf43326bcae
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522540"
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



## <a name="remarks"></a>Notes

Vous pouvez référencer les chaînes à partir de n’importe quel type de manifeste contenant l’attribut de message. Pour faire référence à une chaîne avec un stringType « String » et un ID « Printer. Connection », utilisez $ (String. Printer. Connection) comme valeur de l’attribut de message.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





