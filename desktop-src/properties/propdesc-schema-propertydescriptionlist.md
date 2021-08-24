---
description: Conteneur pour un ou plusieurs éléments propertyDescription individuels.
ms.assetid: b54aaa85-6928-470e-9630-44b094205106
title: propertyDescriptionList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f22e5e8e2c90b1a9f9587117f684ebfb89c55ee702749248cb0a886d5ba8266
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119341839"
---
# <a name="propertydescriptionlist"></a>propertyDescriptionList

Conteneur pour un ou plusieurs éléments [PropertyDescription](./propdesc-schema-propertydescription.md) individuels. Un fichier de schéma de description de la propriété. propDesc doit contenir au moins un élément [propertyDescriptionList]() .

## <a name="syntax"></a>Syntaxe


```
<!-- propertyDescriptionList -->
<xs:element name="propertyDescriptionList">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="s:propertyDescription" minOccurs="1" maxOccurs="unbounded"/>
        </xs:sequence>
        <xs:attribute name="publisher" type="xs:string" use="required"/>
        <xs:attribute name="product"   type="xs:string" use="required"/>
    </xs:complexType>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_formatid_and_propid">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@formatID"/>
        <xs:field    xpath="@propID"/>
    </xs:unique>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_canonical_name">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@name"/>
    </xs:unique>
</xs:element>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                        | Éléments enfants                                                   |
|---------------------------------------|------------------------------------------------------------------|
| [schema](./propdesc-schema-entry.md) | [propertyDescription](./propdesc-schema-propertydescription.md) |



 

## <a name="attributes"></a>Attributs



| Attribut | Description                                                               |
|-----------|---------------------------------------------------------------------------|
| publisher | Public. Obligatoire. Nom complet du serveur de publication fournissant le schéma. |
| product   | Public. Obligatoire. Nom complet du produit qui fournit le schéma.   |



 

## <a name="remarks"></a>Remarques

Le [propertyDescriptionList]() ne doit pas être confondu avec les « listes de propriétés » et les [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), qui sont complètement distincts.

 

 
