---
description: L' <property> élément facultatif spécifie les propriétés utilisées par le fournisseur de localisation.
ms.assetid: c1120dea-cb0b-4746-a5c1-4c83cda6dd7c
title: Élément Property de locationProvider (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71081b8b04ec999daa90958a29708b8efc64bee0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "106539849"
---
# <a name="property-element-of-locationprovider-search-connector-schema"></a>Élément Property de locationProvider (schéma du connecteur de recherche)

L' <property> élément facultatif spécifie les propriétés utilisées par le fournisseur de localisation. Ces propriétés étant spécifiques à ce fournisseur de localisation, il n’existe aucun ensemble prédéfini de noms à utiliser. L' <property> élément a deux attributs, comme décrit dans cette rubrique.

## <a name="syntax"></a>Syntaxe


```
<!-- property element -->
    <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
        <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
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



## <a name="property-element-information"></a><property> Informations sur l’élément



| Élément parent                                                                                 | Éléments enfants                     |
|------------------------------------------------------------------------------------------------|------------------------------------|
| [Élément locationProvider (schéma du connecteur de recherche)](search-schema-sconn-locationprovider.md) | , décrite dans cette rubrique. |



 


## <a name="property-attributes"></a><property> Attributs



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
<td>Obligatoire. Le nom complet de la propriété.</td>
<td> </td>
</tr>
<tr class="even">
<td>type</td>
<td>Obligatoire. Type de propriété.</td>
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
</tbody>
</table>



 

## <a name="remarks"></a>Notes

Pour le fournisseur OpenSearch, les propriétés suivantes sont utilisées :

-   OpenSearchShortName : nom abrégé du service de recherche
-   OpenSearchQueryTemplate : modèle, mis en forme selon la Convention de modèle OpenSearch, pour le service de requête
-   MaximumResultCount : (Number) nombre maximal de résultats retournés par le service de recherche
-   LinkIsFilePath : (booléen) si la valeur est true, le fournisseur tente d’interpréter les éléments retournés en tant que fichiers, en utilisant leurs extensions pour créer le ShellItem approprié dans la vue. Si la valeur est false, les éléments sont traités comme des raccourcis d’URL.

 

 



