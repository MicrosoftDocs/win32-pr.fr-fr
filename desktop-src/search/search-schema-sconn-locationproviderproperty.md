---
description: L' &lt; élément facultatif Property &gt; spécifie les propriétés utilisées par le fournisseur de localisation.
ms.assetid: c1120dea-cb0b-4746-a5c1-4c83cda6dd7c
title: Élément Property de locationProvider (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad478fd1d1c00ad5c7f866831cdfdf898557546b
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883336"
---
# <a name="property-element-of-locationprovider-search-connector-schema"></a>Élément Property de locationProvider (schéma du connecteur de recherche)

L' &lt; élément facultatif Property &gt; spécifie les propriétés utilisées par le fournisseur de localisation. Ces propriétés étant spécifiques à ce fournisseur de localisation, il n’existe aucun ensemble prédéfini de noms à utiliser. L' &lt; &gt; élément Property a deux attributs, comme décrit dans cette rubrique.

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



## <a name="ltpropertygt-element-information"></a>&lt;&gt;informations sur les éléments de propriété



| Élément parent                                                                                 | Éléments enfants                     |
|------------------------------------------------------------------------------------------------|------------------------------------|
| [Élément locationProvider (schéma du connecteur de recherche)](search-schema-sconn-locationprovider.md) | , décrite dans cette rubrique. |



 


## <a name="ltpropertygt-attributes"></a>&lt;attributs de propriété &gt;




| Attribut | Description | Valeurs | 
|-----------|-------------|--------|
| name | Obligatoire. Le nom complet de la propriété. |   | 
| type | Obligatoire. Type de propriété. | Any : valeur par défaut. La valeur ne sera pas forcée par le sous-système de propriété. VT_NULL est retourné par GetPropertyType.<ul><li>NULL : il n’y a aucune valeur pour cette propriété. VT_NULL est retourné par GetPropertyType.</li><li>Chaîne : la valeur doit être un VT_LPWSTR.</li><li>Booléen : la valeur doit être un VT_BOOL.</li><li>Byte : la valeur doit être un VT_UI1.</li><li>Buffer : la valeur doit être un VT_UI1 | Mémoire tampon d’octets VT_VECTOR.</li><li>Int16 : la valeur doit être un VT_I2.</li><li>UInt16 : la valeur doit être un VT_UI2.</li><li>Int32 : la valeur doit être un VT_I4.</li><li>UInt32 : la valeur doit être un VT_UI4.</li><li>Int64 : la valeur doit être un VT_I8.</li><li>UInt64 : la valeur doit être un VT_UI8</li><li>Double : la valeur doit être un VT_R8.</li><li>DateTime : la valeur doit être un VT_FILETIME.</li><li>GUID : la valeur doit être un VT_CLSID.</li><li>Objet BLOB : la valeur doit être un VT_BLOB.</li><li>Objet : la valeur doit être un VT_UNKNOWN.</li><li>Stream : la valeur doit être un VT_STREAM.</li><li>Presse-papiers : la valeur doit être un VT_CF.</li></ul> | 




 

## <a name="remarks"></a>Remarques

pour le fournisseur OpenSearch, les propriétés suivantes sont utilisées :

-   OpenSearchShortName : nom abrégé du service de recherche
-   OpenSearchQueryTemplate : modèle, mis en forme selon la convention de modèle OpenSearch, pour le service de requête
-   MaximumResultCount : (Number) nombre maximal de résultats retournés par le service de recherche
-   LinkIsFilePath : (booléen) si la valeur est true, le fournisseur tente d’interpréter les éléments retournés en tant que fichiers, en utilisant leurs extensions pour créer le ShellItem approprié dans la vue. Si la valeur est false, les éléments sont traités comme des raccourcis d’URL.

 

 



