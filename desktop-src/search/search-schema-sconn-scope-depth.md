---
description: L' &lt; &gt; élément Depth spécifie si la portée du connecteur de recherche doit inclure des URL enfants. Les valeurs autorisées sont Deep et Shallow. Cet élément n’a pas d’éléments enfants ni d’attributs.
ms.assetid: 859decab-cbe3-4cec-b37c-6d0e7c353876
title: Élément Depth (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 430ad3d047331a4bb3ffc58bd134d2364aaa0838
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886762"
---
# <a name="depth-element-search-connector-schema"></a>Élément Depth (schéma du connecteur de recherche)

L' &lt; &gt; élément Depth spécifie si la portée du connecteur de recherche doit inclure des URL enfants. Les valeurs autorisées sont `Deep` et `Shallow`. Cet élément n’a pas d’éléments enfants ni d’attributs.

## <a name="syntax"></a>Syntaxe


```
<!-- depth -->
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
                                <xs:element name="depth" default="Shallow" minOccurs="0">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Shallow"/>
                                            <xs:enumeration value="Deep"/>
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

Si la profondeur est profonde, les utilisateurs peuvent parcourir ou Rechercher des éléments dans le niveau d’URL de scopeItem ou dans des URL enfants.

## <a name="example"></a>Exemple

L’exemple suivant montre une étendue de recherche qui comprend C : \\ dossier et tous ses dossiers enfants et c : \\ FolderB, mais aucun de ses dossiers enfants.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\FolderA</url>
        </scopeItem>
        <scopeItem>
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\FolderB</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



