---
description: L' <supportsAdvancedQuerySyntax> élément boolean spécifie si le moteur de recherche prend en charge la syntaxe de requête avancée. La valeur par défaut est false. Cet élément est facultatif et n’a pas d’éléments enfants ni d’attributs.
ms.assetid: d4aef1f1-63c8-4e9a-9e22-5efbb8c523b2
title: Élément supportsAdvancedQuerySyntax (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8235c1021ae04cbbce65500ebf008f645ef74c1f2bb6ea7f3a9edfe4253e035
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119844509"
---
# <a name="supportsadvancedquerysyntax-element-search-connector-schema"></a>Élément supportsAdvancedQuerySyntax (schéma du connecteur de recherche)

L' <supportsAdvancedQuerySyntax> élément boolean spécifie si le moteur de recherche prend en charge la [syntaxe de requête avancée](-search-3x-advancedquerysyntax.md). La valeur par défaut est false. Cet élément est facultatif et n’a pas d’éléments enfants ni d’attributs.

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



 

 



