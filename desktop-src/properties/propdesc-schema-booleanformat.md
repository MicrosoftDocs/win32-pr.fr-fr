---
description: 'Spécifie comment IPropertyDescription :: FormatForDisplay doit mettre en forme la valeur de la propriété booleanFormat sous forme de chaîne.'
ms.assetid: f6384910-4411-4ac2-884d-3476c1b6ff96
title: booleanFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6ed13194fa18ba558c9c7fbac8fb7cd4317b67
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623715"
---
# <a name="booleanformat"></a>booleanFormat

Spécifie comment [**IPropertyDescription :: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) doit mettre en forme la valeur de la propriété en tant que chaîne. Cela s’applique uniquement si <displayInfo displayType="String"> . Il ne doit y avoir qu’un seul élément [BooleanFormat]() pour chaque élément [displayInfo](./propdesc-schema-displayinfo.md) .

S’il y a plusieurs éléments, le dernier est utilisé. Si aucun élément [BooleanFormat]() n’est fourni, les paramètres d’attribut par défaut sont appliqués à la description de la propriété.

## <a name="syntax"></a>Syntax


```
      <!-- booleanFormat -->
      <xs:element name="booleanFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="YesNo"/>
                <xs:enumeration value="OnOff"/>
                <xs:enumeration value="TrueFalse"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                   | Éléments enfants |
|--------------------------------------------------|----------------|
| [displayInfo](./propdesc-schema-displayinfo.md) | Aucune           |



 

## <a name="attributes"></a>Attributs



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>formatas</td>
<td>Public. Optionnel. La valeur par défaut est &quot; YesNo &quot; . Les valeurs valides sont les suivantes. 
<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>OuiNon</td>
<td>Par défaut. Met en forme la valeur sur &quot; Oui &quot; ou &quot; non &quot; . Requiert que le type de propriété soit booléen.</td>
</tr>
<tr class="even">
<td>ActiverDésactiver</td>
<td>Met en forme la valeur en tant que &quot; activé &quot; ou &quot; désactivé &quot; . Requiert que le type de propriété soit booléen.</td>
</tr>
<tr class="odd">
<td>TrueFalse</td>
<td>Met en forme la valeur avec la valeur &quot; true &quot; ou &quot; false &quot; . Requiert que le type de propriété soit booléen.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
