---
description: Cette propriété est la même que celle de System. Search. UrlToIndex, à ceci près qu’elle comprend l’heure de la dernière modification de l’URL.
ms.assetid: 53ca765b-0795-49ab-9946-c3ef101ababd
title: System. Search. UrlToIndexWithModificationTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fcc83b9796ae2375f10235a08ba0db313fb1958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536588"
---
# <a name="systemsearchurltoindexwithmodificationtime"></a><span data-ttu-id="bd98d-103">System. Search. UrlToIndexWithModificationTime</span><span class="sxs-lookup"><span data-stu-id="bd98d-103">System.Search.UrlToIndexWithModificationTime</span></span>

<span data-ttu-id="bd98d-104">Cette propriété est la même que celle de [**System. Search. UrlToIndex**](props-system-search-urltoindex.md) , à ceci près qu’elle comprend l’heure de la dernière modification de l’URL.</span><span class="sxs-lookup"><span data-stu-id="bd98d-104">This property is the same as [**System.Search.UrlToIndex**](props-system-search-urltoindex.md) except that it includes the time that the URL was last modified.</span></span> <span data-ttu-id="bd98d-105">Il s’agit d’une optimisation pour l’indexeur afin qu’il n’ait pas à rappeler le gestionnaire de protocole pour demander ces informations afin de déterminer si le contenu doit être indexé à nouveau.</span><span class="sxs-lookup"><span data-stu-id="bd98d-105">This is an optimization for the indexer so that it does not have to call back into the protocol handler to ask for this information to determine whether the content needs to be indexed again.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="bd98d-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bd98d-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.UrlToIndexWithModificationTime
   shellPKey = PKEY_Search_UrlToIndexWithModificationTime
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 12
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Any
```

## <a name="remarks"></a><span data-ttu-id="bd98d-107">Notes</span><span class="sxs-lookup"><span data-stu-id="bd98d-107">Remarks</span></span>

<span data-ttu-id="bd98d-108">Cette propriété [System. Search. UrlToIndexWithModificationTime]() est la même que la propriété [System. Search. UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) , sauf que vous transmettez également l’heure de la dernière modification du document.</span><span class="sxs-lookup"><span data-stu-id="bd98d-108">This [System.Search.UrlToIndexWithModificationTime]() property is the same as the [System.Search.UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) property, except that you also pass in the last modified time of the document.</span></span> <span data-ttu-id="bd98d-109">Si l’heure de la dernière modification correspond, l’indexeur suppose que le document est déjà indexé et lève la notification.</span><span class="sxs-lookup"><span data-stu-id="bd98d-109">If the last modified time matches, the indexer assumes that the document is already indexed and throws away the notification.</span></span> <span data-ttu-id="bd98d-110">Cette propriété est un vecteur avec deux éléments, une valeur **VT \_ LPWStr** qui contient l’URL et une valeur de la **VT \_ fileTime** qui contient l’heure de la dernière modification.</span><span class="sxs-lookup"><span data-stu-id="bd98d-110">This property is a vector with two elements, a **VT\_LPWSTR** value that contains the URL and a **VT\_FILETIME** value that contains the last modified time.</span></span>

<span data-ttu-id="bd98d-111">[System. Search. UrlToIndexWithModificationTime]() a été appelé PID \_ GTHR \_ DIRLINK \_ avec \_ le temps dans les versions antérieures du système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="bd98d-111">[System.Search.UrlToIndexWithModificationTime]() was called PID\_GTHR\_DIRLINK\_WITH\_TIME in earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="bd98d-112">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="bd98d-112">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd98d-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bd98d-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bd98d-114">[System. Search. UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bd98d-114">[System.Search.UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="bd98d-115">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="bd98d-115">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="bd98d-116">searchInfo</span><span class="sxs-lookup"><span data-stu-id="bd98d-116">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="bd98d-117">labelInfo</span><span class="sxs-lookup"><span data-stu-id="bd98d-117">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="bd98d-118">typeInfo</span><span class="sxs-lookup"><span data-stu-id="bd98d-118">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="bd98d-119">displayInfo</span><span class="sxs-lookup"><span data-stu-id="bd98d-119">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="bd98d-120">stringFormat</span><span class="sxs-lookup"><span data-stu-id="bd98d-120">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="bd98d-121">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="bd98d-121">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="bd98d-122">numberFormat</span><span class="sxs-lookup"><span data-stu-id="bd98d-122">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="bd98d-123">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="bd98d-123">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="bd98d-124">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="bd98d-124">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="bd98d-125">drawControl</span><span class="sxs-lookup"><span data-stu-id="bd98d-125">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="bd98d-126">editControl</span><span class="sxs-lookup"><span data-stu-id="bd98d-126">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="bd98d-127">filterControl</span><span class="sxs-lookup"><span data-stu-id="bd98d-127">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="bd98d-128">queryControl</span><span class="sxs-lookup"><span data-stu-id="bd98d-128">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
