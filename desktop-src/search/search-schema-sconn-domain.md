---
description: L' <domain> élément facultatif spécifie l’URL du service de recherche utilisé par ce connecteur de recherche. Il s’affiche dans le volet d’informations. Cet élément n’a pas d’éléments enfants ni d’attributs.
ms.assetid: 60a27b13-0bb0-4cf6-9dce-a3abc79ce623
title: Élément de domaine (schéma de connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b57819cf485bccbe63e7560f3fcb92811d7969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862146"
---
# <a name="domain-element-search-connector-schema"></a><span data-ttu-id="b6a21-105">Élément de domaine (schéma de connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="b6a21-105">domain Element (Search Connector Schema)</span></span>

<span data-ttu-id="b6a21-106">L' <domain> élément facultatif spécifie l’URL du service de recherche utilisé par ce connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="b6a21-106">The optional <domain> element specifies the URL of the search service used by this search connector.</span></span> <span data-ttu-id="b6a21-107">Il s’affiche dans le volet d’informations.</span><span class="sxs-lookup"><span data-stu-id="b6a21-107">It is displayed in the details pane.</span></span> <span data-ttu-id="b6a21-108">Cet élément n’a pas d’éléments enfants ni d’attributs.</span><span class="sxs-lookup"><span data-stu-id="b6a21-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6a21-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6a21-109">Syntax</span></span>


```
<!-- domain -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="domain" type="xs:string" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="b6a21-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b6a21-110">Element Information</span></span>



| <span data-ttu-id="b6a21-111">Élément parent</span><span class="sxs-lookup"><span data-stu-id="b6a21-111">Parent Element</span></span>                                                                                                   | <span data-ttu-id="b6a21-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b6a21-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="b6a21-113">Élément searchConnectorDescriptionType (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="b6a21-113">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="b6a21-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b6a21-114">Remarks</span></span>

<span data-ttu-id="b6a21-115">L’URL doit être le domaine de niveau supérieur pour le moteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="b6a21-115">The URL should be the top-level domain for the search provider.</span></span> <span data-ttu-id="b6a21-116">Par exemple : https://www.example.com.</span><span class="sxs-lookup"><span data-stu-id="b6a21-116">For example, https://www.example.com.</span></span>

## <a name="example"></a><span data-ttu-id="b6a21-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="b6a21-117">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <domain>https://www.adventureworks.com</domain>
    ...
</searchConnectionDescription>
```



 

 



