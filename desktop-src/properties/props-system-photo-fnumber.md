---
description: Valeur FNumber lors de la prise de la photo, lue à partir des informations EXIF (Exchangeable Image File).
ms.assetid: 914dc34d-34e9-4283-be26-203da945d3e9
title: System. photo. FNumber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22498d498bdf606cb0562f93df9a7b4d40405ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202591"
---
# <a name="systemphotofnumber"></a><span data-ttu-id="ca076-103">System. photo. FNumber</span><span class="sxs-lookup"><span data-stu-id="ca076-103">System.Photo.FNumber</span></span>

<span data-ttu-id="ca076-104">Valeur FNumber lors de la prise de la photo, lue à partir des informations EXIF (Exchangeable Image File). Cette propriété est calculée à partir de [System. photo. FNumberNumerator](./props-system-photo-fnumbernumerator.md) et de [System. photo. FNumberDenominator](./props-system-photo-fnumberdenominator.md).</span><span class="sxs-lookup"><span data-stu-id="ca076-104">The FNumber value when the photo was taken, as read from the Exchangeable Image File (EXIF) information.This property is calculated from [System.Photo.FNumberNumerator](./props-system-photo-fnumbernumerator.md) and [System.Photo.FNumberDenominator](./props-system-photo-fnumberdenominator.md).</span></span>

<span data-ttu-id="ca076-105">Les valeurs possibles sont les suivantes, issues de la spécification EXIF 2,2.</span><span class="sxs-lookup"><span data-stu-id="ca076-105">The following are possible values as taken from the EXIF 2.2 specification.</span></span>

-   <span data-ttu-id="ca076-106">1</span><span class="sxs-lookup"><span data-stu-id="ca076-106">1</span></span>
-   <span data-ttu-id="ca076-107">1.4</span><span class="sxs-lookup"><span data-stu-id="ca076-107">1.4</span></span>
-   <span data-ttu-id="ca076-108">2</span><span class="sxs-lookup"><span data-stu-id="ca076-108">2</span></span>
-   <span data-ttu-id="ca076-109">2.8</span><span class="sxs-lookup"><span data-stu-id="ca076-109">2.8</span></span>
-   <span data-ttu-id="ca076-110">4</span><span class="sxs-lookup"><span data-stu-id="ca076-110">4</span></span>
-   <span data-ttu-id="ca076-111">5.6</span><span class="sxs-lookup"><span data-stu-id="ca076-111">5.6</span></span>
-   <span data-ttu-id="ca076-112">8</span><span class="sxs-lookup"><span data-stu-id="ca076-112">8</span></span>
-   <span data-ttu-id="ca076-113">11</span><span class="sxs-lookup"><span data-stu-id="ca076-113">11</span></span>
-   <span data-ttu-id="ca076-114">16</span><span class="sxs-lookup"><span data-stu-id="ca076-114">16</span></span>
-   <span data-ttu-id="ca076-115">22</span><span class="sxs-lookup"><span data-stu-id="ca076-115">22</span></span>
-   <span data-ttu-id="ca076-116">32</span><span class="sxs-lookup"><span data-stu-id="ca076-116">32</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="ca076-117">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="ca076-117">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.FNumber
   shellPKey = PKEY_Photo_FNumber
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 33437
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="windows-vista"></a><span data-ttu-id="ca076-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca076-118">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.FNumber
   shellPKey = PKEY_Photo_FNumber
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 33437
   SearchInfo
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="ca076-119">Notes</span><span class="sxs-lookup"><span data-stu-id="ca076-119">Remarks</span></span>

<span data-ttu-id="ca076-120">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="ca076-120">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca076-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ca076-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca076-122">Exchangeable Image File Format pour les appareils photo numériques : EXIF version 2,2</span><span class="sxs-lookup"><span data-stu-id="ca076-122">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="ca076-123">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="ca076-123">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="ca076-124">searchInfo</span><span class="sxs-lookup"><span data-stu-id="ca076-124">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="ca076-125">labelInfo</span><span class="sxs-lookup"><span data-stu-id="ca076-125">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="ca076-126">typeInfo</span><span class="sxs-lookup"><span data-stu-id="ca076-126">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="ca076-127">displayInfo</span><span class="sxs-lookup"><span data-stu-id="ca076-127">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="ca076-128">stringFormat</span><span class="sxs-lookup"><span data-stu-id="ca076-128">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="ca076-129">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="ca076-129">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="ca076-130">numberFormat</span><span class="sxs-lookup"><span data-stu-id="ca076-130">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="ca076-131">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="ca076-131">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="ca076-132">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="ca076-132">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="ca076-133">drawControl</span><span class="sxs-lookup"><span data-stu-id="ca076-133">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="ca076-134">editControl</span><span class="sxs-lookup"><span data-stu-id="ca076-134">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="ca076-135">filterControl</span><span class="sxs-lookup"><span data-stu-id="ca076-135">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="ca076-136">queryControl</span><span class="sxs-lookup"><span data-stu-id="ca076-136">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
