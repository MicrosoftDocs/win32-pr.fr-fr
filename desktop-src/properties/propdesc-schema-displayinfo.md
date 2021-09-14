---
description: Spécifie les informations d’affichage d’une propriété.
ms.assetid: 27c03ced-a5fa-4ab4-b88e-5b78701da878
title: displayInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0bbc3cf0f17d24672e30a110d95341c1cb902d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235541"
---
# <a name="displayinfo"></a>displayInfo

Spécifie les informations d’affichage d’une propriété. Il ne doit y avoir qu’un seul élément [displayInfo]() pour chaque [PropertyDescription](./propdesc-schema-propertydescription.md).

S’il y a plusieurs éléments, le dernier est utilisé. Si aucun élément [displayInfo]() n’est fourni, les paramètres d’attribut par défaut sont appliqués à la description de la propriété.

## <a name="syntax"></a>Syntaxe


```
<!-- displayInfo -->
<xs:element name="displayInfo">
    <xs:complexType>
        <xs:all>
            <xs:element name="stringFormat" minOccurs="0" maxOccurs="1">
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
            <xs:element name="booleanFormat" minOccurs="0" maxOccurs="1">
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
            <xs:element name="numberFormat" minOccurs="0" maxOccurs="1">
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
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="hh:mm"/>
                                <xs:enumeration value="hh:mm:ss"/>
                                <xs:enumeration value="hh:mm:ss.fff"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="dateTimeFormat" minOccurs="0" maxOccurs="1">
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
            <xs:element name="enumeratedList" minOccurs="0" maxOccurs="1">
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
                                <xs:attribute name="minValue" type="xs:string" use="required"/>
                                <xs:attribute name="setValue" type="xs:string"/>
                                <xs:attribute name="text" type="xs:string"/>
                            </xs:complexType>
                        </xs:element>
                    </xs:sequence>

                    <xs:attribute name="defaultText" type="xs:string"/>
                    <xs:attribute name="useValueForDefault" type="xs:boolean"/>
                </xs:complexType>
            </xs:element>
            <xs:element name="drawControl" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="control">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="Default"/>
                                <xs:enumeration value="MultiLineText"/>
                                <xs:enumeration value="MultiValueText"/>
                                <xs:enumeration value="PercentBar"/>
                                <xs:enumeration value="ProgressBar"/>
                                <xs:enumeration value="Rating"/>
                                <xs:enumeration value="StaticText"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="editControl" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="control">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="Default"/>
                                <xs:enumeration value="Calendar"/>
                                <xs:enumeration value="CheckboxDropList"/>
                                <xs:enumeration value="DropList"/>
                                <xs:enumeration value="MultiLineText"/>
                                <xs:enumeration value="MultiValueText"/>
                                <xs:enumeration value="Rating"/>
                                <xs:enumeration value="Text"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="filterControl" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="control">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="Default"/>
                                <xs:enumeration value="Calendar"/>
                                <xs:enumeration value="Rating"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="queryControl" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="control">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="Default"/>
                                <xs:enumeration value="Boolean"/>
                                <xs:enumeration value="Calendar"/>
                                <xs:enumeration value="CheckboxDropList"/>
                                <xs:enumeration value="DropList"/>
                                <xs:enumeration value="MultiValueText"/>
                                <xs:enumeration value="NumericText"/>
                                <xs:enumeration value="Rating"/>
                                <xs:enumeration value="Text"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
        </xs:all>

        <xs:attribute name="defaultColumnWidth" type="xs:nonNegativeInteger" default="20"/>
        <xs:attribute name="displayType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Number"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Enumerated"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        
        <xs:attribute name="alignment" default="Left">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Left"/>
                    <xs:enumeration value="Center"/>
                    <xs:enumeration value="Right"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="relativeDescriptionType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="Date"/>
                    <xs:enumeration value="Size"/>
                    <xs:enumeration value="Count"/>
                    <xs:enumeration value="Revision"/>
                    <xs:enumeration value="Length"/>
                    <xs:enumeration value="Duration"/>
                    <xs:enumeration value="Speed"/>
                    <xs:enumeration value="Rate"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Priority"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="defaultSortDirection" default="Ascending">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                  <xs:enumeration value="Ascending"/>
                  <xs:enumeration value="Descending"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                                   | Éléments enfants                                                                                                 |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [propertyDescription](./propdesc-schema-propertydescription.md) | [stringFormat](./propdesc-schema-stringformat.md)                                                             |
|                                                                  | [booleanFormat](./propdesc-schema-booleanformat.md)                                                           |
|                                                                  | [numberFormat](./propdesc-schema-numberformat.md)                                                             |
|                                                                  | [dateTimeFormat](./propdesc-schema-datetimeformat.md)                                                         |
|                                                                  | [enumeratedList](./propdesc-schema-enumeratedlist.md)                                                         |
|                                                                  | [drawControl](./propdesc-schema-drawcontrol.md)                                                               |
|                                                                  | [editControl](./propdesc-schema-editcontrol.md)                                                               |
|                                                                  | [filterControl](./propdesc-schema-filtercontrol.md)                                                           |
|                                                                  | [queryControl](./propdesc-schema-querycontrol.md) (Windows Vista uniquement. non pris en charge dans Windows 7 et versions ultérieures.) |



 

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
<td>defaultColumnWidth</td>
<td>Public. Optionnel. La valeur par défaut est &quot; 20 &quot; .</td>
</tr>
<tr class="even">
<td>displayType</td>
<td>Public. Optionnel. La valeur par défaut est &quot; String &quot; . Spécifie le type de la chaîne d’affichage. Une fois définis ici, les valeurs de <strong>PROPDESC_DISPLAYTYPE</strong> associées sont récupérées par <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplaytype"><strong>IPropertyDescription :: GetDisplayType</strong></a>. Les types suivants sont valides. 
<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>String</td>
<td>Par défaut. La valeur est affichée sous la forme d’une chaîne. Utilisez &quot; stringFormat &quot; pour mettre en forme. La méthode retourne PDDT_STRING.</td>
</tr>
<tr class="even">
<td>Number</td>
<td>Valeur par défaut pour les propriétés numériques. La valeur est affichée sous la forme d’un nombre. Utilisez &quot; NumberFormat &quot; pour mettre en forme. La méthode retourne PDDT_NUMBER.</td>
</tr>
<tr class="odd">
<td>Booléen</td>
<td>Valeur par défaut si <typeInfo type=&quot;Boolean&quot;> . La valeur est affichée sous la forme d’une valeur booléenne. Utilisez &quot; BooleanFormat &quot; pour mettre en forme. La méthode retourne PDDT_BOOLEAN.</td>
</tr>
<tr class="even">
<td>DateTime</td>
<td>Valeur par défaut si <typeInfo type=&quot;DateTime&quot;> . La valeur est affichée sous la forme d’une date ou d’une heure. Utilisez &quot; DateTimeFormat &quot; pour mettre en forme. La méthode retourne PDDT_DATETIME.</td>
</tr>
<tr class="odd">
<td>Énumération</td>
<td>La valeur est affichée sous la forme d’un mappage de chaîne d’affichage fourni par l' &quot; &quot; élément enumeratedList. La méthode retourne PDDT_ENUMERATED.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>alignement</td>
<td>Optionnel. La valeur par défaut est &quot; gauche &quot; . 
<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Gauche</td>
<td>Par défaut. Aligner à gauche.</td>
</tr>
<tr class="even">
<td>Center</td>
<td>Aligner le centre.</td>
</tr>
<tr class="odd">
<td>Right</td>
<td>Aligner à droite.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>relativeDescriptionType</td>
<td>Optionnel. La valeur par défaut est &quot; général &quot; . Spécifie comment deux valeurs de cette propriété doivent être décrites lorsqu’elles sont comparées les unes avec les autres. Dans le cas d’une équivalence, &quot; même &quot; est toujours utilisé. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescription"><strong>IPropertyDescription :: GetRelativeDescription</strong></a> et <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescriptiontype"><strong>IPropertyDescription :: GetRelativeDescriptionType</strong></a> utilisent cette valeur pour déterminer les noms d’affichage de description relative à utiliser. 
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
<td>Par défaut. Utilise des différences différentes &quot; &quot;  /  &quot; &quot;  /  &quot; &quot; .</td>
</tr>
<tr class="even">
<td>Date</td>
<td>Valeur par défaut si <typeInfo type=&quot;DateTime&quot;> . Utilise le même plus &quot; &quot;  /  &quot; &quot;  /  &quot; tard &quot; , ou utilise une version plus &quot; &quot;  /  &quot; &quot;  /  &quot; récente &quot; , &quot; ou &quot;  /  &quot; &quot;  /  &quot; &quot; utilise la même version plus tôt.</td>
</tr>
<tr class="odd">
<td>Taille</td>
<td>Utilise &quot; le &quot;  /  &quot; même &quot;  /  &quot; plus petit&quot;</td>
</tr>
<tr class="even">
<td>Nombre</td>
<td>Utilise &quot; le &quot;  /  &quot; même &quot;  /  &quot; plus petit&quot;</td>
</tr>
<tr class="odd">
<td>Révision</td>
<td>Utilise &quot; le &quot;  /  &quot; même plus &quot;  /  &quot; tard&quot;</td>
</tr>
<tr class="even">
<td>Longueur</td>
<td>Utilise une &quot; &quot;  /  &quot; &quot;  /  &quot; longueur plus faible&quot;</td>
</tr>
<tr class="odd">
<td>Duration</td>
<td>Utilise une &quot; &quot;  /  &quot; &quot;  /  &quot; longueur plus faible&quot;</td>
</tr>
<tr class="even">
<td>Vitesse</td>
<td>Utilise plus &quot; lentement que &quot;  /  &quot; &quot;  /  &quot; plus rapide&quot;</td>
</tr>
<tr class="odd">
<td>Tarif</td>
<td>Utilise plus &quot; lentement que &quot;  /  &quot; &quot;  /  &quot; plus rapide&quot;</td>
</tr>
<tr class="even">
<td>Rating</td>
<td>Utilise &quot; &quot;  /  &quot; &quot;  /  &quot; une valeur inférieure identique&quot;</td>
</tr>
<tr class="odd">
<td>Priority</td>
<td>Utilise &quot; &quot;  /  &quot; &quot;  /  &quot; une valeur inférieure identique&quot;</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>defaultSortDirection</td>
<td>Spécifie le sens du tri. La valeur par défaut est &quot; croissant &quot; . 
<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Croissant</td>
<td>Trie l’ordre croissant.</td>
</tr>
<tr class="even">
<td>Décroissant</td>
<td>Trie dans l’ordre décroissant.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
