---
description: 'Spécifie comment IPropertyDescription :: FormatForDisplay doit mettre en forme la valeur de la propriété en tant que chaîne.'
ms.assetid: 49ba57b8-3e08-425f-98b2-52ed2c41a488
title: enumeratedList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d098b47463b65c483be68eb7750da929df43cee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519720"
---
# <a name="enumeratedlist"></a>enumeratedList

Spécifie comment [**IPropertyDescription :: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) doit mettre en forme la valeur de la propriété en tant que chaîne. Elle influence également la manière dont la propriété peut être regroupée, ou les valeurs à afficher dans la liste si « editControl » est un listblox. Cela s’applique uniquement si <displayInfo displayType="Enumerated"> . Il ne doit y avoir qu’un seul élément [enumeratedList]() pour chaque élément [displayInfo](./propdesc-schema-displayinfo.md) .

S’il y a plusieurs éléments, le dernier est utilisé. Si aucun élément [enumeratedList]() n’est fourni, les paramètres d’attribut par défaut sont appliqués à la description de la propriété.

## <a name="syntax"></a>Syntaxe


```
<!-- enumeratedList -->
<xs:element name="enumeratedList"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="value" type="xs:string" use="required"/>
                    <xs:attribute name="text" type="xs:string" use="required"/>
                </xs:complexType>
            </xs:element>
            <xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="minValue" type="xs:integer" use="required"/>
                    <xs:attribute name="setValue" type="xs:integer"/>
                    <xs:attribute name="text" type="xs:string"/>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
        <xs:attribute name="defaultText" type="xs:string"/>
        <xs:attribute name="useValueForDefault" type="xs:boolean"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                   | Éléments enfants                               |
|--------------------------------------------------|----------------------------------------------|
| [displayInfo](./propdesc-schema-displayinfo.md) | [variables](./propdesc-schema-enum.md)           |
|                                                  | [enumRange](./propdesc-schema-enumrange.md) |



 

## <a name="attributes"></a>Attributs



| Attribut          | Description                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| defaultText        | Public. Optionnel. Spécifiez le texte par défaut à utiliser si une valeur est donnée à [**IPropertyDescription :: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) qui n’est pas mappée à l’un des éléments énumérés dans la liste. La syntaxe autorise une chaîne d’affichage directe ou une référence à une chaîne d’affichage indirecte ; Utilisez la référence, afin qu’elle puisse être localisée.                              |
| useValueForDefault | Public. Optionnel. Si la valeur est définie sur « true », [**IPropertyDescription :: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) utilise la valeur telle quelle si la valeur n’est pas mappée à l’un des éléments énumérés dans la liste. Pour **IPropertyDescription :: FormatForDisplay**, l’affectation de la valeur « true » a priorité sur la définition de « DefaultText ». La valeur par défaut est « false ». |



 

 

 
