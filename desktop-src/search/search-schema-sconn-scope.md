---
description: L' &lt; élément Scope facultatif &gt; spécifie une collection &lt; d' &gt; éléments scopeItem qui définissent les inclusions et les exclusions de portée pour ce connecteur de recherche particulier.
ms.assetid: 9e92e3db-3d5e-4f86-8d67-90eb5469b04b
title: Élément Scope (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80c011eee8def80a7f1d395a7a52a72d30fb4935
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886697"
---
# <a name="scope-element-search-connector-schema"></a>Élément Scope (schéma du connecteur de recherche)

L' &lt; élément Scope facultatif &gt; spécifie une collection &lt; d' &gt; éléments scopeItem qui définissent les inclusions et les exclusions de portée pour ce connecteur de recherche particulier. Si &lt; Scope &gt; est présent, il doit contenir au moins un &lt; &gt; élément scopeItem. Cet élément n’a pas d’attributs.

## <a name="syntax"></a>Syntaxe


```
<!-- scope -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                       ...
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



| Élément parent                                                                                                   | Éléments enfants                                                                    |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Élément searchConnectorDescriptionType (schéma du connecteur de recherche)](search-schema-searchconnectordescription.md) | [élément scopeItem (schéma du connecteur de recherche)](search-schema-sconn-scopeitem.md). |



 

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



 

 



