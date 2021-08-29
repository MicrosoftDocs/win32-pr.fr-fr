---
description: L' &lt; élément booléen supportsAdvancedQuerySyntax &gt; spécifie si le moteur de recherche prend en charge la syntaxe de requête avancée. La valeur par défaut est false. Cet élément est facultatif et n’a pas d’éléments enfants ni d’attributs.
ms.assetid: d4aef1f1-63c8-4e9a-9e22-5efbb8c523b2
title: Élément supportsAdvancedQuerySyntax (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 432c6917ccf03ddf4a00f30029e01b9075309c65
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880438"
---
# <a name="supportsadvancedquerysyntax-element-search-connector-schema"></a>Élément supportsAdvancedQuerySyntax (schéma du connecteur de recherche)

L' &lt; élément booléen supportsAdvancedQuerySyntax &gt; spécifie si le moteur de recherche prend en charge la [syntaxe de requête avancée](-search-3x-advancedquerysyntax.md). La valeur par défaut est false. Cet élément est facultatif et n’a pas d’éléments enfants ni d’attributs.

## <a name="syntax"></a>Syntaxe


```
<!-- supportsAdvancedQuerySyntax -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="supportsAdvancedQuerySyntax" type="xs:boolean" default="false" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                                                                                   | Éléments enfants |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [Élément searchConnectorDescriptionType (schéma du connecteur de recherche)](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a>Remarques

La valeur `true` indique que le moteur de recherche prend en charge la syntaxe de requête avancée envoyée dans les requêtes de recherche.

## <a name="example"></a>Exemple


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <supportsAdvancedQuerySyntax>true</supportsAdvancedQuerySyntax>
    ...
</searchConnectionDescription>
```



 

 



