---
description: L' <scope> élément facultatif spécifie une collection d' <scopeItem> éléments qui définissent les inclusions et les exclusions de portée pour ce connecteur de recherche particulier.
ms.assetid: 9e92e3db-3d5e-4f86-8d67-90eb5469b04b
title: Élément Scope (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f49041170db80de48d312596249d5c4dca835e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527185"
---
# <a name="scope-element-search-connector-schema"></a><span data-ttu-id="23f9d-103">Élément Scope (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="23f9d-103">scope Element (Search Connector Schema)</span></span>

<span data-ttu-id="23f9d-104">L' <scope> élément facultatif spécifie une collection d' <scopeItem> éléments qui définissent les inclusions et les exclusions de portée pour ce connecteur de recherche particulier.</span><span class="sxs-lookup"><span data-stu-id="23f9d-104">The optional <scope> element specifies a collection of <scopeItem> elements that define the scope inclusions and exclusions for this particular search connector.</span></span> <span data-ttu-id="23f9d-105">Si <scope> est présent, il doit contenir au moins un <scopeItem> élément.</span><span class="sxs-lookup"><span data-stu-id="23f9d-105">If <scope> is present, it MUST contain at least one <scopeItem> element.</span></span> <span data-ttu-id="23f9d-106">Cet élément n’a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="23f9d-106">This element has no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="23f9d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23f9d-107">Syntax</span></span>


```
<!-- scope -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                       ...
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



## <a name="element-information"></a><span data-ttu-id="23f9d-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="23f9d-108">Element Information</span></span>



| <span data-ttu-id="23f9d-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="23f9d-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="23f9d-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="23f9d-110">Child Elements</span></span>                                                                    |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="23f9d-111">Élément searchConnectorDescriptionType (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="23f9d-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | <span data-ttu-id="23f9d-112">[élément scopeItem (schéma du connecteur de recherche)](search-schema-sconn-scopeitem.md).</span><span class="sxs-lookup"><span data-stu-id="23f9d-112">[scopeItem Element (Search Connector Schema)](search-schema-sconn-scopeitem.md).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="23f9d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="23f9d-113">Remarks</span></span>

<span data-ttu-id="23f9d-114">Utilisez les <scope> <scopeItem> éléments et pour identifier les emplacements à rechercher et les emplacements qui doivent être exclus de la recherche.</span><span class="sxs-lookup"><span data-stu-id="23f9d-114">Use the <scope> and <scopeItem> elements to identify which locations should be searched and which locations should be excluded from searching.</span></span>

## <a name="example"></a><span data-ttu-id="23f9d-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="23f9d-115">Example</span></span>

<span data-ttu-id="23f9d-116">L’exemple suivant montre une étendue de recherche qui comprend C : \\ ExampleFolder et tous ses dossiers enfants, à l’exception de c : \\ ExampleFolder \\ ExcludeMe.</span><span class="sxs-lookup"><span data-stu-id="23f9d-116">The following example shows a search scope that includes C:\\ExampleFolder and all its child folders except C:\\ExampleFolder\\ExcludeMe.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder</url>
        </scopeItem>
        <scopeItem>
            <mode>Exclude</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



