---
description: 'Spécifie comment IPropertyDescription :: FormatForDisplay doit mettre en forme la valeur de la propriété en tant que chaîne. Cela s’applique uniquement si <displayInfo displayType=&\#0034;DateTime&\#0034;> .'
ms.assetid: c290fb2e-ef5b-4dea-ba42-7c9e273a89dc
title: dateTimeFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 091898f77f4dcc37bbe65515f8606104a4d968bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202237"
---
# <a name="datetimeformat"></a>dateTimeFormat

Spécifie comment [**IPropertyDescription :: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) doit mettre en forme la valeur de la propriété en tant que chaîne. Cela s’applique uniquement si <displayInfo displayType="DateTime"> . Il ne doit y avoir qu’un seul élément [DateTimeFormat]() pour chaque élément [displayInfo](./propdesc-schema-displayinfo.md) .

S’il y a plusieurs éléments, le dernier est utilisé. Si aucun élément [DateTimeFormat]() n’est fourni, les paramètres d’attribut par défaut sont appliqués à la description de la propriété.

## <a name="syntax"></a>Syntaxe


```
      <!-- dateTimeFormat -->
      <xs:element name="dateTimeFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="General"/>
                <xs:enumeration value="Month"/>
                <xs:enumeration value="YearMonth"/>
                <xs:enumeration value="Year"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatTimeAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="ShortTime"/>
                <xs:enumeration value="LongTime"/>
                <xs:enumeration value="HideTime"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatDateAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="ShortDate"/>
                <xs:enumeration value="LongDate"/>
                <xs:enumeration value="HideDate"/>
                <xs:enumeration value="RelativeShortDate"/>
                <xs:enumeration value="RelativeLongDate"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                   | Éléments enfants |
|--------------------------------------------------|----------------|
| [displayInfo](./propdesc-schema-displayinfo.md) | Aucun           |



 

## <a name="attributes"></a>Attributs



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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
<td>Par défaut. Met en forme la valeur de date et d’heure à l’aide de <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shformatdatetimea"><strong>SHFormatDateTime</strong></a>. Utilisez les attributs <em>formatTimeAs</em> et <em>formatDateAs</em> pour spécifier le mode de mise en forme de la date et de l’heure. Requiert que le type de propriété soit DateTime.</td>
</tr>
<tr class="even">
<td>Month</td>
<td>Met en forme la valeur en tant qu’un des mois de l’année. Requiert que le type de propriété soit Int32. La valeur doit être stockée sous la forme d’une valeur numérique avec 1 représentant le premier mois de l’année.</td>
</tr>
<tr class="odd">
<td>YearMonth</td>
<td>Met en forme la valeur en tant qu' &quot; année-mois &quot; . Requiert que le type de propriété soit Int32. La valeur doit être stockée de manière à ce que les deux octets les plus élevés spécifient l’année et les deux octets inférieurs spécifient le mois.</td>
</tr>
<tr class="even">
<td>Year</td>
<td>Met en forme la valeur sous la forme d’une chaîne simple.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>formatTimeAs</td>
<td>Public. Optionnel. La valeur par défaut est &quot; ShortTime &quot; . Spécifie le format d’affichage de l’heure. S’applique quand <strong>formatas &quot; = &quot; General</strong>. Les valeurs valides sont les suivantes. 
<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ShortTime</td>
<td>Par défaut. Affichez l’heure comme &quot; 7:48 PM &quot; .</td>
</tr>
<tr class="even">
<td>Expérimenté</td>
<td>Affichez l’heure comme &quot; 7:48:33 PM &quot; .</td>
</tr>
<tr class="odd">
<td>HideTime</td>
<td>N’affiche pas la partie heure de la date.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>formatDateAs</td>
<td>Public. Optionnel. La valeur par défaut est &quot; SHORTDATE &quot; . Spécifie le format d’affichage de la date. S’applique quand <strong>formatas &quot; = &quot; General</strong>. Les valeurs valides sont les suivantes. 
<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Exemple</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ShortDate</td>
<td>Par défaut. Affichez la date comme &quot; 5/13/59 &quot; .</td>
</tr>
<tr class="even">
<td>LongDate</td>
<td>Affichez la date &quot; , par exemple mercredi 13 mai, 1959 &quot; .</td>
</tr>
<tr class="odd">
<td>HideDate</td>
<td>N’affiche pas la partie date.</td>
</tr>
<tr class="even">
<td>RelativeShortDate</td>
<td>Affichez la date comme &quot; SHORTDATE &quot; , mais utilisez des descriptions relatives, par exemple hier, dans la mesure du &quot; &quot; possible.</td>
</tr>
<tr class="odd">
<td>RelativeLongDate</td>
<td>Affichez la date comme &quot; LongDate &quot; , mais utilisez des descriptions relatives, par exemple hier, dans la mesure du &quot; &quot; possible.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
