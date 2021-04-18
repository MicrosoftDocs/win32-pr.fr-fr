---
description: Lors de l’utilisation de CONTAINs sur l’index de recherche Windows, il s’agit du nombre de correspondances du terme. S’il y a plusieurs CONTAINs, un et calcule le nombre minimal d’accès, et un ou calcule le nombre maximal d’accès.
ms.assetid: 2f0cddba-7535-451f-9bb5-846c06c426f8
title: System. Search. HitCount
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bb3954d891c1f7c913036449094c27f64cea7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519538"
---
# <a name="systemsearchhitcount"></a><span data-ttu-id="5ad9f-104">System. Search. HitCount</span><span class="sxs-lookup"><span data-stu-id="5ad9f-104">System.Search.HitCount</span></span>

<span data-ttu-id="5ad9f-105">Lors de l’utilisation de CONTAINs sur l’index de recherche Windows, il s’agit du nombre de correspondances du terme.</span><span class="sxs-lookup"><span data-stu-id="5ad9f-105">When using CONTAINS over the Windows Search Index, this is the number of matches of the term.</span></span> <span data-ttu-id="5ad9f-106">S’il y a plusieurs CONTAINs, un et calcule le nombre minimal d’accès, et un ou calcule le nombre maximal d’accès.</span><span class="sxs-lookup"><span data-stu-id="5ad9f-106">If there are multiple CONTAINS, an AND computes the minimal number of hits, and an OR computes the maximal number of hits.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="5ad9f-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ad9f-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.HitCount
   shellPKey = PKEY_Search_HitCount
   formatID = 49691C90-7E17-101A-A91C-08002B2ECDA9
   propID = 4
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Int32
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="5ad9f-108">Notes</span><span class="sxs-lookup"><span data-stu-id="5ad9f-108">Remarks</span></span>

<span data-ttu-id="5ad9f-109">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="5ad9f-109">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ad9f-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5ad9f-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ad9f-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="5ad9f-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="5ad9f-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="5ad9f-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="5ad9f-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="5ad9f-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="5ad9f-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="5ad9f-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="5ad9f-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="5ad9f-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="5ad9f-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="5ad9f-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="5ad9f-117">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="5ad9f-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="5ad9f-118">numberFormat</span><span class="sxs-lookup"><span data-stu-id="5ad9f-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="5ad9f-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="5ad9f-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="5ad9f-120">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="5ad9f-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="5ad9f-121">drawControl</span><span class="sxs-lookup"><span data-stu-id="5ad9f-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="5ad9f-122">editControl</span><span class="sxs-lookup"><span data-stu-id="5ad9f-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="5ad9f-123">filterControl</span><span class="sxs-lookup"><span data-stu-id="5ad9f-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="5ad9f-124">queryControl</span><span class="sxs-lookup"><span data-stu-id="5ad9f-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
