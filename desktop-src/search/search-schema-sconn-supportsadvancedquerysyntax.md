---
description: L' <supportsAdvancedQuerySyntax> élément boolean spécifie si le moteur de recherche prend en charge la syntaxe de requête avancée. La valeur par défaut est false. Cet élément est facultatif et n’a pas d’éléments enfants ni d’attributs.
ms.assetid: d4aef1f1-63c8-4e9a-9e22-5efbb8c523b2
title: Élément supportsAdvancedQuerySyntax (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d31eb96615c952f703729fd9d22f2e5d27f38b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517457"
---
# <a name="supportsadvancedquerysyntax-element-search-connector-schema"></a><span data-ttu-id="30c8f-105">Élément supportsAdvancedQuerySyntax (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="30c8f-105">supportsAdvancedQuerySyntax Element (Search Connector Schema)</span></span>

<span data-ttu-id="30c8f-106">L' <supportsAdvancedQuerySyntax> élément boolean spécifie si le moteur de recherche prend en charge la [syntaxe de requête avancée](-search-3x-advancedquerysyntax.md).</span><span class="sxs-lookup"><span data-stu-id="30c8f-106">The Boolean <supportsAdvancedQuerySyntax> element specifies whether the search provider supports the [Advanced Query Syntax](-search-3x-advancedquerysyntax.md).</span></span> <span data-ttu-id="30c8f-107">La valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="30c8f-107">The default is false.</span></span> <span data-ttu-id="30c8f-108">Cet élément est facultatif et n’a pas d’éléments enfants ni d’attributs.</span><span class="sxs-lookup"><span data-stu-id="30c8f-108">This element is optional and has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="30c8f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30c8f-109">Syntax</span></span>


```
<!-- supportsAdvancedQuerySyntax -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="supportsAdvancedQuerySyntax" type="xs:boolean" default="false" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="30c8f-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="30c8f-110">Element Information</span></span>



| <span data-ttu-id="30c8f-111">Élément parent</span><span class="sxs-lookup"><span data-stu-id="30c8f-111">Parent Element</span></span>                                                                                                   | <span data-ttu-id="30c8f-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="30c8f-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="30c8f-113">Élément searchConnectorDescriptionType (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="30c8f-113">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="30c8f-114">Notes</span><span class="sxs-lookup"><span data-stu-id="30c8f-114">Remarks</span></span>

<span data-ttu-id="30c8f-115">La valeur `true` indique que le moteur de recherche prend en charge la syntaxe de requête avancée envoyée dans les requêtes de recherche.</span><span class="sxs-lookup"><span data-stu-id="30c8f-115">The value `true` indicates that the search provider supports Advanced Query Syntax sent in search queries.</span></span>

## <a name="example"></a><span data-ttu-id="30c8f-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="30c8f-116">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <supportsAdvancedQuerySyntax>true</supportsAdvancedQuerySyntax>
    ...
</searchConnectionDescription>
```



 

 



