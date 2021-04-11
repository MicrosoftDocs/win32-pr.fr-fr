---
description: Nouveauté de Windows 7. Identifie une propriété qui est associée à la propriété définie dans le fichier de description de la propriété.
ms.assetid: 30167942-141A-4f37-B019-0811BA654124
title: relatedProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cabde093a47a25834598659d3ad38e0847c1351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318897"
---
# <a name="relatedproperty"></a>relatedProperty

Nouveauté de Windows 7. Identifie une propriété qui est associée à la propriété définie dans le fichier de description de la propriété. Au besoin, il peut y avoir autant d’éléments [relatedProperty]() dans un [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) .

## <a name="syntax"></a>Syntaxe


```
<!-- relatedPropertyInfo -->
<xs:element name="relatedProperty" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:attribute name="relationshipName" type="canonical-name" use="required"/>
        <xs:attribute name="propertyName" type="canonical-name" use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                                   | Éléments enfants |
|------------------------------------------------------------------|----------------|
| [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) | Aucun           |



 

## <a name="attributes"></a>Attributs



| Attribut        | Description                                                        |
|------------------|--------------------------------------------------------------------|
| relationshipName | Public. Obligatoire. Nom canonique de la relation de propriété. |
| propertyName     | Public. Obligatoire. Nom canonique de la propriété associée.      |



 

## <a name="remarks"></a>Notes

Cet élément vous permet de mapper une propriété à une autre. Par exemple, vous pouvez mapper le texte de votre propriété personnalisée, fabrikam. StorageCapacity, à System. Capacity :


```
<!-- relatedPropertyInfo -->
<propertyDescription name="Fabrikam.StorageCapacity" ... >
    ...
    <relatedPropertyInfo>
        <relatedProperty relationshipName="System.RelatedProperty.Text" propertyName="System.Capacity"/>
    </relatedPropertyInfo>
</propertyDescription>
```



 

 
