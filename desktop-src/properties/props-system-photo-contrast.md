---
description: Indique la direction du traitement du contraste appliquée par l’appareil photo lorsque l’image a été prise. &\#0034 ; 0&\# 0034 ; indique &\# 0034 ; Normal&\# 0034 ;; &\# 0034 ; 1&\# 0034 ; indique &\# 0034 ; Soft&\# 0034 ;; &\# 0034 ; 2&\# 0034 ; indique &\# 0034 ;&dur \# 0034 ;.
ms.assetid: 32f89149-b90d-4fe9-9d1a-b8bb966d62fe
title: System. photo. Contrast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4117f13d35a352971a5f9b9f8685816f8ffbd1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517674"
---
# <a name="systemphotocontrast"></a><span data-ttu-id="c3632-104">System. photo. Contrast</span><span class="sxs-lookup"><span data-stu-id="c3632-104">System.Photo.Contrast</span></span>

<span data-ttu-id="c3632-105">Indique la direction du traitement du contraste appliquée par l’appareil photo lorsque l’image a été prise.</span><span class="sxs-lookup"><span data-stu-id="c3632-105">Indicates the direction of contrast processing applied by the camera when the image was taken.</span></span> <span data-ttu-id="c3632-106">« 0 » indique « normal ». « 1 » indique « Soft »; « 2 » indique « Hard ».</span><span class="sxs-lookup"><span data-stu-id="c3632-106">"0" indicates "Normal"; "1" indicates "Soft"; "2" indicates "Hard".</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="c3632-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="c3632-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.Contrast
   shellPKey = PKEY_Photo_Contrast
   formatID = 2A785BA9-8D23-4DED-82E6-60A350C86A10
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Normal
            value = 0
            text = Normal
            defineToken = PHOTO_CONTRAST_NORMAL
         enum
            name = Soft
            value = 1
            text = Soft
            defineToken = PHOTO_CONTRAST_SOFT
         enum
            name = Hard
            value = 2
            text = Hard
            defineToken = PHOTO_CONTRAST_HARD
```

## <a name="windows-vista"></a><span data-ttu-id="c3632-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c3632-108">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.Contrast
   shellPKey = PKEY_Photo_Contrast
   formatID = 2A785BA9-8D23-4DED-82E6-60A350C86A10
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Normal
            defineName = PHOTO_CONTRAST_NORMAL
         enum
            value = 1
            text = Soft
            defineName = PHOTO_CONTRAST_SOFT
         enum
            value = 2
            text = Hard
            defineName = PHOTO_CONTRAST_HARD
```

## <a name="remarks"></a><span data-ttu-id="c3632-109">Notes</span><span class="sxs-lookup"><span data-stu-id="c3632-109">Remarks</span></span>

<span data-ttu-id="c3632-110">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="c3632-110">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3632-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c3632-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3632-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="c3632-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="c3632-113">searchInfo</span><span class="sxs-lookup"><span data-stu-id="c3632-113">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="c3632-114">labelInfo</span><span class="sxs-lookup"><span data-stu-id="c3632-114">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="c3632-115">typeInfo</span><span class="sxs-lookup"><span data-stu-id="c3632-115">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="c3632-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="c3632-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="c3632-117">stringFormat</span><span class="sxs-lookup"><span data-stu-id="c3632-117">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="c3632-118">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="c3632-118">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="c3632-119">numberFormat</span><span class="sxs-lookup"><span data-stu-id="c3632-119">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="c3632-120">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="c3632-120">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="c3632-121">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="c3632-121">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="c3632-122">drawControl</span><span class="sxs-lookup"><span data-stu-id="c3632-122">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="c3632-123">editControl</span><span class="sxs-lookup"><span data-stu-id="c3632-123">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="c3632-124">filterControl</span><span class="sxs-lookup"><span data-stu-id="c3632-124">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="c3632-125">queryControl</span><span class="sxs-lookup"><span data-stu-id="c3632-125">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
