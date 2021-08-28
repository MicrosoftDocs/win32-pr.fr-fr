---
description: L' &lt; élément facultatif locationProvider &gt; spécifie le moteur de recherche que le connecteur de recherche de fournisseur de services Web doit utiliser. Cet élément contient un attribut obligatoire et un élément enfant facultatif.
ms.assetid: 5481b1ae-e166-4f09-bf0d-d6b7f7c8a331
title: Élément locationProvider (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f049a01cc0c51075c147918a2f43b740000f2e36
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883368"
---
# <a name="locationprovider-element-search-connector-schema"></a>Élément locationProvider (schéma du connecteur de recherche)

L' &lt; élément facultatif locationProvider &gt; spécifie le moteur de recherche que le connecteur de recherche de fournisseur de services Web doit utiliser. Cet élément contient un attribut obligatoire et un élément enfant facultatif.

## <a name="syntax"></a>Syntaxe


```
<!-- locationProvider -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="locationProvider" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0"/>
                    </xs:all>
                <xs:attribute name="clsid" use="required"/>
                <xs:attribute name="codebase" type="xs:string"/>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                                                                                   | Éléments enfants                                                                       |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Élément searchConnectorDescriptionType (schéma du connecteur de recherche)](search-schema-searchconnectordescription.md) | [propertyBag, élément (schéma du connecteur de recherche)](search-schema-sconn-propertybag.md) |



 

## <a name="attributes"></a>Attributs



| Attribut | Description                                                    |
|-----------|----------------------------------------------------------------|
| @clsid    | Obligatoire. Identificateur de classe (CLSID) du moteur de recherche. |
| CodeBase  | facultatif.                                                      |



 

## <a name="remarks"></a>Remarques

la @clsid valeur de l’attribut pour le fournisseur de OpenSearch est {48E277F6-4E74-4cd6-BA6F-FA4F42898223}.

Les connecteurs de recherche basés sur le système de fichiers et le gestionnaire de protocole peuvent utiliser l’élément [ &lt; simpleLocation &gt; ](search-schema-sconn-simplelocation.md) à la place. Si &lt; locationProvider &gt; est présent, il ne doit pas y &lt; avoir &gt; d’élément simpleLocation dans la description de la recherche de connecteur.

## <a name="example-of-a-locationprovider-element"></a>Exemple d’élément locationProvider


```
<locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
        <property name="OpenSearchShortName">MSDN</property>
        <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
        <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
</locationProvider>
```



 

 



