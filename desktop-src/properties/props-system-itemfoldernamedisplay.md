---
description: Nom complet convivial du dossier parent d’un élément.
ms.assetid: 4049b6cb-41a1-4df6-89d1-a2022d3a285d
title: System. ItemFolderNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d637412b02345b52fee2e1c13e8f499314af4c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203834"
---
# <a name="systemitemfoldernamedisplay"></a><span data-ttu-id="2527e-103">System. ItemFolderNameDisplay</span><span class="sxs-lookup"><span data-stu-id="2527e-103">System.ItemFolderNameDisplay</span></span>

<span data-ttu-id="2527e-104">Nom complet convivial du dossier parent d’un élément.</span><span class="sxs-lookup"><span data-stu-id="2527e-104">The user-friendly display name of an item's parent folder.</span></span>

<span data-ttu-id="2527e-105">Cela est dérivé de [System. ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md).</span><span class="sxs-lookup"><span data-stu-id="2527e-105">This is derived from [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md).</span></span> <span data-ttu-id="2527e-106">Si cette propriété est une propriété VT \_ vide, cette propriété doit être également.</span><span class="sxs-lookup"><span data-stu-id="2527e-106">If that property is VT\_EMPTY, then this property should be too.</span></span>

<span data-ttu-id="2527e-107">Si le dossier est un dossier de fichiers, la valeur sera localisée si un nom localisé est disponible.</span><span class="sxs-lookup"><span data-stu-id="2527e-107">If the folder is a file folder, the value will be localized if a localized name is available.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="2527e-108">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2527e-108">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemFolderNameDisplay
   shellPKey = PKEY_ItemFolderNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 2
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="2527e-109">Notes</span><span class="sxs-lookup"><span data-stu-id="2527e-109">Remarks</span></span>

<span data-ttu-id="2527e-110">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="2527e-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="2527e-111">Si [System. ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) est un VT \_ vide, cette propriété doit également être vide.</span><span class="sxs-lookup"><span data-stu-id="2527e-111">If [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) is VT\_EMPTY, then this property should also be empty.</span></span> <span data-ttu-id="2527e-112">Dans le cas contraire, elle doit être dérivée de manière appropriée par la source de données à partir de System. ItemFolderPathDisplay.</span><span class="sxs-lookup"><span data-stu-id="2527e-112">Otherwise, it should be derived appropriately by the data source from System.ItemFolderPathDisplay.</span></span>

<span data-ttu-id="2527e-113">Exemples :</span><span class="sxs-lookup"><span data-stu-id="2527e-113">Examples:</span></span>



| <span data-ttu-id="2527e-114">Chemin d’accès donné</span><span class="sxs-lookup"><span data-stu-id="2527e-114">Given path</span></span>                             | <span data-ttu-id="2527e-115">Nom complet du dossier</span><span class="sxs-lookup"><span data-stu-id="2527e-115">Folder Display Name</span></span> |
|----------------------------------------|---------------------|
| <span data-ttu-id="2527e-116">c : \\ myfiles \\ texte \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="2527e-116">c:\\MyFiles\\Text\\hello.txt</span></span>           | <span data-ttu-id="2527e-117">Texte</span><span class="sxs-lookup"><span data-stu-id="2527e-117">Text</span></span>                |
| <span data-ttu-id="2527e-118">\\\\goodnews.doc du partage de serveur \\ \\ mydir \\</span><span class="sxs-lookup"><span data-stu-id="2527e-118">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="2527e-119">mydir</span><span class="sxs-lookup"><span data-stu-id="2527e-119">mydir</span></span>               |
| <span data-ttu-id="2527e-120">\\\\\\numbers.xls de partage de serveur \\</span><span class="sxs-lookup"><span data-stu-id="2527e-120">\\\\server\\share\\numbers.xls</span></span>         | <span data-ttu-id="2527e-121">partager</span><span class="sxs-lookup"><span data-stu-id="2527e-121">share</span></span>               |
| <span data-ttu-id="2527e-122">c : \\ dossiers \\ mondossier</span><span class="sxs-lookup"><span data-stu-id="2527e-122">c:\\Folders\\MyFolder</span></span>                  | <span data-ttu-id="2527e-123">Dossiers</span><span class="sxs-lookup"><span data-stu-id="2527e-123">Folders</span></span>             |
| <span data-ttu-id="2527e-124">Compte/Mailbox/boîte de réception/'re : Bonjour ! '</span><span class="sxs-lookup"><span data-stu-id="2527e-124">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="2527e-125">Inbox</span><span class="sxs-lookup"><span data-stu-id="2527e-125">Inbox</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="2527e-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2527e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2527e-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="2527e-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="2527e-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="2527e-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="2527e-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="2527e-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="2527e-130">typeInfo</span><span class="sxs-lookup"><span data-stu-id="2527e-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="2527e-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="2527e-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="2527e-132">stringFormat</span><span class="sxs-lookup"><span data-stu-id="2527e-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="2527e-133">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="2527e-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="2527e-134">numberFormat</span><span class="sxs-lookup"><span data-stu-id="2527e-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="2527e-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="2527e-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="2527e-136">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="2527e-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="2527e-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="2527e-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="2527e-138">editControl</span><span class="sxs-lookup"><span data-stu-id="2527e-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="2527e-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="2527e-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="2527e-140">queryControl</span><span class="sxs-lookup"><span data-stu-id="2527e-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
