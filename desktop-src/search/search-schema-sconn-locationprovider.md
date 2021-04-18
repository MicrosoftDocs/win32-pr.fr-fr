---
description: L' <locationProvider> élément facultatif spécifie le moteur de recherche que le connecteur de recherche de fournisseur de services Web doit utiliser. Cet élément contient un attribut obligatoire et un élément enfant facultatif.
ms.assetid: 5481b1ae-e166-4f09-bf0d-d6b7f7c8a331
title: Élément locationProvider (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26c68732300c190b44b984bbe64ca031a81ced84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516213"
---
# <a name="locationprovider-element-search-connector-schema"></a><span data-ttu-id="a6979-104">Élément locationProvider (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="a6979-104">locationProvider Element (Search Connector Schema)</span></span>

<span data-ttu-id="a6979-105">L' <locationProvider> élément facultatif spécifie le moteur de recherche que le connecteur de recherche de fournisseur de services Web doit utiliser.</span><span class="sxs-lookup"><span data-stu-id="a6979-105">The optional <locationProvider> element specifies the search provider to be used by the web service provider search connector.</span></span> <span data-ttu-id="a6979-106">Cet élément contient un attribut obligatoire et un élément enfant facultatif.</span><span class="sxs-lookup"><span data-stu-id="a6979-106">This element contains one mandatory attribute and an optional child element.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6979-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6979-107">Syntax</span></span>


```
<!-- locationProvider -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="locationProvider" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0"/>
                    </xs:all>
                <xs:attribute name="clsid" use="required"/>
                <xs:attribute name="codebase" type="xs:string"/>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="a6979-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a6979-108">Element Information</span></span>



| <span data-ttu-id="a6979-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="a6979-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="a6979-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a6979-110">Child Elements</span></span>                                                                       |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="a6979-111">Élément searchConnectorDescriptionType (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="a6979-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="a6979-112">propertyBag, élément (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="a6979-112">propertyBag Element (Search Connector Schema)</span></span>](search-schema-sconn-propertybag.md) |



 

## <a name="attributes"></a><span data-ttu-id="a6979-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="a6979-113">Attributes</span></span>



| <span data-ttu-id="a6979-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="a6979-114">Attribute</span></span> | <span data-ttu-id="a6979-115">Description</span><span class="sxs-lookup"><span data-stu-id="a6979-115">Description</span></span>                                                    |
|-----------|----------------------------------------------------------------|
| @clsid    | <span data-ttu-id="a6979-116">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a6979-116">Required.</span></span> <span data-ttu-id="a6979-117">Identificateur de classe (CLSID) du moteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="a6979-117">The class identifier (CLSID) of the search provider.</span></span> |
| <span data-ttu-id="a6979-118">CodeBase</span><span class="sxs-lookup"><span data-stu-id="a6979-118">codebase</span></span>  | <span data-ttu-id="a6979-119">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="a6979-119">Optional.</span></span>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="a6979-120">Notes</span><span class="sxs-lookup"><span data-stu-id="a6979-120">Remarks</span></span>

<span data-ttu-id="a6979-121">La @clsid valeur de l’attribut pour le fournisseur OpenSearch est {48E277F6-4E74-4CD6-BA6F-FA4F42898223}.</span><span class="sxs-lookup"><span data-stu-id="a6979-121">The @clsid attribute value for the OpenSearch provider is {48E277F6-4E74-4cd6-BA6F-FA4F42898223}.</span></span>

<span data-ttu-id="a6979-122">Les connecteurs de recherche basés sur le système de fichiers et le gestionnaire de protocole peuvent utiliser l’élément à la [<simpleLocation>](search-schema-sconn-simplelocation.md) place.</span><span class="sxs-lookup"><span data-stu-id="a6979-122">File system and protocol handler based search connectors can use the [<simpleLocation>](search-schema-sconn-simplelocation.md) element instead.</span></span> <span data-ttu-id="a6979-123">Si <locationProvider> est présent, il ne doit pas y avoir <simpleLocation> d’élément dans la description de la recherche de connecteur.</span><span class="sxs-lookup"><span data-stu-id="a6979-123">If <locationProvider> is present, there MUST NOT be a <simpleLocation> element in the Search Connector description.</span></span>

## <a name="example-of-a-locationprovider-element"></a><span data-ttu-id="a6979-124">Exemple d’élément locationProvider</span><span class="sxs-lookup"><span data-stu-id="a6979-124">Example of a locationProvider Element</span></span>


```
<locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
        <property name="OpenSearchShortName">MSDN</property>
        <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
        <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
</locationProvider>
```



 

 



