---
description: Identifie l’extension de fichier de l’élément basé sur un fichier, y compris le point de début.
ms.assetid: b72c695e-bdbd-471d-b902-9e30a62facd4
title: System. FileExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf8792a3965c394a1944985515df527e41e3a159
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517815"
---
# <a name="systemfileextension"></a><span data-ttu-id="d0e09-103">System. FileExtension</span><span class="sxs-lookup"><span data-stu-id="d0e09-103">System.FileExtension</span></span>

<span data-ttu-id="d0e09-104">Identifie l’extension de fichier de l’élément basé sur un fichier, y compris le point de début.</span><span class="sxs-lookup"><span data-stu-id="d0e09-104">Identifies the file extension of the file-based item, including the leading period.</span></span> <span data-ttu-id="d0e09-105">Cette propriété est dérivée de System. FileName.</span><span class="sxs-lookup"><span data-stu-id="d0e09-105">This property is derived from System.FileName.</span></span> <span data-ttu-id="d0e09-106">Si System. FileName n’a pas d’extension de fichier ou si VT est \_ vide, la valeur de cette propriété doit être VT \_ vide.</span><span class="sxs-lookup"><span data-stu-id="d0e09-106">If System.FileName either does not have a file extension or is VT\_EMPTY, the value for this property should be VT\_EMPTY.</span></span>

<span data-ttu-id="d0e09-107">Pour obtenir le type d’un élément (y compris un élément qui n’est pas un fichier), utilisez System. ItemType.</span><span class="sxs-lookup"><span data-stu-id="d0e09-107">To obtain the type of any item (including an item that is not a file), use System.ItemType.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="d0e09-108">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0e09-108">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.FileExtension
   shellPKey = PKEY_FileExtension
   formatID = E4F10A3C-49E6-405D-8288-A23BD4EEAA6C
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="d0e09-109">Notes</span><span class="sxs-lookup"><span data-stu-id="d0e09-109">Remarks</span></span>

<span data-ttu-id="d0e09-110">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="d0e09-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="d0e09-111">Si [System. FileName](./props-system-filename.md) est un VT \_ vide, cette propriété doit également être vide.</span><span class="sxs-lookup"><span data-stu-id="d0e09-111">If [System.FileName](./props-system-filename.md) is VT\_EMPTY, this property should also be empty.</span></span> <span data-ttu-id="d0e09-112">Sinon, cette propriété doit être dérivée de manière appropriée par la source de données à partir de System. FileName.</span><span class="sxs-lookup"><span data-stu-id="d0e09-112">Otherwise, this property should be derived appropriately by the data source from System.FileName.</span></span> <span data-ttu-id="d0e09-113">Si System. FileName n’inclut pas d’extension de fichier, [System. FileExtension]() doit être VT \_ vide.</span><span class="sxs-lookup"><span data-stu-id="d0e09-113">If System.FileName does not include a file extension, [System.FileExtension]() should be VT\_EMPTY.</span></span> <span data-ttu-id="d0e09-114">Pour obtenir le type d’un élément (y compris un élément qui n’est pas un fichier), utilisez [System. ItemType](./props-system-itemtype.md).</span><span class="sxs-lookup"><span data-stu-id="d0e09-114">To obtain the type of any item (including an item that is not a file), use [System.ItemType](./props-system-itemtype.md).</span></span>

<span data-ttu-id="d0e09-115">Exemples de propriétés de chemin d’accès et d’extension de fichier.</span><span class="sxs-lookup"><span data-stu-id="d0e09-115">Path and file extension property examples.</span></span> 

| <span data-ttu-id="d0e09-116">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="d0e09-116">Path</span></span>                               | <span data-ttu-id="d0e09-117">Extension de fichier</span><span class="sxs-lookup"><span data-stu-id="d0e09-117">File Extension</span></span> |
|------------------------------------|----------------|
| <span data-ttu-id="d0e09-118">c : \\ fichiers \\ \\hello.txt personnels</span><span class="sxs-lookup"><span data-stu-id="d0e09-118">c:\\files\\personal\\hello.txt</span></span>     | <span data-ttu-id="d0e09-119">.txt</span><span class="sxs-lookup"><span data-stu-id="d0e09-119">.txt</span></span>           |
| <span data-ttu-id="d0e09-120">\\\\news.doc du partage de serveur \\ \\ mydir \\</span><span class="sxs-lookup"><span data-stu-id="d0e09-120">\\\\server\\share\\mydir\\news.doc</span></span> | <span data-ttu-id="d0e09-121">.doc</span><span class="sxs-lookup"><span data-stu-id="d0e09-121">.doc</span></span>           |
| <span data-ttu-id="d0e09-122">\\\\\\numbers.xls de partage de serveur \\</span><span class="sxs-lookup"><span data-stu-id="d0e09-122">\\\\server\\share\\numbers.xls</span></span>     | <span data-ttu-id="d0e09-123">.xls</span><span class="sxs-lookup"><span data-stu-id="d0e09-123">.xls</span></span>           |
| <span data-ttu-id="d0e09-124">\\\\\\dossier partage du serveur \\</span><span class="sxs-lookup"><span data-stu-id="d0e09-124">\\\\server\\share\\folder</span></span>          | <span data-ttu-id="d0e09-125">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="d0e09-125">VT\_EMPTY</span></span>      |
| <span data-ttu-id="d0e09-126">c : \\ Stuff \\</span><span class="sxs-lookup"><span data-stu-id="d0e09-126">c:\\Stuff\\MyFolder</span></span>                | <span data-ttu-id="d0e09-127">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="d0e09-127">VT\_EMPTY</span></span>      |
| <span data-ttu-id="d0e09-128">\[desktop\]</span><span class="sxs-lookup"><span data-stu-id="d0e09-128">\[desktop\]</span></span>                        | <span data-ttu-id="d0e09-129">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="d0e09-129">VT\_EMPTY</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="d0e09-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d0e09-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0e09-131">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="d0e09-131">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="d0e09-132">searchInfo</span><span class="sxs-lookup"><span data-stu-id="d0e09-132">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="d0e09-133">labelInfo</span><span class="sxs-lookup"><span data-stu-id="d0e09-133">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="d0e09-134">typeInfo</span><span class="sxs-lookup"><span data-stu-id="d0e09-134">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="d0e09-135">displayInfo</span><span class="sxs-lookup"><span data-stu-id="d0e09-135">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="d0e09-136">stringFormat</span><span class="sxs-lookup"><span data-stu-id="d0e09-136">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="d0e09-137">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="d0e09-137">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="d0e09-138">numberFormat</span><span class="sxs-lookup"><span data-stu-id="d0e09-138">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="d0e09-139">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="d0e09-139">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="d0e09-140">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="d0e09-140">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="d0e09-141">drawControl</span><span class="sxs-lookup"><span data-stu-id="d0e09-141">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="d0e09-142">editControl</span><span class="sxs-lookup"><span data-stu-id="d0e09-142">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="d0e09-143">filterControl</span><span class="sxs-lookup"><span data-stu-id="d0e09-143">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="d0e09-144">queryControl</span><span class="sxs-lookup"><span data-stu-id="d0e09-144">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
