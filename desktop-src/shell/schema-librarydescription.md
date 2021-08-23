---
description: L' <libraryDescription> élément est le conteneur de niveau supérieur pour la définition de la bibliothèque. Cet élément est obligatoire.
ms.assetid: 62098944-E1B2-46e8-AC87-314C55F96B62
title: Élément libraryDescription (schéma de bibliothèque)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a454321649746dc9408110e2fb96a616934977022ac80a4c0325494d354bfb46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942059"
---
# <a name="librarydescription-element-library-schema"></a>Élément libraryDescription (schéma de bibliothèque)

L' <libraryDescription> élément est le conteneur de niveau supérieur pour la définition de la bibliothèque. Cet élément est obligatoire.

## <a name="syntax"></a>Syntaxe


```
<!-- libraryDescription -->
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema" elementFormDefault="qualified" attributeFormDefault="unqualified">
    <xs:include schemaLocation="commonTypes-ms.xsd"/>
    <xs:element name="libraryDescription">
        <xs:complexType>
            <xs:all>
                <xs:element name="name" type="xs:string"/>
                <xs:element name="ownerSID" minOccurs="0"/>
                <xs:element name="version" type="xs:int" minOccurs="0"/>
                <xs:element name="isLibraryPinned" type="xs:boolean" default="false" minOccurs="0"/>
                <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
                <xs:element name="propertyStore" minOccurs="0">
                    <xs:complexType>
                        <xs:complexContent>
                            <xs:extension base="propertyStoreType"/>
                        </xs:complexContent>
                    </xs:complexType>
                </xs:element>
                <xs:element name="templateInfo" minOccurs="0">
                    <xs:complexType>
                        <xs:all>
                            <xs:element name="folderType" minOccurs="0"/>
                        </xs:all>
                    </xs:complexType>
                </xs:element>
                <xs:element name="searchConnectorDescriptionList" minOccurs="0">
                    <xs:complexType>
                        <xs:sequence minOccurs="0">
                            <xs:element name="searchConnectorDescription" 
                             type="searchConnectorDescriptionType" minOccurs="0" 
                             maxOccurs="unbounded"/>
                        </xs:sequence>
                    </xs:complexType>
                </xs:element>
            </xs:all>
        </xs:complexType>
    </xs:element>
</xs:schema>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent | Éléments enfants                                                                                                          |
|----------------|-------------------------------------------------------------------------------------------------------------------------|
|                | [élément Name (schéma de bibliothèque)](schema-library-name.md). Obligatoire.                                                     |
|                | [élément ownerSID (schéma de bibliothèque)](schema-library-ownersid.md). Facultatif.                                             |
|                | [version, élément (schéma de bibliothèque)](schema-library-version.md). Facultatif.                                               |
|                | [élément isLibraryPinned (schéma de bibliothèque)](schema-library-islibrarypinned.md). Facultatif.                               |
|                | [élément iconReference (schéma de bibliothèque)](schema-library-iconreference.md). Facultatif.                                   |
|                | [élément propertyStore (schéma de bibliothèque)](schema-library-propertystore.md). Facultatif.                                   |
|                | [élément templateInfo (schéma de bibliothèque)](schema-library-templateinfo.md). Facultatif.                                     |
|                | [élément searchConnectorDescriptionList (schéma de bibliothèque)](schema-library-searchconnectordescriptionlist.md). Obligatoire. |



 

## <a name="remarks"></a>Remarques

chaque bibliothèque peut contenir un ou plusieurs emplacements qui peuvent être explorés ou recherchés par un utilisateur à l’aide de Windows Explorer. Les emplacements sont définis par des connecteurs de recherche utilisant [<searchConnectorDescription>](schema-library-searchconnectordescription.md) des éléments dans un [<searchConnectorDescriptionList>](schema-library-searchconnectordescriptionlist.md) élément conteneur.

Une bibliothèque peut avoir un ensemble unique de propriétés, et les emplacements de la bibliothèque peuvent également avoir des ensembles de propriétés uniques. Ces propriétés sont définies dans les [<property>](schema-library-property.md) éléments d’un [<propertyStore>](schema-library-propertystore.md) élément conteneur.

## <a name="example"></a>Exemple


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
    <name>@shell32.dll,-34575</name>
    <ownerSID>S-1-5-21-379071477-2495173225-776587366-1000</ownerSID>
    <version>1</version>
    <isLibraryPinned>true</isLibraryPinned>
    <iconReference>imageres.dll,-1002</iconReference>
    <templateInfo>
        <folderType>{7d49d726-3c21-4f05-99aa-fdc2c9474656}</folderType>
    </templateInfo>
    <searchConnectorDescriptionList>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34577</description>
            <isDefaultSaveLocation>true</isDefaultSaveLocation>
            <simpleLocation>
                <url>knownfolder:{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</url>
                <serialized>MBAAAEAFCAAA...MFNVAAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34579</description>
            <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
            <simpleLocation>
                <url>knownfolder:{ED4824AF-DCE4-45A8-81E2-FC7965083634}</url>
                <serialized>MBAAAEAFCAAA...HJIfK9AAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
    </searchConnectorDescriptionList>
</libraryDescription>
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Schéma de description de la bibliothèque](library-schema-entry.md)
</dt> <dt>

[Schéma de la description du connecteur de recherche](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
