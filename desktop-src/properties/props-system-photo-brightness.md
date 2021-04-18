---
description: Valeur de luminosité de l’image, en unités APEX, généralement comprise entre-99,99 et 99,99.
ms.assetid: 533f6934-dec8-455a-937c-d4e144be4335
title: System. photo. Brightness
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 131b7e2d51f402aa8da4d5e9b266fe1fc1b39b29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106522692"
---
# <a name="systemphotobrightness"></a><span data-ttu-id="91b50-103">System. photo. Brightness</span><span class="sxs-lookup"><span data-stu-id="91b50-103">System.Photo.Brightness</span></span>

<span data-ttu-id="91b50-104">Valeur de luminosité de l’image, en unités APEX, généralement comprise entre-99,99 et 99,99.</span><span class="sxs-lookup"><span data-stu-id="91b50-104">The brightness value of the image, in APEX units, usually in the range of -99.99 to 99.99.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="91b50-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91b50-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.Brightness
   shellPKey = PKEY_Photo_Brightness
   formatID = 1A701BF6-478C-4361-83AB-3701BB053C58
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="91b50-106">Notes</span><span class="sxs-lookup"><span data-stu-id="91b50-106">Remarks</span></span>

<span data-ttu-id="91b50-107">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="91b50-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="91b50-108">Consultez la spécification EXIF 2,2, annexe C, pour obtenir une comparaison des chiffres [System. photo. Brightness]() et des mesures de Foot-Lambert.</span><span class="sxs-lookup"><span data-stu-id="91b50-108">See the EXIF 2.2 specification, Annex C, for a comparison of [System.Photo.Brightness]() numbers and Foot-Lambert measurements.</span></span> <span data-ttu-id="91b50-109">Cette propriété est calculée à partir de [System. photo. BrightnessNumerator](./props-system-photo-brightnessnumerator.md) et de [System. photo. BrightnessDenominator](./props-system-photo-brightnessdenominator.md).</span><span class="sxs-lookup"><span data-stu-id="91b50-109">This property is calculated from [System.Photo.BrightnessNumerator](./props-system-photo-brightnessnumerator.md) and [System.Photo.BrightnessDenominator](./props-system-photo-brightnessdenominator.md).</span></span> <span data-ttu-id="91b50-110">Si le numérateur de la valeur enregistrée est FFFFFFFF. H, « Unknown » doit être indiqué.</span><span class="sxs-lookup"><span data-stu-id="91b50-110">If the numerator of the recorded value is FFFFFFFF.H, "Unknown" should be indicated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91b50-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="91b50-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91b50-112">Exchangeable Image File Format pour les appareils photo numériques : EXIF version 2,2</span><span class="sxs-lookup"><span data-stu-id="91b50-112">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="91b50-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="91b50-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="91b50-114">searchInfo</span><span class="sxs-lookup"><span data-stu-id="91b50-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="91b50-115">labelInfo</span><span class="sxs-lookup"><span data-stu-id="91b50-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="91b50-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="91b50-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="91b50-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="91b50-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="91b50-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="91b50-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="91b50-119">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="91b50-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="91b50-120">numberFormat</span><span class="sxs-lookup"><span data-stu-id="91b50-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="91b50-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="91b50-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="91b50-122">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="91b50-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="91b50-123">drawControl</span><span class="sxs-lookup"><span data-stu-id="91b50-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="91b50-124">editControl</span><span class="sxs-lookup"><span data-stu-id="91b50-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="91b50-125">filterControl</span><span class="sxs-lookup"><span data-stu-id="91b50-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="91b50-126">queryControl</span><span class="sxs-lookup"><span data-stu-id="91b50-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
