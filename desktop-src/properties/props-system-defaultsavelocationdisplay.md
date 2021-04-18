---
description: Permet d’afficher sous la forme d’une icône, qu’il s’agisse ou non de l’emplacement d’enregistrement par défaut pour le propriétaire et/ou les non-propriétaires d’une bibliothèque.
ms.assetid: 42375796-bf95-4092-bce0-c77e7b5bfeea
title: System. DefaultSaveLocationDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1147a7c0fce8b4bc564b57bac2476b1826e4313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536148"
---
# <a name="systemdefaultsavelocationdisplay"></a><span data-ttu-id="17d95-103">System. DefaultSaveLocationDisplay</span><span class="sxs-lookup"><span data-stu-id="17d95-103">System.DefaultSaveLocationDisplay</span></span>

<span data-ttu-id="17d95-104">Permet d’afficher sous la forme d’une icône, qu’il s’agisse ou non de l’emplacement d’enregistrement par défaut pour le propriétaire et/ou les non-propriétaires d’une bibliothèque</span><span class="sxs-lookup"><span data-stu-id="17d95-104">Helps display as an icon whether or not a location is the default save location for owner and/or non-owners of a library</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="17d95-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="17d95-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.DefaultSaveLocationDisplay
   shellPKey = PKEY_DefaultSaveLocationDisplay
   formatID = 5D76B67F-9B3D-44BB-B6AE-25DA4F638A67
   propID = 10
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enum
            name = DefaultSaveNone
            value = 0
            text
            defineToken = ISDEFAULTSAVE_NONE
         enum
            name = DefaultSaveOwner
            value = 1
            text = Default save location
            defineToken = ISDEFAULTSAVE_OWNER
         enum
            name = DefaultSavePublic
            value = 2
            text = Public save location
            defineToken = ISDEFAULTSAVE_NONOWNER
         enum
            name = DefaultSaveBoth
            value = 3
            text = Default and public save location
            defineToken = ISDEFAULTSAVE_BOTH
```

## <a name="remarks"></a><span data-ttu-id="17d95-106">Notes</span><span class="sxs-lookup"><span data-stu-id="17d95-106">Remarks</span></span>

<span data-ttu-id="17d95-107">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="17d95-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17d95-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="17d95-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17d95-109">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="17d95-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="17d95-110">searchInfo</span><span class="sxs-lookup"><span data-stu-id="17d95-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="17d95-111">labelInfo</span><span class="sxs-lookup"><span data-stu-id="17d95-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="17d95-112">typeInfo</span><span class="sxs-lookup"><span data-stu-id="17d95-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="17d95-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="17d95-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="17d95-114">stringFormat</span><span class="sxs-lookup"><span data-stu-id="17d95-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="17d95-115">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="17d95-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="17d95-116">numberFormat</span><span class="sxs-lookup"><span data-stu-id="17d95-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="17d95-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="17d95-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="17d95-118">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="17d95-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="17d95-119">drawControl</span><span class="sxs-lookup"><span data-stu-id="17d95-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="17d95-120">editControl</span><span class="sxs-lookup"><span data-stu-id="17d95-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="17d95-121">filterControl</span><span class="sxs-lookup"><span data-stu-id="17d95-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="17d95-122">queryControl</span><span class="sxs-lookup"><span data-stu-id="17d95-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
