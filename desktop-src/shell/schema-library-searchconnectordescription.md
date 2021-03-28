---
description: L' <searchConnectorDescription> élément est l’élément conteneur de niveau supérieur d’une définition de connecteur de recherche.
ms.assetid: 383CAA20-56CA-4bdc-AC79-E57A1D59785C
title: Élément searchConnectorDescription (schéma de bibliothèque)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faa6c213d43a648ebea51b58b4c3103a0ee42f13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973607"
---
# <a name="searchconnectordescription-element-library-schema"></a><span data-ttu-id="6d12b-103">Élément searchConnectorDescription (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="6d12b-103">searchConnectorDescription Element (Library Schema)</span></span>

<span data-ttu-id="6d12b-104">L' <searchConnectorDescription> élément est l’élément conteneur de niveau supérieur d’une définition de connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="6d12b-104">The <searchConnectorDescription> element is the top level container element of a search connector definition.</span></span> <span data-ttu-id="6d12b-105">L' <searchConnectorDescription> élément est une extension du <searchConnectorDescriptionType> type d’élément associé aux connecteurs de recherche fédérée Windows. Toutefois, vous ne pouvez pas inclure de connecteurs de recherche pour la recherche Windows fédérée ou les gestionnaires de protocoles dans une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="6d12b-105">The <searchConnectorDescription> element is an extension of the <searchConnectorDescriptionType> element type associated with Windows Federated Search connectors; however, you cannot include search connectors for Windows Federated Search or protocol handlers in a library.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d12b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d12b-106">Syntax</span></span>

``` syntax
<!-- searchConnectorDescription -->
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema" elementFormDefault="qualified" attributeFormDefault="unqualified">
   <xs:complexType name="searchConnectorDescriptionType">
      <xs:all>
         <xs:element name="isSearchOnlyItem" type="xs:boolean" default="false" minOccurs="0"/>
         <xs:element name="isDefaultSaveLocation" type="xs:boolean" minOccurs="0"/>
         <xs:element name="isDefaultNonOwnerSaveLocation" type="xs:boolean" minOccurs="0"/
         <xs:element name="description" type="xs:string" minOccurs="0"/>
         <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
         <xs:element name="imageLink" minOccurs="0">
            <xs:complexType>
               <xs:sequence>
                  <xs:element name="url" type="xs:anyURI"/>
               </xs:sequence>
            </xs:complexType>
         </xs:element>
         <xs:element name="author" type="xs:string" minOccurs="0"/>
         <xs:element name="dateCreated" type="xs:dateTime" minOccurs="0"/>
         <xs:element name="templateInfo" minOccurs="0">
            <xs:complexType>
               <xs:all>
                  <xs:element name="folderType" minOccurs="0"/>
               </xs:all>
            </xs:complexType>
         </xs:element>
         <xs:element name="simpleLocation" type="shellLinkType" minOccurs="0"/>
         <xs:element name="locationProvider" minOccurs="0">
            <xs:complexType>
               <xs:all>
                  <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0"/>
               </xs:all>
               <xs:attribute name="clsid" use="required"/>
               <xs:attribute name="codebase" type="xs:string"/>
            </xs:complexType>
         </xs:element>
         <xs:element name="scope" minOccurs="0">
            <xs:complexType>
               <xs:sequence minOccurs="0">
                  <xs:element name="scopeItem" maxOccurs="unbounded">
                     <xs:complexType>
                        <xs:all>
                           <xs:element name="mode" default="Include">
                              <xs:simpleType>
                                 <xs:restriction base="xs:string">
                                    <xs:enumeration value="Include"/>
                                    <xs:enumeration value="Exclude"/>
                                 </xs:restriction>
                              </xs:simpleType>
                           </xs:element>
                           <xs:element name="depth" default="Shallow" minOccurs="0">
                              <xs:simpleType>
                                 <xs:restriction base="xs:string">
                                    <xs:enumeration value="Shallow"/>
                                    <xs:enumeration value="Deep"/>
                                 </xs:restriction>
                              </xs:simpleType>
                           </xs:element>
                           <xs:element name="url" type="xs:anyURI"/>
                        </xs:all>
                     </xs:complexType>
                  </xs:element>
               </xs:sequence>
            </xs:complexType>
         </xs:element>
         <xs:element name="propertyStore" type="propertyStoreType" minOccurs="0"/>
         <xs:element name="includeInStartMenuScope" type="xs:boolean" default="false" minOccurs="0"/>
         <xs:element name="domain" type="xs:string" minOccurs="0"/>
         <xs:element name="supportsAdvancedQuerySyntax" type="xs:boolean" default="false" minOccurs="0"/>
         <xs:element name="isIndexed" type="xs:boolean" minOccurs="0"/>
      </xs:all>
      <xs:attribute name="publisher" type="xs:string"/>
      <xs:attribute name="product" type="xs:string"/>
   </xs:complexType>
</xs:schema>
```

## <a name="element-information"></a><span data-ttu-id="6d12b-107">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="6d12b-107">Element Information</span></span>

<span data-ttu-id="6d12b-108">Reportez-vous à la documentation du schéma dans [Windows Search](/previous-versions/bb268030(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="6d12b-108">Refer to the schema documentation in [Windows Search](/previous-versions/bb268030(v=msdn.10))</span></span>



| <span data-ttu-id="6d12b-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="6d12b-109">Parent Element</span></span>                                                                                               | <span data-ttu-id="6d12b-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6d12b-110">Child Elements</span></span>                        |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [<span data-ttu-id="6d12b-111">Élément searchConnectorDescriptionList (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="6d12b-111">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md) | <span data-ttu-id="6d12b-112"><isSearchOnlyI. TEM></span><span class="sxs-lookup"><span data-stu-id="6d12b-112"><isSearchOnlyI.tem></span></span>             |
|                                                                                                              | <description>                   |
|                                                                                                              | <iconReference>                 |
|                                                                                                              | <imageLink>                     |
|                                                                                                              | <author>                        |
|                                                                                                              | <dateCreated>                   |
|                                                                                                              | <templateInfo>                  |
|                                                                                                              | <locationProvider>              |
|                                                                                                              | <scope>                         |
|                                                                                                              | <propertyStore>                 |
|                                                                                                              | <domain>                        |
|                                                                                                              | <supportsAdvancedQuerySyntax>   |
|                                                                                                              | <isDefaultSaveLocation>         |
|                                                                                                              | <isDefaultNonOwnerSaveLocation> |
|                                                                                                              | <isIndexed>                     |
|                                                                                                              | <simpleLocation>                |
|                                                                                                              | <includeInStartMenu>            |



 

## <a name="attributes"></a><span data-ttu-id="6d12b-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="6d12b-113">Attributes</span></span>



| <span data-ttu-id="6d12b-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="6d12b-114">Attribute</span></span> | <span data-ttu-id="6d12b-115">Description</span><span class="sxs-lookup"><span data-stu-id="6d12b-115">Description</span></span>                                                                      |
|-----------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6d12b-116">publisher</span><span class="sxs-lookup"><span data-stu-id="6d12b-116">publisher</span></span> | <span data-ttu-id="6d12b-117">facultatif.</span><span class="sxs-lookup"><span data-stu-id="6d12b-117">Optional.</span></span> <span data-ttu-id="6d12b-118">Nom complet du serveur de publication qui fournit le connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="6d12b-118">The display name of the publisher providing the search connector.</span></span>      |
| <span data-ttu-id="6d12b-119">product</span><span class="sxs-lookup"><span data-stu-id="6d12b-119">product</span></span>   | <span data-ttu-id="6d12b-120">facultatif.</span><span class="sxs-lookup"><span data-stu-id="6d12b-120">Optional.</span></span> <span data-ttu-id="6d12b-121">Nom complet du produit auquel le connecteur de recherche s’applique.</span><span class="sxs-lookup"><span data-stu-id="6d12b-121">The display name of the product to which the search connector applies.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6d12b-122">Notes</span><span class="sxs-lookup"><span data-stu-id="6d12b-122">Remarks</span></span>

<span data-ttu-id="6d12b-123">L' <searchConnectorDescription> élément d’une bibliothèque utilise la même définition de schéma que la <searchConnectorDescription> recherche fédérée Windows.</span><span class="sxs-lookup"><span data-stu-id="6d12b-123">The <searchConnectorDescription> element of a library uses the same schema definition as the <searchConnectorDescription> for Windows Federated Search.</span></span> <span data-ttu-id="6d12b-124">Bien qu’ils utilisent les mêmes schémas, les connecteurs de recherche pour la recherche fédérée Windows ne peuvent pas être inclus dans une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="6d12b-124">Although they use the same schemas, search connectors for Windows Federated search cannot be included in a library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d12b-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6d12b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d12b-126">Schéma de description de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6d12b-126">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="6d12b-127">Schéma de la description du connecteur de recherche</span><span class="sxs-lookup"><span data-stu-id="6d12b-127">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
