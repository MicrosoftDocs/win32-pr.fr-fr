---
description: L' <scope> élément facultatif spécifie une collection d' <scopeItem> éléments qui définissent les inclusions et les exclusions de portée pour ce connecteur de recherche particulier.
ms.assetid: 9e92e3db-3d5e-4f86-8d67-90eb5469b04b
title: Élément Scope (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f49041170db80de48d312596249d5c4dca835e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527185"
---
# <a name="scope-element-search-connector-schema"></a>Élément Scope (schéma du connecteur de recherche)

L' <scope> élément facultatif spécifie une collection d' <scopeItem> éléments qui définissent les inclusions et les exclusions de portée pour ce connecteur de recherche particulier. Si <scope> est présent, il doit contenir au moins un <scopeItem> élément. Cet élément n’a pas d’attributs.

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



 

## <a name="remarks"></a>Notes

Utilisez les <scope> <scopeItem> éléments et pour identifier les emplacements à rechercher et les emplacements qui doivent être exclus de la recherche.

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



 

 



