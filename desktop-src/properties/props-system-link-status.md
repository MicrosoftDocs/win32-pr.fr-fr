---
description: Spécifie si le chemin d’accès de lien dans System. Link. TargetParsingPath est vérifié.
ms.assetid: 38c73501-6376-41bb-8ad0-8f94ad42dfc9
title: System. Link. Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9b4a6b398ba022f9f62a0860262028ced49a55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519081"
---
# <a name="systemlinkstatus"></a><span data-ttu-id="0b644-103">System. Link. Status</span><span class="sxs-lookup"><span data-stu-id="0b644-103">System.Link.Status</span></span>

<span data-ttu-id="0b644-104">Spécifie si le chemin d’accès de lien dans [System. Link. TargetParsingPath](./props-system-link-targetparsingpath.md) est vérifié.</span><span class="sxs-lookup"><span data-stu-id="0b644-104">Specifies whether the link path in [System.Link.TargetParsingPath](./props-system-link-targetparsingpath.md) is verified.</span></span> <span data-ttu-id="0b644-105">Ces valeurs sont définies.</span><span class="sxs-lookup"><span data-stu-id="0b644-105">These values are defined.</span></span>

-   <span data-ttu-id="0b644-106">**Non résolu** (par défaut)</span><span class="sxs-lookup"><span data-stu-id="0b644-106">**Unresolved** (default)</span></span>
-   <span data-ttu-id="0b644-107">Résolu</span><span class="sxs-lookup"><span data-stu-id="0b644-107">Resolved</span></span>
-   <span data-ttu-id="0b644-108">Rompu</span><span class="sxs-lookup"><span data-stu-id="0b644-108">Broken</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="0b644-109">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="0b644-109">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Link.Status
   shellPKey = PKEY_Link_Status
   formatID = B9B4B3FC-2B51-4A42-B5D8-324146AFCF25
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Int32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Resolved
            value = 1
            text = Resolved
            defineToken = LINK_STATUS_RESOLVED
         enum
            name = Broken
            value = 2
            text = Broken
            defineToken = LINK_STATUS_BROKEN
```

## <a name="windows-vista"></a><span data-ttu-id="0b644-110">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b644-110">Windows Vista</span></span>

```
propertyDescription
   name = System.Link.Status
   shellPKey = PKEY_Link_Status
   formatID = B9B4B3FC-2B51-4A42-B5D8-324146AFCF25
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Int32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 1
            text = Resolved
            defineName = LINK_STATUS_RESOLVED
         enum
            value = 2
            text = Broken
            defineName = LINK_STATUS_BROKEN
```

## <a name="remarks"></a><span data-ttu-id="0b644-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0b644-111">Remarks</span></span>

<span data-ttu-id="0b644-112">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="0b644-112">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b644-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0b644-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b644-114">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="0b644-114">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="0b644-115">searchInfo</span><span class="sxs-lookup"><span data-stu-id="0b644-115">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="0b644-116">labelInfo</span><span class="sxs-lookup"><span data-stu-id="0b644-116">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="0b644-117">typeInfo</span><span class="sxs-lookup"><span data-stu-id="0b644-117">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="0b644-118">displayInfo</span><span class="sxs-lookup"><span data-stu-id="0b644-118">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="0b644-119">stringFormat</span><span class="sxs-lookup"><span data-stu-id="0b644-119">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="0b644-120">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="0b644-120">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="0b644-121">numberFormat</span><span class="sxs-lookup"><span data-stu-id="0b644-121">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="0b644-122">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="0b644-122">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="0b644-123">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="0b644-123">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="0b644-124">drawControl</span><span class="sxs-lookup"><span data-stu-id="0b644-124">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="0b644-125">editControl</span><span class="sxs-lookup"><span data-stu-id="0b644-125">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="0b644-126">filterControl</span><span class="sxs-lookup"><span data-stu-id="0b644-126">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="0b644-127">queryControl</span><span class="sxs-lookup"><span data-stu-id="0b644-127">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
