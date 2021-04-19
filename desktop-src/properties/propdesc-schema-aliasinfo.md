---
description: Spécifie un alias de tri ou une liste d’alias de tri en spécifiant un élément qui contient une propriété de tri ou une liste de propriétés de tri.
ms.assetid: 4c514197-0df0-49c6-b39e-8a2a7cefa93d
title: aliasInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 052409864617bdaba7acbf9ae561752c83d18395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527397"
---
# <a name="aliasinfo"></a><span data-ttu-id="af281-103">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="af281-103">aliasInfo</span></span>

<span data-ttu-id="af281-104">Spécifie un alias de tri ou une liste d’alias de tri en spécifiant un élément qui contient une propriété de tri ou une liste de propriétés de tri.</span><span class="sxs-lookup"><span data-stu-id="af281-104">Specifies a sort alias or list of sort aliases by specifying an element that contains a sort property or list of sort properties.</span></span> <span data-ttu-id="af281-105">Il ne doit y avoir qu’un seul élément [aliasInfo]() pour chaque élément [PropertyDescription](./propdesc-schema-propertydescription.md) .</span><span class="sxs-lookup"><span data-stu-id="af281-105">There should be only one [aliasInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md) element.</span></span> <span data-ttu-id="af281-106">Pour les propriétés qui définissent canGroupBy = true, à moins qu’une propriété de tri secondaire ne soit spécifiée ( aliasInfo/@additionalSortByAliases = prop : example), l’utilisateur peut connaître un comportement inattendu lors de la modification de l’ordre de tri dans une vue regroupée par la propriété.</span><span class="sxs-lookup"><span data-stu-id="af281-106">For properties that set canGroupBy=true, unless a secondary sort property is specified (aliasInfo/@additionalSortByAliases=prop:example), the user may experience unexpected behavior when changing the sort order in a view that is grouped by the property.</span></span> <span data-ttu-id="af281-107">Plus précisément, l’ordre des groupes change, mais l’ordre des éléments dans les groupes ne l’est pas.</span><span class="sxs-lookup"><span data-stu-id="af281-107">Specifically, the order of the groups will change, but the order of items within the groups will not.</span></span>

## <a name="syntax"></a><span data-ttu-id="af281-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af281-108">Syntax</span></span>


```
<!-- aliasInfo -->
<xs:element name="aliasInfo">
    <xs:complexType>
        <xs:attribute name="sortByAlias" type="canonical-name"/>
        <xs:attribute name="additionalSortByAliases" type="proplist"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="af281-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="af281-109">Element Information</span></span>



| <span data-ttu-id="af281-110">Élément parent</span><span class="sxs-lookup"><span data-stu-id="af281-110">Parent Element</span></span>                                                   | <span data-ttu-id="af281-111">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="af281-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="af281-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="af281-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="af281-113">Aucun</span><span class="sxs-lookup"><span data-stu-id="af281-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="af281-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="af281-114">Attributes</span></span>



| <span data-ttu-id="af281-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="af281-115">Attribute</span></span>               | <span data-ttu-id="af281-116">Description</span><span class="sxs-lookup"><span data-stu-id="af281-116">Description</span></span>                                                                                                                                                            |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af281-117">sortByAlias</span><span class="sxs-lookup"><span data-stu-id="af281-117">sortByAlias</span></span>             | <span data-ttu-id="af281-118">Public.</span><span class="sxs-lookup"><span data-stu-id="af281-118">Public.</span></span> <span data-ttu-id="af281-119">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="af281-119">Optional.</span></span> <span data-ttu-id="af281-120">Nom canonique de la propriété à utiliser pour le tri.</span><span class="sxs-lookup"><span data-stu-id="af281-120">The canonical name of the property that should be used to sort by.</span></span> <span data-ttu-id="af281-121">Cette chaîne est de type canonique.</span><span class="sxs-lookup"><span data-stu-id="af281-121">This string is of type canonical-type.</span></span>                                            |
| <span data-ttu-id="af281-122">additionalSortByAliases</span><span class="sxs-lookup"><span data-stu-id="af281-122">additionalSortByAliases</span></span> | <span data-ttu-id="af281-123">Public.</span><span class="sxs-lookup"><span data-stu-id="af281-123">Public.</span></span> <span data-ttu-id="af281-124">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="af281-124">Optional.</span></span> <span data-ttu-id="af281-125">Liste délimitée par des points-virgules des propriétés supplémentaires à utiliser lors du tri.</span><span class="sxs-lookup"><span data-stu-id="af281-125">A semi-colon delimited list of additional properties to be used when sorting.</span></span> <span data-ttu-id="af281-126">Les propriétés sont appliquées au tri dans la séquence à laquelle elles sont fournies.</span><span class="sxs-lookup"><span data-stu-id="af281-126">The properties are applied to the sort in the sequence they are given.</span></span> |



 

 

 
