---
description: L' <mode> élément spécifie si l’URL doit être incluse ou exclue de l’étendue du connecteur de recherche. Les valeurs autorisées sont include et Exclude. Cet élément n’a pas d’éléments enfants ni d’attributs.
ms.assetid: 7654c04a-31c4-4260-a51c-0600804e62a9
title: mode, élément (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a210abf5c9c2bbc4cd5d53978866a729d834928cf39e54bfb6e6fcc9c42c7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944319"
---
# <a name="mode-element-search-connector-schema"></a>mode, élément (schéma du connecteur de recherche)

L' <mode> élément spécifie si l’URL doit être incluse ou exclue de l’étendue du connecteur de recherche. Les valeurs autorisées sont `Include` et `Exclude`. Cet élément n’a pas d’éléments enfants ni d’attributs.

## <a name="syntax"></a>Syntaxe


```
<!-- mode -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                ...
                                <xs:element name="mode" default="Include">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Include"/>
                                            <xs:enumeration value="Exclude"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                </xs:element>
                                ...
                            </xs:all>
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                                                   | Éléments enfants |
|----------------------------------------------------------------------------------|----------------|
| [Élément scopeItem (schéma du connecteur de recherche)](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a>Remarques

Une étendue exclue ne peut pas être recherchée ou parcourue. Vous pouvez imbriquer des URL scopeItem. Par exemple, vous pouvez inclure une étendue parente et tous ses enfants à l’exception d’un en ajoutant l’URL parente telle qu’elle est incluse, avec une valeur de profondeur de profondeur et en excluant l’URL enfant.

## <a name="example"></a>Exemple

L’exemple suivant montre une étendue de recherche qui comprend C : \\ ExampleFolder et tous ses dossiers enfants, à l’exception de c : \\ ExampleFolder \\ ExcludeMe.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder</url>
        </scopeItem>
        <scopeItem>
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



