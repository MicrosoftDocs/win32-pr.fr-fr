---
description: L' <libraryDescription> élément est le conteneur de niveau supérieur pour la définition de la bibliothèque. Cet élément est obligatoire.
ms.assetid: 62098944-E1B2-46e8-AC87-314C55F96B62
title: Élément libraryDescription (schéma de bibliothèque)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 125cb01ce1bd38418c10f5b14ff7b28f64efba87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972294"
---
# <a name="librarydescription-element-library-schema"></a><span data-ttu-id="2b9f1-104">Élément libraryDescription (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="2b9f1-104">libraryDescription Element (Library Schema)</span></span>

<span data-ttu-id="2b9f1-105">L' <libraryDescription> élément est le conteneur de niveau supérieur pour la définition de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="2b9f1-105">The <libraryDescription> element is the top-level container for the library definition.</span></span> <span data-ttu-id="2b9f1-106">Cet élément est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="2b9f1-106">This element is required.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b9f1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b9f1-107">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="2b9f1-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="2b9f1-108">Element Information</span></span>



| <span data-ttu-id="2b9f1-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="2b9f1-109">Parent element</span></span> | <span data-ttu-id="2b9f1-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2b9f1-110">Child elements</span></span>                                                                                                          |
|----------------|-------------------------------------------------------------------------------------------------------------------------|
|                | <span data-ttu-id="2b9f1-111">[élément Name (schéma de bibliothèque)](schema-library-name.md).</span><span class="sxs-lookup"><span data-stu-id="2b9f1-111">[name Element (Library Schema)](schema-library-name.md).</span></span> <span data-ttu-id="2b9f1-112">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="2b9f1-112">Required.</span></span>                                                     |
|                | <span data-ttu-id="2b9f1-113">[élément ownerSID (schéma de bibliothèque)](schema-library-ownersid.md).</span><span class="sxs-lookup"><span data-stu-id="2b9f1-113">[ownerSID Element (Library Schema)](schema-library-ownersid.md).</span></span> <span data-ttu-id="2b9f1-114">facultatif.</span><span class="sxs-lookup"><span data-stu-id="2b9f1-114">Optional.</span></span>                                             |
|                | <span data-ttu-id="2b9f1-115">[version, élément (schéma de bibliothèque)](schema-library-version.md).</span><span class="sxs-lookup"><span data-stu-id="2b9f1-115">[version Element (Library Schema)](schema-library-version.md).</span></span> <span data-ttu-id="2b9f1-116">facultatif.</span><span class="sxs-lookup"><span data-stu-id="2b9f1-116">Optional.</span></span>                                               |
|                | <span data-ttu-id="2b9f1-117">[élément isLibraryPinned (schéma de bibliothèque)](schema-library-islibrarypinned.md).</span><span class="sxs-lookup"><span data-stu-id="2b9f1-117">[isLibraryPinned Element (Library Schema)](schema-library-islibrarypinned.md).</span></span> <span data-ttu-id="2b9f1-118">facultatif.</span><span class="sxs-lookup"><span data-stu-id="2b9f1-118">Optional.</span></span>                               |
|                | <span data-ttu-id="2b9f1-119">[élément iconReference (schéma de bibliothèque)](schema-library-iconreference.md).</span><span class="sxs-lookup"><span data-stu-id="2b9f1-119">[iconReference Element (Library Schema)](schema-library-iconreference.md).</span></span> <span data-ttu-id="2b9f1-120">facultatif.</span><span class="sxs-lookup"><span data-stu-id="2b9f1-120">Optional.</span></span>                                   |
|                | <span data-ttu-id="2b9f1-121">[élément propertyStore (schéma de bibliothèque)](schema-library-propertystore.md).</span><span class="sxs-lookup"><span data-stu-id="2b9f1-121">[propertyStore Element (Library Schema)](schema-library-propertystore.md).</span></span> <span data-ttu-id="2b9f1-122">facultatif.</span><span class="sxs-lookup"><span data-stu-id="2b9f1-122">Optional.</span></span>                                   |
|                | <span data-ttu-id="2b9f1-123">[élément templateInfo (schéma de bibliothèque)](schema-library-templateinfo.md).</span><span class="sxs-lookup"><span data-stu-id="2b9f1-123">[templateInfo Element (Library Schema)](schema-library-templateinfo.md).</span></span> <span data-ttu-id="2b9f1-124">facultatif.</span><span class="sxs-lookup"><span data-stu-id="2b9f1-124">Optional.</span></span>                                     |
|                | <span data-ttu-id="2b9f1-125">[élément searchConnectorDescriptionList (schéma de bibliothèque)](schema-library-searchconnectordescriptionlist.md).</span><span class="sxs-lookup"><span data-stu-id="2b9f1-125">[searchConnectorDescriptionList Element (Library Schema)](schema-library-searchconnectordescriptionlist.md).</span></span> <span data-ttu-id="2b9f1-126">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="2b9f1-126">Required.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2b9f1-127">Notes</span><span class="sxs-lookup"><span data-stu-id="2b9f1-127">Remarks</span></span>

<span data-ttu-id="2b9f1-128">Chaque bibliothèque peut contenir un ou plusieurs emplacements qui peuvent être explorés ou recherchés par un utilisateur à l’aide de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="2b9f1-128">Each library can contain one or more locations that can be browsed or searched by a user using Windows Explorer.</span></span> <span data-ttu-id="2b9f1-129">Les emplacements sont définis par des connecteurs de recherche utilisant [<searchConnectorDescription>](schema-library-searchconnectordescription.md) des éléments dans un [<searchConnectorDescriptionList>](schema-library-searchconnectordescriptionlist.md) élément conteneur.</span><span class="sxs-lookup"><span data-stu-id="2b9f1-129">The locations are defined by search connectors using [<searchConnectorDescription>](schema-library-searchconnectordescription.md) elements in a [<searchConnectorDescriptionList>](schema-library-searchconnectordescriptionlist.md) container element.</span></span>

<span data-ttu-id="2b9f1-130">Une bibliothèque peut avoir un ensemble unique de propriétés, et les emplacements de la bibliothèque peuvent également avoir des ensembles de propriétés uniques.</span><span class="sxs-lookup"><span data-stu-id="2b9f1-130">A library can have a unique set of properties, and locations in the library can also have unique sets of properties.</span></span> <span data-ttu-id="2b9f1-131">Ces propriétés sont définies dans les [<property>](schema-library-property.md) éléments d’un [<propertyStore>](schema-library-propertystore.md) élément conteneur.</span><span class="sxs-lookup"><span data-stu-id="2b9f1-131">These properties are defined in [<property>](schema-library-property.md) elements within a [<propertyStore>](schema-library-propertystore.md) container element.</span></span>

## <a name="example"></a><span data-ttu-id="2b9f1-132">Exemple</span><span class="sxs-lookup"><span data-stu-id="2b9f1-132">Example</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="2b9f1-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2b9f1-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b9f1-134">Schéma de description de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2b9f1-134">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="2b9f1-135">Schéma de la description du connecteur de recherche</span><span class="sxs-lookup"><span data-stu-id="2b9f1-135">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
