---
description: L' <locationProvider> élément facultatif spécifie le moteur de recherche que le connecteur de recherche de fournisseur de services Web doit utiliser. Cet élément contient un attribut obligatoire et un élément enfant facultatif.
ms.assetid: 5481b1ae-e166-4f09-bf0d-d6b7f7c8a331
title: Élément locationProvider (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26c68732300c190b44b984bbe64ca031a81ced84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516213"
---
# <a name="locationprovider-element-search-connector-schema"></a>Élément locationProvider (schéma du connecteur de recherche)

L' <locationProvider> élément facultatif spécifie le moteur de recherche que le connecteur de recherche de fournisseur de services Web doit utiliser. Cet élément contient un attribut obligatoire et un élément enfant facultatif.

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
| CodeBase  | Optionnel.                                                      |



 

## <a name="remarks"></a>Notes

La @clsid valeur de l’attribut pour le fournisseur OpenSearch est {48E277F6-4E74-4CD6-BA6F-FA4F42898223}.

Les connecteurs de recherche basés sur le système de fichiers et le gestionnaire de protocole peuvent utiliser l’élément à la [<simpleLocation>](search-schema-sconn-simplelocation.md) place. Si <locationProvider> est présent, il ne doit pas y avoir <simpleLocation> d’élément dans la description de la recherche de connecteur.

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



 

 



