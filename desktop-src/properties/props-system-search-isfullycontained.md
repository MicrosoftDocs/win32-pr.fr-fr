---
description: Émis comme TRUE par tous les éléments enfants d’un conteneur (par exemple, un message électronique ou un fichier compressé avec une extension de nom. zip) qui émet System. Search. IsClosedDirectory comme TRUE. Cela permet de s’assurer que les éléments enfants sont inclus dans l’index de recherche.
ms.assetid: 6da60e89-6956-41f6-8624-063c4d46464d
title: System. Search. IsFullyContained
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1245f29a2940146a4e5d8f0a392210173be75e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530051"
---
# <a name="systemsearchisfullycontained"></a><span data-ttu-id="102c4-104">System. Search. IsFullyContained</span><span class="sxs-lookup"><span data-stu-id="102c4-104">System.Search.IsFullyContained</span></span>

<span data-ttu-id="102c4-105">Émis comme **true** par tous les éléments enfants d’un conteneur (par exemple, un message électronique ou un fichier compressé avec une extension de nom. zip) qui émet [System. Search. IsClosedDirectory](./props-system-search-iscloseddirectory.md) comme **true**.</span><span class="sxs-lookup"><span data-stu-id="102c4-105">Emitted as **TRUE** by all child items of a container (such as an e-mail or a compressed file with a .zip name extension) that emits [System.Search.IsClosedDirectory](./props-system-search-iscloseddirectory.md) as **TRUE**.</span></span> <span data-ttu-id="102c4-106">Cela permet de s’assurer que les éléments enfants sont inclus dans l’index de recherche.</span><span class="sxs-lookup"><span data-stu-id="102c4-106">This ensures that the child items are included in the search index.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="102c4-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="102c4-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.IsFullyContained
   shellPKey = PKEY_Search_IsFullyContained
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 24
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a><span data-ttu-id="102c4-108">Notes</span><span class="sxs-lookup"><span data-stu-id="102c4-108">Remarks</span></span>

<span data-ttu-id="102c4-109">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="102c4-109">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="102c4-110">La propriété [System. Search. IsClosedDirectory](./props-system-search-iscloseddirectory.md) permet d’optimiser les performances de l’indexeur en permettant à l’indexeur d’ignorer l’énumération des éléments enfants d’un conteneur.</span><span class="sxs-lookup"><span data-stu-id="102c4-110">The [System.Search.IsClosedDirectory](./props-system-search-iscloseddirectory.md) property helps to optimize indexer performance by allowing the indexer to skip the enumeration of a container's child items.</span></span> <span data-ttu-id="102c4-111">Toutefois, ces éléments enfants sont marqués par l’indexeur comme non visités et, par conséquent, ils sont supprimés de l’index.</span><span class="sxs-lookup"><span data-stu-id="102c4-111">However, those child items are marked by the indexer as not visited, and as such will be deleted from the index.</span></span> <span data-ttu-id="102c4-112">En émettant [System. Search. IsFullyContained]() comme **true**, un élément n’est pas supprimé de l’index, même s’il n’a pas été visité.</span><span class="sxs-lookup"><span data-stu-id="102c4-112">By emitting [System.Search.IsFullyContained]() as **TRUE**, an item is not deleted from the index despite having not been visited.</span></span>

## <a name="related-topics"></a><span data-ttu-id="102c4-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="102c4-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="102c4-114">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="102c4-114">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="102c4-115">searchInfo</span><span class="sxs-lookup"><span data-stu-id="102c4-115">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="102c4-116">labelInfo</span><span class="sxs-lookup"><span data-stu-id="102c4-116">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="102c4-117">typeInfo</span><span class="sxs-lookup"><span data-stu-id="102c4-117">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="102c4-118">displayInfo</span><span class="sxs-lookup"><span data-stu-id="102c4-118">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="102c4-119">stringFormat</span><span class="sxs-lookup"><span data-stu-id="102c4-119">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="102c4-120">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="102c4-120">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="102c4-121">numberFormat</span><span class="sxs-lookup"><span data-stu-id="102c4-121">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="102c4-122">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="102c4-122">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="102c4-123">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="102c4-123">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="102c4-124">drawControl</span><span class="sxs-lookup"><span data-stu-id="102c4-124">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="102c4-125">editControl</span><span class="sxs-lookup"><span data-stu-id="102c4-125">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="102c4-126">filterControl</span><span class="sxs-lookup"><span data-stu-id="102c4-126">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="102c4-127">queryControl</span><span class="sxs-lookup"><span data-stu-id="102c4-127">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
