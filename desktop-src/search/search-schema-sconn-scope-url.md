---
description: L' &lt; &gt; élément URL spécifie une URL qui représente l’étendue du connecteur de recherche. Cet élément n’a pas d’éléments enfants ni d’attributs.
ms.assetid: 5afd84aa-98e3-4118-845a-d4efad19a488
title: Élément URL scopeItem (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a1db669f7365f04bed49c769ab695ab674b20b
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886710"
---
# <a name="scopeitem-url-element-search-connector-schema"></a>Élément URL scopeItem (schéma du connecteur de recherche)

L' &lt; &gt; élément URL spécifie une URL qui représente l’étendue du connecteur de recherche. Cet élément n’a pas d’éléments enfants ni d’attributs.

## <a name="syntax"></a>Syntaxe


```
<!-- url -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0"><xs:all>
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                ...
                                <xs:element name="url" type="xs:anyURI"/>
                            </xs:all>
                        </xs:complexType>
                    </xs:element>
                </xs:sequence></xs:all>
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

La valeur peut être un chemin d’accès au système de fichiers local ou une URL.

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
            <mode>Exclude</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



