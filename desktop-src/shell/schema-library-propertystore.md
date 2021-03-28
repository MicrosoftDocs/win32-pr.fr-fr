---
description: L' <propertyStore> élément spécifie un ensemble d’une ou plusieurs propriétés utilisées par cette bibliothèque. Cet élément est facultatif et n’a pas d’attributs.
ms.assetid: 19532C1F-686F-4c14-8BA8-0043E77BE594
title: Élément propertyStore (schéma de bibliothèque)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ad3b2c15180d6859ea54dea63ec7fc46b7e636c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973531"
---
# <a name="propertystore-element-library-schema"></a><span data-ttu-id="1eb3b-104">Élément propertyStore (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="1eb3b-104">propertyStore Element (Library Schema)</span></span>

<span data-ttu-id="1eb3b-105">L' <propertyStore> élément spécifie un ensemble d’une ou plusieurs propriétés utilisées par cette bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="1eb3b-105">The <propertyStore> element specifies a set of one or more properties used by this library.</span></span> <span data-ttu-id="1eb3b-106">Cet élément est facultatif et n’a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="1eb3b-106">This element is optional and has no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eb3b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1eb3b-107">Syntax</span></span>

``` syntax
<!-- propertyStore -->
<xs:element name="propertyStore" minOccurs="0">
    <xs:complexType>
        <xs:complexContent>
            <!-- properties are extensions of propertyStoreType -->
            <xs:extension base="propertyStoreType"/>        
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a><span data-ttu-id="1eb3b-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="1eb3b-108">Element Information</span></span>



| <span data-ttu-id="1eb3b-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="1eb3b-109">Parent Element</span></span>                                                               | <span data-ttu-id="1eb3b-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1eb3b-110">Child Elements</span></span>                                                   |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="1eb3b-111">Élément libraryDescription (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="1eb3b-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) | [<span data-ttu-id="1eb3b-112">Property, élément (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="1eb3b-112">property Element (Library Schema)</span></span>](schema-library-property.md) |



 

## <a name="remarks"></a><span data-ttu-id="1eb3b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="1eb3b-113">Remarks</span></span>

<span data-ttu-id="1eb3b-114">L' <propertyStore> élément peut avoir un ou plusieurs <property> éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="1eb3b-114">The <propertyStore> element can have one or more <property> child elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1eb3b-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1eb3b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1eb3b-116">Schéma de description de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1eb3b-116">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="1eb3b-117">Schéma de la description du connecteur de recherche</span><span class="sxs-lookup"><span data-stu-id="1eb3b-117">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
