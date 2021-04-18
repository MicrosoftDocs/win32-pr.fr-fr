---
description: Spécifie les informations de type d’une propriété.
ms.assetid: ae1f8835-ef6c-42bb-b44f-ad374337a012
title: typeInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa783a606066163fd8b17f53ef8a0fe2da44e539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533819"
---
# <a name="typeinfo"></a>typeInfo

Spécifie les informations de type d’une propriété. Il ne doit y avoir qu’un seul élément [TypeInfo]() pour chaque [PropertyDescription](./propdesc-schema-propertydescription.md). Cet élément a été modifié pour Windows 7.

S’il y a plusieurs éléments, le dernier est utilisé. Si aucun élément [TypeInfo]() n’est fourni, les paramètres d’attribut par défaut sont appliqués à la description de la propriété.

## <a name="syntax-for-windows-7"></a>Syntaxe pour Windows 7


```
<!-- typeInfo for Windows 7-->
<xs:element name="typeInfo">
    <xs:complexType>
        <xs:attribute name="type" default="Any">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Any"/>
                    <xs:enumeration value="Null"/>
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Byte"/>
                    <xs:enumeration value="Buffer"/>
                    <xs:enumeration value="Int16"/>
                    <xs:enumeration value="UInt16"/>
                    <xs:enumeration value="Int32"/>
                    <xs:enumeration value="UInt32"/>
                    <xs:enumeration value="Int64"/>
                    <xs:enumeration value="UInt64"/>
                    <xs:enumeration value="Double"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Guid"/>
                    <xs:enumeration value="Blob"/>
                    <xs:enumeration value="Stream"/>
                    <xs:enumeration value="Clipboard"/>
                    <xs:enumeration value="Object"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="groupingRange">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Discrete"/>
                    <xs:enumeration value="Alphanumeric"/>
                    <xs:enumeration value="Size"/>
                    <xs:enumeration value="Date"/>
                    <xs:enumeration value="Dynamic"/>
                    <xs:enumeration value="Percent"/>
                    <xs:enumeration value="Enumerated"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="isInnate" type="xs:boolean" default="false"/>
        <xs:attribute name="canBePurged" type="xs:boolean"/>
        <xs:attribute name="multipleValues" type="xs:boolean" default="false"/>
        <xs:attribute name="isGroup" type="xs:boolean" default="false"/>
        <xs:attribute name="aggregationType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="First"/>
                    <xs:enumeration value="Sum"/>
                    <xs:enumeration value="Average"/>
                    <xs:enumeration value="DateRange"/>
                    <xs:enumeration value="Union"/>
                    <xs:enumeration value="Maximum"/>
                    <xs:enumeration value="Minimum"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="isTreeProperty" type="xs:boolean" default="false"/>
        <xs:attribute name="isViewable" type="xs:boolean" default="false"/>
        <xs:attribute name="isQueryable" type="xs:boolean" default="false"/>
        <xs:attribute name="includeInFullTextQuery" type="xs:boolean" default="false"/>
        <xs:attribute name="searchRawValue" type="xs:boolean" default="false"/>
        <xs:attribute name="conditionType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="None"/>
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Number"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Size"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="defaultOperation">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Equal"/>
                    <xs:enumeration value="NotEqual"/>
                    <xs:enumeration value="LessThan"/>
                    <xs:enumeration value="GreaterThan"/>
                    <xs:enumeration value="Contains"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
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
<td>type</td>
<td>Public. Optionnel. La valeur par défaut est &quot; Any &quot; . Indique le type de la propriété. Les types suivants sont valides et les types de variantes associés sont récupérés par <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription :: GetPropertyType</strong></a>. 
<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Quelconque</td>
<td>Par défaut. Le sous-système de propriété n’applique pas ou ne force pas la valeur de la propriété. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription :: GetPropertyType</strong></a> retourne VT_NULL. Les éditeurs de logiciels indépendants (ISV) sont fortement encouragés à fournir un type au lieu de revenir sur cette valeur par défaut.</td>
</tr>
<tr class="even">
<td>Null</td>
<td>Il n’y a aucune valeur pour cette propriété. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription :: GetPropertyType</strong></a> retourne VT_NULL.</td>
</tr>
<tr class="odd">
<td>String</td>
<td>La valeur doit être un VT_LPWSTR, qui est une chaîne Unicode terminée par une référence null.</td>
</tr>
<tr class="even">
<td>Boolean</td>
<td>La valeur doit être un VT_BOOL, qui est une valeur booléenne.</td>
</tr>
<tr class="odd">
<td>Byte</td>
<td>La valeur doit être un VT_UI1, qui est un octet.</td>
</tr>
<tr class="even">
<td>Buffer</td>
<td>La valeur doit être un VT_UI1 | Mémoire tampon d’octets VT_VECTOR.</td>
</tr>
<tr class="odd">
<td>Int16</td>
<td>La valeur doit être un VT_I2, qui est un entier de 16 bits.</td>
</tr>
<tr class="even">
<td>UInt16</td>
<td>La valeur doit être un VT_UI2, qui est un entier non signé 16 bits.</td>
</tr>
<tr class="odd">
<td>Int32</td>
<td>La valeur doit être un VT_I4, qui est un entier 32 bits.</td>
</tr>
<tr class="even">
<td>UInt32</td>
<td>La valeur doit être un VT_UI4, qui est un entier non signé 32 bits.</td>
</tr>
<tr class="odd">
<td>Int64</td>
<td>La valeur doit être un VT_I8, qui est un entier 64 bits.</td>
</tr>
<tr class="even">
<td>UInt64</td>
<td>La valeur doit être un VT_UI8, qui est un entier non signé 64 bits.</td>
</tr>
<tr class="odd">
<td>Double</td>
<td>La valeur doit être un VT_R8, qui est un double.</td>
</tr>
<tr class="even">
<td>DateTime</td>
<td>La valeur doit être un VT_FILETIME, qui est un <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>fileTime</strong></a>.</td>
</tr>
<tr class="odd">
<td>Guid</td>
<td>La valeur doit être un VT_CLSID, qui est un identificateur de classe (CLSID).</td>
</tr>
<tr class="even">
<td>Objet blob</td>
<td>La valeur doit être un VT_BLOB, qui sont des octets à préfixe de longueur.</td>
</tr>
<tr class="odd">
<td>Stream</td>
<td>La valeur doit être un VT_STREAM, qui est un objet qui implémente <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a>.</td>
</tr>
<tr class="even">
<td>Presse-papiers</td>
<td>La valeur doit être un VT_CF, qui est un format de presse-papiers.</td>
</tr>
<tr class="odd">
<td>Object</td>
<td>La valeur doit être un VT_UNKNOWN, qui est un objet qui implémente <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>groupingRange</td>
<td>Optionnel. La valeur par défaut est &quot; discrète &quot; . Spécifie le mode d’affichage de la propriété lorsqu’une vue est regroupée par cette propriété. Une fois définis ici, ces valeurs sont récupérées par <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getgroupingrange"><strong>IPropertyDescription :: GetGroupingRange</strong></a>. Les types suivants sont valides.

<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Discret</td>
<td>Par défaut. Affiche des valeurs individuelles.</td>
</tr>
<tr class="even">
<td>Alphanumérique</td>
<td>Affiche des plages alphanumériques statiques pour les valeurs.</td>
</tr>
<tr class="odd">
<td>Taille</td>
<td>Affiche des plages de tailles statiques pour les valeurs.</td>
</tr>
<tr class="even">
<td>Date</td>
<td>Affiche les groupes de mois/années. Valeur par défaut pour les propriétés de type = &quot; DateTime &quot; .</td>
</tr>
<tr class="odd">
<td>TimeRelative</td>
<td>Affiche dans des groupes relatifs à l’heure.</td>
</tr>
<tr class="even">
<td>Dynamique</td>
<td>Affiche les plages créées dynamiquement pour les valeurs.</td>
</tr>
<tr class="odd">
<td>Pourcentage</td>
<td>Affiche le pourcentage de compartiments.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>isInnate</td>
<td>Public. Optionnel. La valeur par défaut est &quot;false&quot;. Spécifie si la propriété est considérée comme innée. Une propriété innée est une propriété qui est soit calculée à partir du contenu d’un fichier, soit à partir d’autres ressources ou systèmes. Par exemple, System. Size est une propriété innée fournie par le système de fichiers. la modification de la valeur de la propriété dans et de elle-même ne fait rien. Les autres exemples sont System. image. dimensions et System.Document. PageCount, qui sont calculées par des programmes basés sur le contenu du fichier, et non sur la base d’un paramètre modifiable par l’utilisateur. La définition de isInnate = &quot; true &quot; signifie que l’utilisateur ne peut pas modifier cette propriété directement via un contrôle de propriété. Cette valeur correspond à l’indicateur de PDTF_ISINNATE défini dans <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> et utilisé dans <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription :: GetTypeFlags</strong></a>.</td>
</tr>
<tr class="even">
<td>canBePurged</td>
<td><strong>Windows Vista avec Service Pack 1 (SP1) et versions ultérieures uniquement</strong>. Public. Optionnel. Quand la valeur &quot; &quot; est true, permet de supprimer une propriété innée. Les propriétés innées, calculées à partir d’autres propriétés, sont en lecture seule par définition. La valeur par défaut de cet attribut dépend de la valeur <em>isInnate</em> .

<table>
<thead>
<tr class="header">
<th>isInnate</th>
<th>Valeur par défaut de canBePurged</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>true</td>
<td>false</td>
</tr>
<tr class="even">
<td>false</td>
<td>true</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
Une propriété dont la valeur <em>isInnate</em> est &quot; false &quot; (ce qui signifie que la propriété est en lecture/écriture) ne peut pas également définir la valeur <em>canBePurged</em> sur &quot; false &quot; . Cette restriction est appliquée par le système d’exploitation.
</blockquote>
</div>
<div>
 
</div>
<p>Bien que cet attribut ait été introduit dans Windows Vista avec Service Pack 1 (SP1), un fichier. propDesc qui comprend cet attribut est compatible avec Windows Vista avant Windows Vista avec SP1. L’attribut <em>canBePurged</em> est simplement ignoré dans cette situation.</p></td>
</tr>
<tr class="odd">
<td>multipleValues</td>
<td>Public. Optionnel. La valeur par défaut est &quot;false&quot;. Spécifie si cette propriété peut avoir plusieurs valeurs. Cette valeur correspond à l’indicateur de PDTF_MULTIPLEVALUES défini dans <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> et utilisé dans <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription :: GetTypeFlags</strong></a>. Cela détermine également si VT_VECTOR est ou non le VARTYPE de la valeur de propriété.</td>
</tr>
<tr class="even">
<td>isGroup</td>
<td>Public. Optionnel. La valeur par défaut est &quot;false&quot;. Spécifie si la propriété est un en-tête de groupe. Un en-tête de groupe est strictement utilisé dans les fichiers. il n’a pas de valeur, n’est jamais stocké dans un fichier et doit également avoir <typeInfo type=&quot;Null&quot;> . Certaines interfaces utilisateur du système utilisent des plist pour indiquer la séquence des propriétés à afficher. Ces exemples peuvent inclure des références à des en-têtes de groupe (par exemple, System. PropGroup. Camera), qui indiquent à l’interface utilisateur de démarrer une nouvelle section de groupe (par exemple, les paramètres de l' &quot; appareil photo &quot; ). Une description de propriété avec isGroup = &quot; true &quot; doit spécifier un <labelInfo label=&quot;Some localized label&quot;> , sinon il ne s’agit pas d’une propriété utile. Cette valeur correspond à l’indicateur de PDTF_ISGROUP défini dans <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> et utilisé dans <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription :: GetTypeFlags</strong></a>.</td>
</tr>
<tr class="odd">
<td>aggregationType</td>
<td>Public. Optionnel. La valeur par défaut est &quot; default &quot; . Spécifie la manière dont les propriétés d’agrégation sont affichées lorsque plusieurs éléments sont sélectionnés. Une fois définis ici, ces valeurs sont récupérées par <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getaggregationtype"><strong>IPropertyDescription :: GetAggregationType</strong></a> en tant que <a href="/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type"><strong>PROPDESC_AGGREGATION_TYPE</strong></a>. Les types suivants sont valides.

<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Default</td>
<td>Par défaut. Affiche un espace réservé à <strong>plusieurs valeurs</strong> dans l’interface utilisateur. Il s’agit de la valeur par défaut si le <em>type</em> est incompatible avec le <em>aggregationType</em>spécifié.</td>
</tr>
<tr class="even">
<td>Premier</td>
<td>Affiche la valeur de la propriété du premier élément de la sélection ou de la collection.</td>
</tr>
<tr class="odd">
<td>SUM</td>
<td>Affiche la somme des valeurs numériques. Utile pour les propriétés telles que System. Media. Duration ou System. Size. Cette valeur n’est pas compatible avec les types non numériques.</td>
</tr>
<tr class="even">
<td>Moyenne</td>
<td>Affiche la moyenne des valeurs numériques. Utile pour les propriétés telles que System. Rating. Cette valeur n’est pas compatible avec les types non numériques.</td>
</tr>
<tr class="odd">
<td>DateRange</td>
<td>Affiche une plage de dates. Utile pour les propriétés telles que System. photo. DateTaken. Cette valeur n’est pas compatible avec tout sauf type = &quot; DateTime &quot; et est la valeur par défaut pour les propriétés de ce type.</td>
</tr>
<tr class="even">
<td>Union</td>
<td>Affiche une Union de toutes les valeurs dans la sélection ou la collection. L’ordre dans lequel les valeurs sont affichées n’est pas défini. Cette valeur est la valeur par défaut pour les propriétés de type = &quot; String &quot; et multipleValues = &quot; true &quot; .</td>
</tr>
<tr class="odd">
<td>Maximale</td>
<td>Affiche la valeur maximale dans la collection. Utile pour les propriétés telles que System. DateModified. Non compatible avec les types non numériques ou non-date.</td>
</tr>
<tr class="even">
<td>Minimum</td>
<td>Affiche la valeur minimale dans la collection. Non compatible avec les types non numériques ou non-date.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>isTreeProperty</td>
<td>Public. Optionnel. La valeur par défaut est &quot;false&quot;.</td>
</tr>
<tr class="odd">
<td>isViewable</td>
<td>Public. Optionnel. La valeur par défaut est &quot;false&quot;. Spécifie si cette propriété doit être affichée à l’intention de l’utilisateur. Par exemple, l’interface utilisateur du sélecteur de colonnes affiche uniquement les propriétés qui ont isViewable = &quot; true &quot; . L’interface utilisateur est une exception pilotée par un PropList, qui affiche toujours la propriété. Si vous avez une propriété qui est uniquement destinée à passer des données entre deux objets et qui ne sont jamais destinées à être consultées par l’utilisateur, cet attribut doit avoir la valeur false. Cette valeur correspond à l’indicateur de PDTF_ISVIEWABLE défini dans <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> et utilisé dans <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription :: GetTypeFlags</strong></a>.</td>
</tr>
<tr class="even">
<td>isQueryable</td>
<td>Windows Vista uniquement. Non pris en charge dans Windows 7 et versions ultérieures. Public. Optionnel. La valeur par défaut est &quot;false&quot;. Spécifie si cette propriété doit être disponible dans l’interface utilisateur de recherche Générateur de requêtes. Une propriété doit avoir isViewable = &quot; true &quot; avant que isQueryable = &quot; true &quot; soit respecté. Cette valeur correspond à l’indicateur de PDTF_ISQUERYABLE défini dans <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> et utilisé dans <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription :: GetTypeFlags</strong></a>.</td>
</tr>
<tr class="odd">
<td>searchRawValue</td>
<td><strong>Windows 7 et versions ultérieures.</strong> Public. Optionnel. La valeur par défaut est &quot;false&quot;.</td>
</tr>
<tr class="even">
<td>includeInFullTextQuery</td>
<td>Windows Vista uniquement. Non pris en charge dans Windows 7 et versions ultérieures. Public. Optionnel. La valeur par défaut est &quot;false&quot;.</td>
</tr>
<tr class="odd">
<td>conditionType</td>
<td>Public. Optionnel. La valeur par défaut est &quot; String &quot; . Spécifie un indicateur pour la recherche Générateur de requêtes l’interface utilisateur afin qu’elle puisse déterminer la liste des opérateurs de condition possibles à l’intérieur d’un prédicat. Les valeurs reconnues sont les suivantes. 
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
<td>Par défaut. Les opérateurs suivants seront utilisés : &quot; est &quot; , n' &quot; est pas &quot; , &quot; &lt; &quot; ,, &quot; &gt; &quot; &quot; <= &quot; , &quot; >= &quot; , &quot; commence par &quot; , et &quot; se termine par &quot; , &quot; contient &quot; , &quot; ne contient pas &quot; , &quot; est comme &quot; .</td>
</tr>
<tr class="even">
<td>Number</td>
<td>Valeur par défaut pour les propriétés numériques. Les opérateurs suivants seront utilisés : égal à, n' &quot; &quot; est pas égal à, est inférieur à &quot; &quot; &quot; &quot; , &quot; est supérieur à &quot; , &quot; est inférieur ou égal à &quot; , &quot; est supérieur ou égal à &quot; .</td>
</tr>
<tr class="odd">
<td>DateTime</td>
<td>Valeur par défaut pour les propriétés de type = &quot; DateTime &quot; . Les opérateurs suivants seront utilisés : &quot; est, n’est &quot; &quot; pas &quot; , est &quot; avant &quot; , est &quot; après &quot; , &quot; est avant, mais comprend &quot; , &quot; est après, mais contient &quot; .</td>
</tr>
<tr class="even">
<td>Boolean</td>
<td>Valeur par défaut pour les propriétés de type = &quot; Boolean &quot; . Identique au nombre.</td>
</tr>
<tr class="odd">
<td>Taille</td>
<td>Identique au nombre.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>defaultOperation</td>
<td>Public. Optionnel. La valeur par défaut est &quot; égale à &quot; . Spécifie un indicateur pour l’outil de Générateur de requêtes de recherche afin qu’il puisse déterminer l’opérateur par défaut. Les valeurs possibles sont les suivantes :

<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Égal à</td>
<td>Par défaut. Indique un équivalent.</td>
</tr>
<tr class="even">
<td>NotEqual</td>
<td>N’indique pas l’équivalent.</td>
</tr>
<tr class="odd">
<td>LessThan</td>
<td>Indique inférieur à.</td>
</tr>
<tr class="even">
<td>GreaterThan</td>
<td>Valeur par défaut pour les propriétés de conditionType = &quot; size &quot; . Indique supérieur à.</td>
</tr>
<tr class="odd">
<td>Contient</td>
<td>Valeur par défaut pour les propriétés de conditionType = &quot; String &quot; . Indique l’inclusion.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
