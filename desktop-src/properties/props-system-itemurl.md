---
description: Représente une URL correctement formée qui pointe vers l’élément.
ms.assetid: d592f12b-f8c2-406f-a031-eeb8212e64f7
title: System. ItemUrl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02beb9629661a052d2ec1fae7c7a34e999e777e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542979"
---
# <a name="systemitemurl"></a><span data-ttu-id="0dc72-103">System. ItemUrl</span><span class="sxs-lookup"><span data-stu-id="0dc72-103">System.ItemUrl</span></span>

<span data-ttu-id="0dc72-104">Représente une URL correctement formée qui pointe vers l’élément.</span><span class="sxs-lookup"><span data-stu-id="0dc72-104">Represents a well-formed URL that points to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="0dc72-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0dc72-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemUrl
   shellPKey = PKEY_ItemUrl
   formatID = 49691C90-7E17-101A-A91C-08002B2ECDA9
   propID = 9
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="0dc72-106">Notes</span><span class="sxs-lookup"><span data-stu-id="0dc72-106">Remarks</span></span>

<span data-ttu-id="0dc72-107">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="0dc72-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="0dc72-108">Pour référencer des éléments d’espace de noms Shell par le biais des API Shell, utilisez [System. ParsingPath](./props-system-parsingpath.md).</span><span class="sxs-lookup"><span data-stu-id="0dc72-108">To reference Shell namespace items through Shell APIs, use [System.ParsingPath](./props-system-parsingpath.md).</span></span>

<span data-ttu-id="0dc72-109">Exemples de valeurs</span><span class="sxs-lookup"><span data-stu-id="0dc72-109">Example values:</span></span>



| <span data-ttu-id="0dc72-110">Type d’élément</span><span class="sxs-lookup"><span data-stu-id="0dc72-110">Item type</span></span> | <span data-ttu-id="0dc72-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="0dc72-111">Example</span></span>                        |
|-----------|--------------------------------|
| <span data-ttu-id="0dc72-112">Fichier</span><span class="sxs-lookup"><span data-stu-id="0dc72-112">File</span></span>      | <span data-ttu-id="0dc72-113">file:///c:/mydir/bar/hello.txt</span><span class="sxs-lookup"><span data-stu-id="0dc72-113">file:///c:/mydir/bar/hello.txt</span></span> |
| <span data-ttu-id="0dc72-114">Fichier</span><span class="sxs-lookup"><span data-stu-id="0dc72-114">File</span></span>      | <span data-ttu-id="0dc72-115">CSC://{GUID}/...</span><span class="sxs-lookup"><span data-stu-id="0dc72-115">csc://{GUID}/...</span></span>               |
| <span data-ttu-id="0dc72-116">Message</span><span class="sxs-lookup"><span data-stu-id="0dc72-116">Message</span></span>   | <span data-ttu-id="0dc72-117">mapi://...</span><span class="sxs-lookup"><span data-stu-id="0dc72-117">mapi://...</span></span>                     |



 

## <a name="related-topics"></a><span data-ttu-id="0dc72-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0dc72-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0dc72-119">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="0dc72-119">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="0dc72-120">searchInfo</span><span class="sxs-lookup"><span data-stu-id="0dc72-120">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="0dc72-121">labelInfo</span><span class="sxs-lookup"><span data-stu-id="0dc72-121">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="0dc72-122">typeInfo</span><span class="sxs-lookup"><span data-stu-id="0dc72-122">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="0dc72-123">displayInfo</span><span class="sxs-lookup"><span data-stu-id="0dc72-123">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="0dc72-124">stringFormat</span><span class="sxs-lookup"><span data-stu-id="0dc72-124">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="0dc72-125">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="0dc72-125">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="0dc72-126">numberFormat</span><span class="sxs-lookup"><span data-stu-id="0dc72-126">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="0dc72-127">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="0dc72-127">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="0dc72-128">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="0dc72-128">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="0dc72-129">drawControl</span><span class="sxs-lookup"><span data-stu-id="0dc72-129">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="0dc72-130">editControl</span><span class="sxs-lookup"><span data-stu-id="0dc72-130">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="0dc72-131">filterControl</span><span class="sxs-lookup"><span data-stu-id="0dc72-131">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="0dc72-132">queryControl</span><span class="sxs-lookup"><span data-stu-id="0dc72-132">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
