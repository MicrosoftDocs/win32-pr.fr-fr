---
description: 'Spécifie comment IPropertyDescription :: FormatForDisplay doit mettre en forme la valeur de la propriété en tant que chaîne. Cela s’applique uniquement si <displayInfo displayType=&\#0034;Number&\#0034;> .'
ms.assetid: 9e8cfe5c-e17a-40d6-958f-a1bd1130c699
title: numberFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6750a9fb4dcf6a7a56c350fccf80241644b956da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106540845"
---
# <a name="numberformat"></a>numberFormat

Spécifie comment [**IPropertyDescription :: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) doit mettre en forme la valeur de la propriété en tant que chaîne. Cela s’applique uniquement si <displayInfo displayType="Number"> . Il ne doit y avoir qu’un seul élément [NumberFormat]() pour chaque élément [displayInfo](./propdesc-schema-displayinfo.md) .

S’il y a plusieurs éléments, le dernier est utilisé. Si aucun élément [NumberFormat]() n’est fourni, les paramètres d’attribut par défaut sont appliqués à la description de la propriété.

## <a name="syntax"></a>Syntaxe


```
      <!-- numberFormat -->
      <xs:element name="numberFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="General"/>
                <xs:enumeration value="Percentage"/>
                <xs:enumeration value="ByteSize"/>
                <xs:enumeration value="KBSize"/>
                <xs:enumeration value="SampleSize"/>
                <xs:enumeration value="Bitrate"/>
                <xs:enumeration value="SampleRate"/>
                <xs:enumeration value="FrameRate"/>
                <xs:enumeration value="Pixels"/>
                <xs:enumeration value="DPI"/>
                <xs:enumeration value="Duration"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatDurationAs">
              <xs:restriction base="xs:string">
                <xs:enumeration value="hh:mm"/>
                <xs:enumeration value="hh:mm:ss"/>
                <xs:enumeration value="hh:mm:ss.fff"/>
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
<td>Public. Optionnel. La valeur par défaut est &quot; général &quot; . Spécifie le format d’affichage. Les valeurs valides sont les suivantes. 
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
<td>Par défaut. Affiche la valeur sous la forme d’un nombre sans mise en forme.</td>
</tr>
<tr class="even">
<td>Pourcentage</td>
<td>Met en forme la valeur sous la forme d’un pourcentage. Requiert que la propriété soit UInt32.</td>
</tr>
<tr class="odd">
<td>Taille d’octet</td>
<td>Met en forme la valeur en tant qu’octet, &quot; Ko &quot; , &quot; Mo &quot; ou &quot; Go, selon le &quot; cas. Requiert que la propriété soit UInt64.</td>
</tr>
<tr class="even">
<td>KBSize</td>
<td>Met en forme la valeur en tant que &quot; Ko &quot; , quelle que soit la valeur. Requiert que la propriété soit UInt64.</td>
</tr>
<tr class="odd">
<td>SampleSize</td>
<td>Met en forme la valeur en tant que nombre de bits. Requiert que la propriété soit UInt32.</td>
</tr>
<tr class="even">
<td>Débit binaire</td>
<td>Met en forme la valeur en &quot; Kbits/s &quot; . Requiert que la propriété soit UInt32. La valeur doit être stockée en &quot; unités de bits par seconde &quot; .</td>
</tr>
<tr class="odd">
<td>SampleRate</td>
<td>Met en forme la valeur en &quot; kHz &quot; . Requiert que la propriété soit UInt32. La valeur doit être stockée en &quot; Hertz &quot; unités.</td>
</tr>
<tr class="even">
<td>FrameRate</td>
<td>Met en forme la valeur en images/seconde. Requiert que la propriété soit UInt32. La valeur doit être stockée en &quot; unités de kilo-images par &quot; seconde.</td>
</tr>
<tr class="odd">
<td>Pixels</td>
<td>Met en forme la valeur en unités en pixels. Requiert que la propriété soit UInt32.</td>
</tr>
<tr class="even">
<td>PPP</td>
<td>Met en forme la valeur en points par pouce. Requiert que la propriété soit UInt32.</td>
</tr>
<tr class="odd">
<td>Duration</td>
<td>Met en forme la valeur en tant que durée. Utilisez <formatDurationAs> pour spécifier le format de durée. Requiert que la propriété soit UInt64.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>formatDurationAs</td>
<td>Public. Optionnel. La valeur par défaut est &quot; hh : mm : SS &quot; . S’applique uniquement si <em>formatas &quot; = &quot; Duration</em>. Requiert que la propriété soit UInt64. Les valeurs valides sont les suivantes. 
<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>hh:mm</td>
<td>Met en forme la valeur en heures et minutes.</td>
</tr>
<tr class="even">
<td>hh:mm:ss</td>
<td>Par défaut. Met en forme la valeur en heures, minutes et secondes.</td>
</tr>
<tr class="odd">
<td>hh : mm : SS. fff</td>
<td>Met en forme la valeur en heures, minutes, secondes et millisecondes.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
