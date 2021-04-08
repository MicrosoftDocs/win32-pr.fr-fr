---
description: Si \_ la valeur est true, le programme d’installation de l’appareil installe actuellement le logiciel.
ms.assetid: 7C62C1E3-D3F3-49ce-A19D-B3A1C14E24D6
title: System. Devices. IsSoftwareInstalling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ba8b61b2c2a11c6e35efb9bafaae69aeb3d01d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034442"
---
# <a name="systemdevicesissoftwareinstalling"></a><span data-ttu-id="6dd21-103">System. Devices. IsSoftwareInstalling</span><span class="sxs-lookup"><span data-stu-id="6dd21-103">System.Devices.IsSoftwareInstalling</span></span>

<span data-ttu-id="6dd21-104">Si \_ la valeur est true, le programme d’installation de l’appareil installe actuellement le logiciel.</span><span class="sxs-lookup"><span data-stu-id="6dd21-104">If VARIANT\_TRUE, the device installer is currently installing software.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="6dd21-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="6dd21-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.Devices.IsSoftwareInstalling
   shellPKey = PKEY_Devices_IsSoftwareInstalling
   formatID = 83DA6326-97A6-4088-9453-A1923F573B29
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = SoftwareInstalling
            value = #TRUE#
            text = Device setup in progress
            defineToken = ISSOFTWAREINSTALLING_INSTALLING
```

## <a name="windows-7"></a><span data-ttu-id="6dd21-106">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6dd21-106">Windows 7</span></span>

```
propertyDescription
   name = System.Devices.IsSoftwareInstalling
   shellPKey = PKEY_Devices_IsSoftwareInstalling
   formatID = 83DA6326-97A6-4088-9453-A1923F573B29
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = SoftwareInstalling
            value = #TRUE#
            text = Software is installing for this device
            defineToken = ISSOFTWAREINSTALLING_INSTALLING
```

## <a name="remarks"></a><span data-ttu-id="6dd21-107">Notes</span><span class="sxs-lookup"><span data-stu-id="6dd21-107">Remarks</span></span>

<span data-ttu-id="6dd21-108">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="6dd21-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6dd21-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6dd21-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6dd21-110">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="6dd21-110">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="6dd21-111">searchInfo</span><span class="sxs-lookup"><span data-stu-id="6dd21-111">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="6dd21-112">labelInfo</span><span class="sxs-lookup"><span data-stu-id="6dd21-112">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="6dd21-113">typeInfo</span><span class="sxs-lookup"><span data-stu-id="6dd21-113">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="6dd21-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="6dd21-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="6dd21-115">stringFormat</span><span class="sxs-lookup"><span data-stu-id="6dd21-115">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="6dd21-116">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="6dd21-116">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="6dd21-117">numberFormat</span><span class="sxs-lookup"><span data-stu-id="6dd21-117">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="6dd21-118">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="6dd21-118">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="6dd21-119">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="6dd21-119">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="6dd21-120">drawControl</span><span class="sxs-lookup"><span data-stu-id="6dd21-120">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="6dd21-121">editControl</span><span class="sxs-lookup"><span data-stu-id="6dd21-121">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="6dd21-122">filterControl</span><span class="sxs-lookup"><span data-stu-id="6dd21-122">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="6dd21-123">queryControl</span><span class="sxs-lookup"><span data-stu-id="6dd21-123">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
