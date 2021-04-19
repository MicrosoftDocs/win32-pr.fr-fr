---
description: L' <searchConnectorDescriptionType> élément est le conteneur de niveau supérieur pour la définition de connecteur de recherche.
ms.assetid: a6b45864-210d-4099-804d-7548fd8eb562
title: Élément searchConnectorDescriptionType (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7edb69647567b7e18e25e11dcd0fc773d0be7902
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513982"
---
# <a name="searchconnectordescriptiontype-element-search-connector-schema"></a><span data-ttu-id="73590-103">Élément searchConnectorDescriptionType (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="73590-103">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>

<span data-ttu-id="73590-104">L' <searchConnectorDescriptionType> élément est le conteneur de niveau supérieur pour la définition de connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="73590-104">The <searchConnectorDescriptionType> element is the top level container for the search connector definition.</span></span>

-   [<span data-ttu-id="73590-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73590-105">Syntax</span></span>](#syntax)
-   [<span data-ttu-id="73590-106">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="73590-106">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="73590-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="73590-107">Attributes</span></span>](#attributes)
-   [<span data-ttu-id="73590-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="73590-108">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="73590-109">Exemple de fichier de description de connecteur de recherche</span><span class="sxs-lookup"><span data-stu-id="73590-109">Example of a Search Connector Description File</span></span>](#example-of-a-search-connector-description-file)
-   [<span data-ttu-id="73590-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="73590-110">Related topics</span></span>](#related-topics)

## <a name="syntax"></a><span data-ttu-id="73590-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73590-111">Syntax</span></span>


```
<!-- searchConnectorDescriptionType -->
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



## <a name="element-information"></a><span data-ttu-id="73590-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="73590-112">Element Information</span></span>



| <span data-ttu-id="73590-113">Élément parent</span><span class="sxs-lookup"><span data-stu-id="73590-113">Parent Element</span></span> | <span data-ttu-id="73590-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="73590-114">Child Elements</span></span>                                                                                                           |
|----------------|--------------------------------------------------------------------------------------------------------------------------|
|                | [<span data-ttu-id="73590-115">Élément isSearchOnlyItem (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="73590-115">isSearchOnlyItem Element (Search Connector Schema)</span></span>](search-schema-sconn-issearchonlyitem.md)                           |
|                | [<span data-ttu-id="73590-116">Élément isDefaultSaveLocation (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="73590-116">isDefaultSaveLocation Element (Search Connector Schema)</span></span>](search-schema-sconn-isdefaultsavelocation.md)                 |
|                | [<span data-ttu-id="73590-117">Élément isDefaultNonOwnerSaveLocation (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="73590-117">isDefaultNonOwnerSaveLocation Element (Search Connector Schema)</span></span>](search-schema-sconn-isdefaultnonownersavelocation.md) |
|                | [<span data-ttu-id="73590-118">Description, élément (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="73590-118">description Element (Search Connector Schema)</span></span>](search-schema-sconn-description.md)                                     |
|                | [<span data-ttu-id="73590-119">Élément iconReference (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="73590-119">iconReference Element (Search Connector Schema)</span></span>](search-schema-sconn-iconreference.md)                                 |
|                | [<span data-ttu-id="73590-120">Élément imageLink (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="73590-120">imageLink Element (Search Connector Schema)</span></span>](search-schema-sconn-imagelink.md)                                         |
|                | [<span data-ttu-id="73590-121">auteur, élément (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="73590-121">author Element (Search Connector Schema)</span></span>](search-schema-sconn-author.md)                                               |
|                | [<span data-ttu-id="73590-122">Élément dateCreated (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="73590-122">dateCreated Element (Search Connector Schema)</span></span>](search-schema-sconn-datecreated.md)                                     |
|                | [<span data-ttu-id="73590-123">Élément templateInfo (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="73590-123">templateInfo Element (Search Connector Schema)</span></span>](search-schema-sconn-templateinfo.md)                                   |
|                | [<span data-ttu-id="73590-124">Élément locationProvider (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="73590-124">locationProvider Element (Search Connector Schema)</span></span>](search-schema-sconn-locationprovider.md)                           |
|                | [<span data-ttu-id="73590-125">Élément Scope (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="73590-125">scope Element (Search Connector Schema)</span></span>](search-schema-sconn-scope.md)                                                 |
|                | [<span data-ttu-id="73590-126">Élément propertyStore (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="73590-126">propertyStore Element (Search Connector Schema)</span></span>](search-schema-sconn-propertystore.md)                                 |
|                | [<span data-ttu-id="73590-127">Élément includeInStartMenuScope (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="73590-127">includeInStartMenuScope Element (Search Connector Schema)</span></span>](search-schema-sconn-includeinstartmenuscope.md)             |
|                | [<span data-ttu-id="73590-128">Élément de domaine (schéma de connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="73590-128">domain Element (Search Connector Schema)</span></span>](search-schema-sconn-domain.md)                                               |
|                | [<span data-ttu-id="73590-129">Élément supportsAdvancedQuerySyntax (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="73590-129">supportsAdvancedQuerySyntax Element (Search Connector Schema)</span></span>](search-schema-sconn-supportsadvancedquerysyntax.md)     |
|                | [<span data-ttu-id="73590-130">Élément isIndexed (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="73590-130">isIndexed Element (Search Connector Schema)</span></span>](search-schema-sconn-isindexed.md)                                         |



 

## <a name="attributes"></a><span data-ttu-id="73590-131">Attributs</span><span class="sxs-lookup"><span data-stu-id="73590-131">Attributes</span></span>



| <span data-ttu-id="73590-132">Attribut</span><span class="sxs-lookup"><span data-stu-id="73590-132">Attribute</span></span> | <span data-ttu-id="73590-133">Description</span><span class="sxs-lookup"><span data-stu-id="73590-133">Description</span></span>                                                                      |
|-----------|----------------------------------------------------------------------------------|
| <span data-ttu-id="73590-134">publisher</span><span class="sxs-lookup"><span data-stu-id="73590-134">publisher</span></span> | <span data-ttu-id="73590-135">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="73590-135">Optional.</span></span> <span data-ttu-id="73590-136">Nom complet du serveur de publication qui fournit le connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="73590-136">The display name of the publisher providing the search connector.</span></span>      |
| <span data-ttu-id="73590-137">product</span><span class="sxs-lookup"><span data-stu-id="73590-137">product</span></span>   | <span data-ttu-id="73590-138">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="73590-138">Optional.</span></span> <span data-ttu-id="73590-139">Nom complet du produit auquel le connecteur de recherche s’applique.</span><span class="sxs-lookup"><span data-stu-id="73590-139">The display name of the product to which the search connector applies.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="73590-140">Notes</span><span class="sxs-lookup"><span data-stu-id="73590-140">Remarks</span></span>

<span data-ttu-id="73590-141">Les connecteurs de recherche pour la recherche fédérée ne peuvent pas être utilisés dans les bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="73590-141">Search connectors for federated search cannot be used in libraries.</span></span> <span data-ttu-id="73590-142">Le schéma pour les connecteurs de recherche de bibliothèque est une extension du schéma décrit ici et contient des informations spécifiques aux bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="73590-142">The schema for library search connectors is an extension of the schema described here and includes information specific to libraries.</span></span>

## <a name="example-of-a-search-connector-description-file"></a><span data-ttu-id="73590-143">Exemple de fichier de description de connecteur de recherche</span><span class="sxs-lookup"><span data-stu-id="73590-143">Example of a Search Connector Description File</span></span>

<span data-ttu-id="73590-144">Voici un exemple de fichier de description de connecteur de recherche pour un service Web de recherche fédérée.</span><span class="sxs-lookup"><span data-stu-id="73590-144">The following is an example of a Search Connector Description file for a federated search web service.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
  <description>Search MSDN. Powered by live.com</description>
  <isSearchOnlyItem>true</isSearchOnlyItem>
  <domain>https://social.msdn.microsoft.com</domain>
  <supportsAdvancedQuerySyntax>false</supportsAdvancedQuerySyntax>
  <templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
  </templateInfo>
  <propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://social.msdn.microsoft.com/Search/?Query={searchTerms}</property>
  </propertyStore>
  <locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
      <property name="OpenSearchShortName">MSDN</property>
      <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
      <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
  </locationProvider>
</searchConnectorDescription>
```



<span data-ttu-id="73590-145">Voici un exemple de fichier de description de connecteur de recherche pour un gestionnaire de protocole MAPI.</span><span class="sxs-lookup"><span data-stu-id="73590-145">The following is an example of a Search Connector Description file for a MAPI protocol handler.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    <description>Microsoft Outlook</description>
    <isSearchOnlyItem>true</isSearchOnlyItem>
    <includeInStartMenuScope>true</includeInStartMenuScope>
    <templateInfo>
        <folderType>{91475FE5-586B-4EBA-8D75-D17434B8CDF6}</folderType>
    </templateInfo>
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
</searchConnectorDescription>
```



## <a name="related-topics"></a><span data-ttu-id="73590-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="73590-146">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="73590-147">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="73590-147">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="73590-148">Vue d’ensemble du schéma de description du connecteur de recherche</span><span class="sxs-lookup"><span data-stu-id="73590-148">Overview of the Search Connector Description Schema</span></span>](search-sconn-desc-schema-entry.md)
</dt> <dt>

<span data-ttu-id="73590-149">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="73590-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="73590-150">Recherche fédérée dans Windows</span><span class="sxs-lookup"><span data-stu-id="73590-150">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> </dl>

 

 



