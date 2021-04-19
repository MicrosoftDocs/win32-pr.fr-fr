---
description: Émis par un IFilter de conteneur pour chaque URL enfant dans le conteneur. Les enfants sont finalement analysés par l’indexeur s’ils sont dans la portée.
ms.assetid: e864b3fa-6d43-40fe-9556-474953098947
title: System. Search. UrlToIndex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4832279237cb7a3659b37d6502bd853caff113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541822"
---
# <a name="systemsearchurltoindex"></a><span data-ttu-id="2453b-104">System. Search. UrlToIndex</span><span class="sxs-lookup"><span data-stu-id="2453b-104">System.Search.UrlToIndex</span></span>

<span data-ttu-id="2453b-105">Émis par un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) de conteneur pour chaque URL enfant dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="2453b-105">Emitted by a container [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) for each child URL within the container.</span></span> <span data-ttu-id="2453b-106">Les enfants sont finalement analysés par l’indexeur s’ils sont dans la portée.</span><span class="sxs-lookup"><span data-stu-id="2453b-106">The children are eventually crawled by the indexer if they are within scope.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="2453b-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2453b-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.UrlToIndex
   shellPKey = PKEY_Search_UrlToIndex
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
```

## <a name="remarks"></a><span data-ttu-id="2453b-108">Notes</span><span class="sxs-lookup"><span data-stu-id="2453b-108">Remarks</span></span>

<span data-ttu-id="2453b-109">Cette propriété contient une URL et est émise par un gestionnaire de protocole pour chaque URL enfant ou sous l’URL actuelle.</span><span class="sxs-lookup"><span data-stu-id="2453b-109">This property contains a URL and is emitted by a protocol handler for each child URL or directoy under the current URL.</span></span> <span data-ttu-id="2453b-110">L’indexeur rappelle le gestionnaire de protocole et demande ce document à indexer.</span><span class="sxs-lookup"><span data-stu-id="2453b-110">The indexer calls back into the protocol handler, and asks for that document to be indexed.</span></span> <span data-ttu-id="2453b-111">[System. Search. UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) s’appelait PID \_ GTHR \_ DIRLINK dans les versions antérieures du système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="2453b-111">[System.Search.UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) was called PID\_GTHR\_DIRLINK in earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="2453b-112">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="2453b-112">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2453b-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2453b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2453b-114">System. Search. UrlToIndexWithModificationTime</span><span class="sxs-lookup"><span data-stu-id="2453b-114">System.Search.UrlToIndexWithModificationTime</span></span>](./props-system-search-urltoindexwithmodificationtime.md)
</dt> <dt>

[<span data-ttu-id="2453b-115">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="2453b-115">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="2453b-116">searchInfo</span><span class="sxs-lookup"><span data-stu-id="2453b-116">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="2453b-117">labelInfo</span><span class="sxs-lookup"><span data-stu-id="2453b-117">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="2453b-118">typeInfo</span><span class="sxs-lookup"><span data-stu-id="2453b-118">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="2453b-119">displayInfo</span><span class="sxs-lookup"><span data-stu-id="2453b-119">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="2453b-120">stringFormat</span><span class="sxs-lookup"><span data-stu-id="2453b-120">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="2453b-121">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="2453b-121">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="2453b-122">numberFormat</span><span class="sxs-lookup"><span data-stu-id="2453b-122">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="2453b-123">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="2453b-123">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="2453b-124">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="2453b-124">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="2453b-125">drawControl</span><span class="sxs-lookup"><span data-stu-id="2453b-125">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="2453b-126">editControl</span><span class="sxs-lookup"><span data-stu-id="2453b-126">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="2453b-127">filterControl</span><span class="sxs-lookup"><span data-stu-id="2453b-127">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="2453b-128">queryControl</span><span class="sxs-lookup"><span data-stu-id="2453b-128">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
