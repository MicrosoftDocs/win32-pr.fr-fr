---
description: Null indique le cas normal (le fichier est disponible hors connexion). La casse partielle est uniquement réservée aux dossiers dans lesquels du contenu peut être disponible hors connexion, et certains ne le peuvent pas.
ms.assetid: 46b03632-702e-46df-8204-33ada85adbee
title: System. FileOfflineAvailabilityStatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ca5c3f004c89cfb7b8625f9eb939a42f7fe842
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865558"
---
# <a name="systemfileofflineavailabilitystatus"></a><span data-ttu-id="54e91-104">System. FileOfflineAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="54e91-104">System.FileOfflineAvailabilityStatus</span></span>

<span data-ttu-id="54e91-105">Null indique le cas normal (le fichier est disponible hors connexion).</span><span class="sxs-lookup"><span data-stu-id="54e91-105">Null indicates the normal case (file is available offline).</span></span> <span data-ttu-id="54e91-106">La casse partielle est uniquement réservée aux dossiers dans lesquels du contenu peut être disponible hors connexion, et certains ne le peuvent pas.</span><span class="sxs-lookup"><span data-stu-id="54e91-106">The partial case is only for folders where some content may be available offline and some may not.</span></span>

## <a name="windows-10-version-1703"></a><span data-ttu-id="54e91-107">Windows 10 version 1703</span><span class="sxs-lookup"><span data-stu-id="54e91-107">Windows 10, version 1703</span></span>

```
propertyDescription
   name = System.FileOfflineAvailabilityStatus
   shellPKey = PKEY_FileOfflineAvailabilityStatus
   formatID = FCEFF153-E839-4CF3-A9E7-EA22832094B8
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotAvailableOffline
            value = 0
            text = NotAvailableOffline
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_NOTAVAILABLEOFFLINE
         enum
            name = PartiallyAvailableOffline
            value = 1
            text = PartiallyAvailableOffline
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_PARTIAL
         enum
            name = Complete
            value = 2
            text = Complete
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_COMPLETE
         enum
            name = CompletePinned
            value = 3
            text = CompletePinned
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_COMPLETE_PINNED
         enum
            name = Excluded
            value = 4
            text = Excluded
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_EXCLUDED
         enum
            name = Empty
            value = 5
            text = Empty
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_FOLDER_EMPTY
```

## <a name="windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a><span data-ttu-id="54e91-108">Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="54e91-108">Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1</span></span>

```
propertyDescription
   name = System.FileOfflineAvailabilityStatus
   shellPKey = PKEY_FileOfflineAvailabilityStatus
   formatID = FCEFF153-E839-4CF3-A9E7-EA22832094B8
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotAvailableOffline
            value = 0
            text = NotAvailableOffline
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_PROP_NOTAVAILABLEOFFLINE
         enum
            name = PartiallyAvailableOffline
            value = 1
            text = PartiallyAvailableOffline
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_PROP_PARTIALLYAVAILABLEOFFLINE
```

## <a name="remarks"></a><span data-ttu-id="54e91-109">Notes</span><span class="sxs-lookup"><span data-stu-id="54e91-109">Remarks</span></span>

<span data-ttu-id="54e91-110">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="54e91-110">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54e91-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="54e91-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54e91-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="54e91-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="54e91-113">searchInfo</span><span class="sxs-lookup"><span data-stu-id="54e91-113">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="54e91-114">labelInfo</span><span class="sxs-lookup"><span data-stu-id="54e91-114">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="54e91-115">typeInfo</span><span class="sxs-lookup"><span data-stu-id="54e91-115">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="54e91-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="54e91-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="54e91-117">stringFormat</span><span class="sxs-lookup"><span data-stu-id="54e91-117">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="54e91-118">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="54e91-118">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="54e91-119">numberFormat</span><span class="sxs-lookup"><span data-stu-id="54e91-119">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="54e91-120">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="54e91-120">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="54e91-121">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="54e91-121">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="54e91-122">drawControl</span><span class="sxs-lookup"><span data-stu-id="54e91-122">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="54e91-123">editControl</span><span class="sxs-lookup"><span data-stu-id="54e91-123">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="54e91-124">filterControl</span><span class="sxs-lookup"><span data-stu-id="54e91-124">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="54e91-125">queryControl</span><span class="sxs-lookup"><span data-stu-id="54e91-125">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
