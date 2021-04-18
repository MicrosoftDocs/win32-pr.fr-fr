---
description: Nouveauté de Windows 7. Élément conteneur pour les éléments relatedProperty.
ms.assetid: F8BAAE5C-A7EA-487a-B829-91A27E24B58D
title: relatedPropertyInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 442de657bed7e97f74064c39cc0934c65a6f520d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520483"
---
# <a name="relatedpropertyinfo"></a>relatedPropertyInfo

Nouveauté de Windows 7. Élément conteneur pour les éléments [relatedProperty](./propdesc-schema-relatedproperty.md) . Il ne doit y avoir qu’un seul élément [relatedPropertyInfo]() pour chaque élément [PropertyDescription](./propdesc-schema-propertydescription.md) .

## <a name="syntax"></a>Syntaxe


```
<!-- relatedPropertyInfo -->
<xs:element name="relatedPropertyInfo">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="relatedProperty" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="relationshipName" type="canonical-name" use="required"/>
                    <xs:attribute name="propertyName" type="canonical-name" use="required"/>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>

    <xs:unique name="No_two_relatedProperties_can_have_the_same_relationship_name">
        <xs:selector xpath="s:relatedProperty"/>
        <xs:field    xpath="@relationshipName"/>
    </xs:unique>
</xs:element>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                                   | Éléments enfants                                           |
|------------------------------------------------------------------|----------------------------------------------------------|
| [propertyDescription](./propdesc-schema-propertydescription.md) | [relatedProperty](./propdesc-schema-relatedproperty.md) |



 

## <a name="attributes"></a>Attributs

Cet élément n’a pas d’attributs.

 

 
