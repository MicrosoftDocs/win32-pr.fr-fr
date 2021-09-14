---
description: image
ms.assetid: 89893C4E-4F4E-4d85-9623-08607B4383E5
title: image, élément (schéma de description de propriété)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24ecb1b88b8b724ce299a81281f926972180743
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127227448"
---
# <a name="image"></a>image

Il ne doit y avoir qu’un seul élément [image]() pour chaque élément parent.

## <a name="syntax"></a>Syntaxe


```
<!-- image -->
<xs:element name="image">
    <xs:complexType>
        <xs:attribute name="res" use="required">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:maxLength value="260"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informations sur les éléments



| Éléments parents                                                                  | Éléments enfants |
|----------------------------------------------------------------------------------|----------------|
| [enum](./propdesc-schema-enum.md), [enumRange](./propdesc-schema-enumrange.md) | None           |



 

## <a name="attributes"></a>Attributs



| Attribut | Description       |
|-----------|-------------------|
| res       | Public. Obligatoire. |



 

 

 
