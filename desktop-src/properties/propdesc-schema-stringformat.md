---
description: 'Spécifie comment IPropertyDescription :: FormatForDisplay doit mettre en forme la valeur de la propriété stringFormat sous forme de chaîne.'
ms.assetid: 7c38bc15-be86-4260-b2e4-13afc90de6d7
title: stringFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb40ec92ed7b31486062b5cca027eb5257e07af
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631898"
---
# <a name="stringformat"></a>stringFormat

Spécifie comment [**IPropertyDescription :: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) doit mettre en forme la valeur de la propriété en tant que chaîne. Cela s’applique uniquement si <displayInfo displayType="String"> . Il ne doit y avoir qu’un seul élément [stringFormat]() pour chaque élément [displayInfo](./propdesc-schema-displayinfo.md) .

S’il y a plusieurs éléments, le dernier est utilisé. Si aucun élément [stringFormat]() n’est fourni, les paramètres d’attribut par défaut sont appliqués à la description de la propriété.

## <a name="syntax"></a>Syntax


```
<!-- stringFormat -->
<xs:element name="stringFormat"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="formatAs">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="FileName"/>
                    <xs:enumeration value="FilePath"/>
                    <xs:enumeration value="Hyperlink"/>
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
<td>Public. Optionnel. La valeur par défaut est &quot; général &quot; . Les valeurs valides sont les suivantes. 
<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Général</td>
<td>Par défaut. Retourne la valeur sous forme de chaîne non mise en forme.</td>
</tr>
<tr class="even">
<td>FileName</td>
<td>Met en forme la valeur en tant que nom de fichier. Masque l’extension en fonction des paramètres utilisateur. Requiert que le type de propriété soit une chaîne.</td>
</tr>
<tr class="odd">
<td>FilePath</td>
<td>Met en forme la valeur sous la forme d’un chemin d’accès de fichier. Masque l’extension en fonction des paramètres utilisateur. Requiert que le type de propriété soit une chaîne.</td>
</tr>
<tr class="even">
<td>Hyperlink</td>
<td>Met en forme la valeur en tant que lien hypertexte.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
