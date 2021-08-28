---
description: L' &lt; &gt; élément scopeItem représente une entrée unique dans la table d’étendue d’exclusion/d’inclusion.
ms.assetid: 18a58b3b-771c-4829-b3d4-253383b4bee8
title: Élément scopeItem (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a585acd065efcbc58091d4c8bebce733ed2c73
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880446"
---
# <a name="scopeitem-element-search-connector-schema"></a>Élément scopeItem (schéma du connecteur de recherche)

L' &lt; &gt; élément scopeItem représente une entrée unique dans la table d’étendue d’exclusion/d’inclusion. &lt;scopeItem &gt; étend le type shellLinkType standard en ajoutant trois nouveaux éléments qui contrôlent l’inclusion et l’exclusion de dossiers, contrôlent la profondeur des résultats et spécifient l’emplacement de l’étendue. Si l' &lt; &gt; élément Scope existe, cet élément est obligatoire. Il a trois éléments enfants et aucun attribut.

## <a name="syntax"></a>Syntaxe


```
<!-- scopeItem -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                <xs:element name="mode" default="Include">
                                    ...
                                </xs:element>
                                <xs:element name="depth" default="Shallow" minOccurs="0">
                                    ...
                                </xs:element>
                                <xs:element name="url" type="xs:anyURI"/>
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



| Élément parent                                                           | Éléments enfants                                                                        |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Élément Scope (schéma du connecteur de recherche)](search-schema-sconn-scope.md) | [élément Scope (schéma du connecteur de recherche)](search-schema-sconn-scope-mode.md).        |
|                                                                          | [élément Scope (schéma du connecteur de recherche)](search-schema-sconn-scope-depth.md).       |
|                                                                          | [élément URL scopeItem (schéma du connecteur de recherche)](search-schema-sconn-scope-url.md). |



 

## <a name="remarks"></a>Remarques

Utilisez les &lt; &gt; éléments Scope et &lt; scopeItem &gt; pour identifier les emplacements à rechercher et les emplacements qui doivent être exclus de la recherche.

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



 

 



