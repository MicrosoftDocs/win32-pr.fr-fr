---
description: Si cette propriété a la valeur true, l’appareil est un appareil partagé.
ms.assetid: d1da0747-ad07-49e5-8082-5f39bf0a84d8
title: System. Devices. IsShared
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f41cf4f6ad2988a21e30c0c67101b2582699704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321130"
---
# <a name="systemdevicesisshared"></a><span data-ttu-id="e363e-103">System. Devices. IsShared</span><span class="sxs-lookup"><span data-stu-id="e363e-103">System.Devices.IsShared</span></span>

<span data-ttu-id="e363e-104">Si cette propriété a la valeur true, l’appareil est un appareil partagé.</span><span class="sxs-lookup"><span data-stu-id="e363e-104">If this property is true, the device is a shared device.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="e363e-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="e363e-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.Devices.IsShared
   shellPKey = PKEY_Devices_IsShared
   formatID = 78C34FC8-104A-4ACA-9EA4-524D52996E57
   propID = 84
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Shared
            value = #TRUE#
            text = Shared
            defineToken = ISSHAREDDEVICE_SHARED
         enum
            name = NotShared
            value = #FALSE#
            text = Not Shared
            defineToken = ISSHAREDDEVICE_NOTSHARED
```

## <a name="windows-7"></a><span data-ttu-id="e363e-106">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e363e-106">Windows 7</span></span>

```
propertyDescription
   name = System.Devices.IsShared
   shellPKey = PKEY_Devices_IsSharedDevice
   formatID = 78C34FC8-104A-4ACA-9EA4-524D52996E57
   propID = 84
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Shared
            value = #TRUE#
            text = Shared
            defineToken = ISSHAREDDEVICE_SHARED
         enum
            name = NotShared
            value = #FALSE#
            text = Not Shared
            defineToken = ISSHAREDDEVICE_NOTSHARED
```

## <a name="remarks"></a><span data-ttu-id="e363e-107">Notes</span><span class="sxs-lookup"><span data-stu-id="e363e-107">Remarks</span></span>

<span data-ttu-id="e363e-108">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="e363e-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e363e-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e363e-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e363e-110">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="e363e-110">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="e363e-111">searchInfo</span><span class="sxs-lookup"><span data-stu-id="e363e-111">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="e363e-112">labelInfo</span><span class="sxs-lookup"><span data-stu-id="e363e-112">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="e363e-113">typeInfo</span><span class="sxs-lookup"><span data-stu-id="e363e-113">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="e363e-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="e363e-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="e363e-115">stringFormat</span><span class="sxs-lookup"><span data-stu-id="e363e-115">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="e363e-116">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="e363e-116">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="e363e-117">numberFormat</span><span class="sxs-lookup"><span data-stu-id="e363e-117">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="e363e-118">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="e363e-118">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="e363e-119">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="e363e-119">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="e363e-120">drawControl</span><span class="sxs-lookup"><span data-stu-id="e363e-120">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="e363e-121">editControl</span><span class="sxs-lookup"><span data-stu-id="e363e-121">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="e363e-122">filterControl</span><span class="sxs-lookup"><span data-stu-id="e363e-122">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="e363e-123">queryControl</span><span class="sxs-lookup"><span data-stu-id="e363e-123">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
