---
description: L' <property> élément spécifie une propriété utilisée par la bibliothèque. Ces propriétés étant spécifiques à la bibliothèque, il n’existe aucun ensemble prédéfini de noms de propriétés à utiliser. Cet élément est facultatif et n’a pas d’éléments enfants.
ms.assetid: 8BF6EC7A-A87E-45fe-A8F0-4B49594E9E7B
title: Property, élément (schéma de bibliothèque)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b269e8914cf1f5da92d96e1922f7347a161daf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991105"
---
# <a name="property-element-library-schema"></a>Property, élément (schéma de bibliothèque)

L' <property> élément spécifie une propriété utilisée par la bibliothèque. Ces propriétés étant spécifiques à la bibliothèque, il n’existe aucun ensemble prédéfini de noms de propriétés à utiliser. Cet élément est facultatif et n’a pas d’éléments enfants.

## <a name="syntax"></a>Syntaxe

``` syntax
<!-- property -->
<xs:element name="property" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension base="xs:anyType">
                <xs:attribute name="name" type="canonical-name" use="required"/>
                    <xs:simpleType name="canonical-name">
                        <xs:restriction base="xs:string">
                            <xs:maxLength value="63"/>
                            <xs:pattern value="[0-9A-Za-z.]*"/>
                        </xs:restriction>
                    </xs:simpleType>
                <xs:attribute name="type"/>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                                             | Éléments enfants |
|----------------------------------------------------------------------------|----------------|
| [Élément propertyStore (schéma de bibliothèque)](schema-library-propertystore.md) | Aucun           |



 

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

</tr>
<tr class="even">
<td>type</td>
<td>Public. Obligatoire. Type de propriété.</td>
<td><ul>
<li>Any : valeur par défaut. La valeur ne sera pas forcée par le sous-système de propriété. VT_NULL est retourné par GetPropertyType.</li>
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
<li>UInt64 : la valeur doit être un VT_UI8.</li>
<li>Double : la valeur doit être un VT_R8.</li>
<li>DateTime : la valeur doit être un VT_FILETIME.</li>
<li>GUID : la valeur doit être un VT_CLSID.</li>
<li>Objet BLOB : la valeur doit être un VT_BLOB.</li>
<li>Objet : la valeur doit être un VT_UNKNOWN.</li>
<li>Stream : la valeur doit être un VT_STREAM.</li>
<li>Presse-papiers : la valeur doit être un VT_CF.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Notes

La configuration requise pour l’élément <nom canonique> correspond à la configuration requise pour Windows Search et le système de propriétés Windows. La chaîne doit être de type canonique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Schéma de description de la bibliothèque](library-schema-entry.md)
</dt> <dt>

[Schémas de propriété](../properties/building-property-handlers-property-schemas.md)
</dt> <dt>

[Schéma de la description du connecteur de recherche](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
