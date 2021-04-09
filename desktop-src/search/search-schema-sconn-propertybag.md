---
description: L' <propertyBag> élément requis spécifie un ensemble d’une ou plusieurs propriétés utilisées par ce fournisseur de localisation.
ms.assetid: 63f8f2e4-3b52-4d6e-8d3a-2e133aac0e86
title: propertyBag, élément (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8fb9e80691e929f7fcceaff3dded4b99a242e92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033872"
---
# <a name="propertybag-element-search-connector-schema"></a><span data-ttu-id="08a19-103">propertyBag, élément (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="08a19-103">propertyBag Element (Search Connector Schema)</span></span>

<span data-ttu-id="08a19-104">L' <propertyBag> élément requis spécifie un ensemble d’une ou plusieurs propriétés utilisées par ce fournisseur de localisation.</span><span class="sxs-lookup"><span data-stu-id="08a19-104">The required <propertyBag> element specifies a set of one or more properties used by this location provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="08a19-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08a19-105">Syntax</span></span>


```
<!-- propertyBag -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
            <xs:element name="locationProvider" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
                            <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
                        </xs:element>
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



## <a name="element-information"></a><span data-ttu-id="08a19-106">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="08a19-106">Element Information</span></span>



| <span data-ttu-id="08a19-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="08a19-107">Parent Element</span></span>                                                                                 | <span data-ttu-id="08a19-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="08a19-108">Child Elements</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="08a19-109">Élément locationProvider (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="08a19-109">locationProvider Element (Search Connector Schema)</span></span>](search-schema-sconn-locationprovider.md) | [<span data-ttu-id="08a19-110">Élément Property (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="08a19-110">property Element (Search Connector Schema)</span></span>](search-schema-sconn-locationproviderproperty.md) |



 

## <a name="example-of-a-propertybag-element-and-property-elements"></a><span data-ttu-id="08a19-111">Exemple d’élément PropertyBag et d’éléments de propriété</span><span class="sxs-lookup"><span data-stu-id="08a19-111">Example of a PropertyBag Element and property Elements</span></span>


```
<locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
        <property name="OpenSearchShortName">MSDN</property>
        <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
        <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
</locationProvider>
```



 

 



