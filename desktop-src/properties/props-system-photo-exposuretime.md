---
description: Temps d’exposition de la photo, en secondes, lu à partir des informations EXIF (Exchangeable Image File).
ms.assetid: 44f7e6d5-c4d9-4b41-b6c6-15145abb7983
title: System. photo. ExposureTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5811a3d375f41883d1db8f392e714b7bbe0dfa8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202594"
---
# <a name="systemphotoexposuretime"></a><span data-ttu-id="f6460-103">System. photo. ExposureTime</span><span class="sxs-lookup"><span data-stu-id="f6460-103">System.Photo.ExposureTime</span></span>

<span data-ttu-id="f6460-104">Temps d’exposition de la photo, en secondes, lu à partir des informations EXIF (Exchangeable Image File).</span><span class="sxs-lookup"><span data-stu-id="f6460-104">The exposure time for the photo, in seconds, as read from the Exchangeable Image File (EXIF) information.</span></span> <span data-ttu-id="f6460-105">Cette propriété est calculée à partir de [System. photo. ExposureTimeNumerator](./props-system-photo-exposuretimenumerator.md) et de [System. photo. ExposureTimeDenominator](./props-system-photo-exposuretimedenominator.md).</span><span class="sxs-lookup"><span data-stu-id="f6460-105">This property is calculated from [System.Photo.ExposureTimeNumerator](./props-system-photo-exposuretimenumerator.md) and [System.Photo.ExposureTimeDenominator](./props-system-photo-exposuretimedenominator.md).</span></span>

<span data-ttu-id="f6460-106">La liste suivante répertorie les valeurs possibles tirées de la spécification EXIF 2,2.</span><span class="sxs-lookup"><span data-stu-id="f6460-106">The following is a list of possible values taken from the EXIF 2.2 specification.</span></span>

-   <span data-ttu-id="f6460-107">30</span><span class="sxs-lookup"><span data-stu-id="f6460-107">30</span></span>
-   <span data-ttu-id="f6460-108">15</span><span class="sxs-lookup"><span data-stu-id="f6460-108">15</span></span>
-   <span data-ttu-id="f6460-109">8</span><span class="sxs-lookup"><span data-stu-id="f6460-109">8</span></span>
-   <span data-ttu-id="f6460-110">4</span><span class="sxs-lookup"><span data-stu-id="f6460-110">4</span></span>
-   <span data-ttu-id="f6460-111">2</span><span class="sxs-lookup"><span data-stu-id="f6460-111">2</span></span>
-   <span data-ttu-id="f6460-112">1</span><span class="sxs-lookup"><span data-stu-id="f6460-112">1</span></span>
-   <span data-ttu-id="f6460-113">1/2</span><span class="sxs-lookup"><span data-stu-id="f6460-113">1/2</span></span>
-   <span data-ttu-id="f6460-114">1/4</span><span class="sxs-lookup"><span data-stu-id="f6460-114">1/4</span></span>
-   <span data-ttu-id="f6460-115">1/8</span><span class="sxs-lookup"><span data-stu-id="f6460-115">1/8</span></span>
-   <span data-ttu-id="f6460-116">1/15</span><span class="sxs-lookup"><span data-stu-id="f6460-116">1/15</span></span>
-   <span data-ttu-id="f6460-117">1/30</span><span class="sxs-lookup"><span data-stu-id="f6460-117">1/30</span></span>
-   <span data-ttu-id="f6460-118">1/60</span><span class="sxs-lookup"><span data-stu-id="f6460-118">1/60</span></span>
-   <span data-ttu-id="f6460-119">1/125</span><span class="sxs-lookup"><span data-stu-id="f6460-119">1/125</span></span>
-   <span data-ttu-id="f6460-120">1/250</span><span class="sxs-lookup"><span data-stu-id="f6460-120">1/250</span></span>
-   <span data-ttu-id="f6460-121">1/500</span><span class="sxs-lookup"><span data-stu-id="f6460-121">1/500</span></span>
-   <span data-ttu-id="f6460-122">1/1000</span><span class="sxs-lookup"><span data-stu-id="f6460-122">1/1000</span></span>
-   <span data-ttu-id="f6460-123">1/2000</span><span class="sxs-lookup"><span data-stu-id="f6460-123">1/2000</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="f6460-124">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6460-124">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.ExposureTime
   shellPKey = PKEY_Photo_ExposureTime
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 33434
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="f6460-125">Notes</span><span class="sxs-lookup"><span data-stu-id="f6460-125">Remarks</span></span>

<span data-ttu-id="f6460-126">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="f6460-126">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6460-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f6460-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6460-128">Exchangeable Image File Format pour les appareils photo numériques : EXIF version 2,2</span><span class="sxs-lookup"><span data-stu-id="f6460-128">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="f6460-129">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="f6460-129">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="f6460-130">searchInfo</span><span class="sxs-lookup"><span data-stu-id="f6460-130">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="f6460-131">labelInfo</span><span class="sxs-lookup"><span data-stu-id="f6460-131">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="f6460-132">typeInfo</span><span class="sxs-lookup"><span data-stu-id="f6460-132">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="f6460-133">displayInfo</span><span class="sxs-lookup"><span data-stu-id="f6460-133">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="f6460-134">stringFormat</span><span class="sxs-lookup"><span data-stu-id="f6460-134">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="f6460-135">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="f6460-135">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="f6460-136">numberFormat</span><span class="sxs-lookup"><span data-stu-id="f6460-136">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="f6460-137">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="f6460-137">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="f6460-138">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="f6460-138">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="f6460-139">drawControl</span><span class="sxs-lookup"><span data-stu-id="f6460-139">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="f6460-140">editControl</span><span class="sxs-lookup"><span data-stu-id="f6460-140">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="f6460-141">filterControl</span><span class="sxs-lookup"><span data-stu-id="f6460-141">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="f6460-142">queryControl</span><span class="sxs-lookup"><span data-stu-id="f6460-142">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
