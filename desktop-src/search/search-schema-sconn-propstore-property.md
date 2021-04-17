---
description: L' <property> élément facultatif spécifie une propriété utilisée par le connecteur de recherche. Ces propriétés étant spécifiques à ce connecteur de recherche, il n’existe aucun ensemble prédéfini de noms à utiliser. Cet élément n’a pas d’éléments enfants.
ms.assetid: 33854123-d4c0-4385-910b-a32d6922423f
title: Élément Property de propertyStore (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2e4cee6f26ee65ba03d9225eafcea4a03a7c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525450"
---
# <a name="property-element-of-propertystore-search-connector-schema"></a>Élément Property de propertyStore (schéma du connecteur de recherche)

L' <property> élément facultatif spécifie une propriété utilisée par le connecteur de recherche. Ces propriétés étant spécifiques à ce connecteur de recherche, il n’existe aucun ensemble prédéfini de noms à utiliser. Cet élément n’a pas d’éléments enfants.

## <a name="syntax"></a>Syntaxe


```
<!-- property for propertyStore element -->
    <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
        <xs:element name="property" minOccurs="0" maxOccurrs="unbounded">
            <xs:complexType>
                <xs:complexContent>
                    <xs:extension base="xs:anyType">
                        <xs:attribute name="name" type="canonical-name" use="required"/>
                        <xs:attribute name="type"/>
                    </xs:extension>
                </xs:complexContent>
            </xs:complexType>
        </xs:element>
    </xs:element>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                                                           | Éléments enfants |
|------------------------------------------------------------------------------------------|----------------|
| [Élément propertyStore (schéma du connecteur de recherche)](search-schema-sconn-propertystore.md) |                |



 

## <a name="attributes"></a>Attributs



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Description</th>
<th>Valeurs</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>name</td>
<td>Public. Obligatoire. Le nom complet de la propriété.</td>
<td> </td>
</tr>
<tr class="even">
<td>type</td>
<td>Public. Obligatoire. Type de propriété.</td>
<td>Any : valeur par défaut. La valeur ne sera pas forcée par le sous-système de propriété. VT_NULL est retourné par GetPropertyType.
<ul>
<li>NULL : il n’y a aucune valeur pour cette propriété. VT_NULL est retourné par GetPropertyType.</li>
<li>Chaîne : la valeur doit être un VT_LPWSTR.</li>
<li>Booléen : la valeur doit être un VT_BOOL.</li>
<li>Byte : la valeur doit être un VT_UI1.</li>
<li>Buffer : la valeur doit être un VT_UI1 | Mémoire tampon d’octets VT_VECTOR.</li>
<li>Int16 : la valeur doit être un VT_I2.</li>
<li>UInt16 : la valeur doit être un VT_UI2.</li>
<li>Int32 : la valeur doit être un VT_I4.</li>
<li>UInt32 : la valeur doit être un VT_UI4.</li>
<li>Int64 : la valeur doit être un VT_I8.</li>
<li>UInt64 : la valeur doit être un VT_UI8</li>
<li>Double : la valeur doit être un VT_R8.</li>
<li>DateTime : la valeur doit être un VT_FILETIME.</li>
<li>GUID : la valeur doit être un VT_CLSID.</li>
<li>Objet BLOB : la valeur doit être un VT_BLOB.</li>
<li>Objet : la valeur doit être un VT_UNKNOWN.</li>
<li>Stream : la valeur doit être un VT_STREAM.</li>
<li>Presse-papiers : la valeur doit être un VT_CF.</li>
</ul></td>
</tr>
<tr class="odd">
<td>schéma</td>
<td>Public. Optionnel. Schéma dans lequel la propriété est définie.</td>
<td> </td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Notes

Les connecteurs de recherche OpenSearch peuvent utiliser la propriété OpenSearchHTMLRolloverTemplate. Cette propriété identifie un modèle mis en forme selon la Convention de modèle OpenSearch. Le modèle OpenSearchHTMLRolloverTemplate est utilisé lorsque l’utilisateur clique sur le bouton « Rechercher sur le site Web » dans la barre de commandes.

## <a name="example"></a>Exemple

L’exemple suivant illustre un <propertyStore> élément avec deux <property> éléments.


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



