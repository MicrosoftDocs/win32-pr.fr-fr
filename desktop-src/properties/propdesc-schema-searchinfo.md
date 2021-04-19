---
description: Spécifie comment configurer le moteur de recherche Windows par rapport à une définition de propriété donnée.
ms.assetid: 1cb0b630-323c-41cf-8aaf-db3028b2e369
title: searchInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eee94585aaa66a761e527ac6ada1c33b0d23966d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517774"
---
# <a name="searchinfo"></a>searchInfo

Spécifie comment configurer le moteur de recherche Windows par rapport à une définition de propriété donnée. Si aucun élément [searchInfo]() n’est fourni, la propriété n’est pas incluse dans le moteur de recherche Windows. Cet élément a été modifié pour Windows 7.

## <a name="syntax-for-windows-7"></a>Syntaxe pour Windows 7


```
<!-- searchInfo for Windows 7-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                    <xs:enumeration value="OnDiskAll"/>
                    <xs:enumeration value="OnDiskVector"/>
                    <xs:enumeration value="OnDemand"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="512"/>
        <xs:attribute name="mnemonics" type="xs:string"/>                            
    </xs:complexType>
</xs:element>
```



## <a name="syntax-for-windows-vista"></a>Syntaxe pour Windows Vista


```
<!-- searchInfo for Windows Vista-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="128"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                                   | Éléments enfants |
|------------------------------------------------------------------|----------------|
| [propertyDescription](./propdesc-schema-propertydescription.md) | Aucun           |



 

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
<td>inInvertedIndex</td>
<td>Public. Optionnel. Indique si la valeur de la propriété doit être stockée dans l’index inversé. Cela permet aux utilisateurs finaux d’effectuer des requêtes de texte intégral sur les valeurs de cette propriété. La valeur par défaut est &quot;false&quot;.</td>
</tr>
<tr class="even">
<td>isColumn</td>
<td>Public. Optionnel. Indique si la propriété doit également être stockée dans la base de données de recherche Windows en tant que colonne, de sorte que les éditeurs de logiciels indépendants puissent créer des requêtes basées sur des prédicats (par exemple, &quot; sélectionnez * où &quot; System. title &quot; = 'qqq' &quot; ). Si le créateur du schéma souhaite permettre aux utilisateurs finaux (ou aux développeurs) de créer des requêtes basées sur des prédicats sur les propriétés, cette valeur doit être définie sur &quot; true &quot; . La valeur par défaut est &quot;false&quot;.</td>
</tr>
<tr class="odd">
<td>isColumnSparse</td>
<td>Public. Optionnel. La valeur par défaut est &quot;true&quot;. Si la propriété est à valeurs multiples, cet attribut a toujours la &quot; valeur true &quot; .</td>
</tr>
<tr class="even">
<td>columnIndexType</td>
<td>Public. Optionnel. Pour optimiser le tri et le regroupement, le moteur de recherche Windows peut créer des index secondaires pour les propriétés qui ont isColumn = &quot; true &quot; . Cet attribut est utile uniquement lorsque inInvertedIndex a la &quot; valeur true &quot; dans Windows Vista ou lorsque isColumn a la &quot; valeur true &quot; dans Windows 7. Si la propriété a tendance à être triée fréquemment par les utilisateurs, cet attribut doit être spécifié. La valeur par défaut dans Windows Vista est &quot; NotIndexed &quot; . La valeur par défaut dans Windows 7 est &quot; OnDemand &quot; . Les valeurs suivantes sont valides.
<ul>
<li><strong>NotIndexed</strong>: ne jamais générer un index de valeur.</li>
<li><strong>OnDisk</strong>: générer un index de valeur par défaut pour cette propriété.</li>
<li><strong>OnDiskAll</strong> (Windows 7 et versions ultérieures uniquement) : générez un index de valeur par défaut pour cette propriété, et s’il s’agit d’une propriété Vector, également un index de valeur pour toutes les valeurs de vecteur concaténées.</li>
<li><strong>OnDiskVector</strong> (Windows 7 et versions ultérieures uniquement) : générez un index de valeur par défaut pour les valeurs de vecteur concaténées.</li>
<li><strong>OnDemand</strong> (Windows 7 et versions ultérieures uniquement) : générez uniquement les index de valeur par demande, autrement dit, la première fois qu’ils sont utilisés pour une requête.</li>
</ul></td>
</tr>
<tr class="odd">
<td>maxSize</td>
<td>Public. Optionnel. Taille maximale, en octets, autorisée pour une certaine propriété qui est stockée dans la base de données de recherche Windows. La valeur par défaut est :
<ul>
<li><strong>Windows Vista</strong>: 128 octets</li>
<li><strong>Windows 7 et versions ultérieures</strong>: 512 octets</li>
</ul>
Notez que cette taille maximale est mesurée en octets, et non en caractères. Le nombre maximal de caractères dépend de leur encodage.<br/></td>
</tr>
<tr class="even">
<td>mnémoniques</td>
<td><strong>Windows 7 et versions ultérieures.</strong> Public. Optionnel. Liste de valeurs mnémoniques qui peuvent être utilisées pour faire référence à la propriété dans les requêtes de recherche. La liste est délimitée par le caractère « | ».</td>
</tr>
</tbody>
</table>



 

 

 
