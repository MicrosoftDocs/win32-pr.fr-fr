---
description: Chemin d’accès d’affichage convivial du dossier parent d’un élément.
ms.assetid: 16f67edc-ca8a-4c2e-9d9b-be8600446e51
title: System. ItemFolderPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c4ae4c9178356d36c644f1bc886d63331155e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518449"
---
# <a name="systemitemfolderpathdisplay"></a><span data-ttu-id="ec33f-103">System. ItemFolderPathDisplay</span><span class="sxs-lookup"><span data-stu-id="ec33f-103">System.ItemFolderPathDisplay</span></span>

<span data-ttu-id="ec33f-104">Chemin d’accès d’affichage convivial du dossier parent d’un élément.</span><span class="sxs-lookup"><span data-stu-id="ec33f-104">The user-friendly display path of an item's parent folder.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="ec33f-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ec33f-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemFolderPathDisplay
   shellPKey = PKEY_ItemFolderPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 6
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="ec33f-106">Notes</span><span class="sxs-lookup"><span data-stu-id="ec33f-106">Remarks</span></span>

<span data-ttu-id="ec33f-107">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="ec33f-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="ec33f-108">Si [System. ItemPathDisplay](./props-system-itempathdisplay.md) est un VT \_ vide, cette propriété doit également être vide.</span><span class="sxs-lookup"><span data-stu-id="ec33f-108">If [System.ItemPathDisplay](./props-system-itempathdisplay.md) is VT\_EMPTY, then this property should also be empty.</span></span> <span data-ttu-id="ec33f-109">Dans le cas contraire, elle doit être dérivée de manière appropriée par la source de données à partir de System. ItemPathDisplay.</span><span class="sxs-lookup"><span data-stu-id="ec33f-109">Otherwise, it should be derived appropriately by the data source from System.ItemPathDisplay.</span></span>

<span data-ttu-id="ec33f-110">Exemples de valeurs</span><span class="sxs-lookup"><span data-stu-id="ec33f-110">Example values:</span></span>



| <span data-ttu-id="ec33f-111">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="ec33f-111">Path</span></span>                                   | <span data-ttu-id="ec33f-112">ItemFolderPathDisplay</span><span class="sxs-lookup"><span data-stu-id="ec33f-112">ItemFolderPathDisplay</span></span>    |
|----------------------------------------|--------------------------|
| <span data-ttu-id="ec33f-113">c : \\ fichiers \\ \\hello.txt personnels</span><span class="sxs-lookup"><span data-stu-id="ec33f-113">c:\\files\\personal\\hello.txt</span></span>         | <span data-ttu-id="ec33f-114">c : \\ fichiers \\ personnels</span><span class="sxs-lookup"><span data-stu-id="ec33f-114">c:\\files\\personal</span></span>      |
| <span data-ttu-id="ec33f-115">\\\\goodnews.doc du partage de serveur \\ \\ mydir \\</span><span class="sxs-lookup"><span data-stu-id="ec33f-115">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="ec33f-116">\\\\\\mydir de partage de serveur \\</span><span class="sxs-lookup"><span data-stu-id="ec33f-116">\\\\server\\share\\mydir</span></span> |
| <span data-ttu-id="ec33f-117">\\\\\\numbers.xls de partage de serveur \\</span><span class="sxs-lookup"><span data-stu-id="ec33f-117">\\\\server\\share\\numbers.xls</span></span>         | <span data-ttu-id="ec33f-118">\\\\partage de serveur \\</span><span class="sxs-lookup"><span data-stu-id="ec33f-118">\\\\server\\share</span></span>        |
| <span data-ttu-id="ec33f-119">c : \\ nourriture \\ mondossier</span><span class="sxs-lookup"><span data-stu-id="ec33f-119">c:\\food\\MyFolder</span></span>                     | <span data-ttu-id="ec33f-120">c : \\ nourriture</span><span class="sxs-lookup"><span data-stu-id="ec33f-120">c:\\food</span></span>                 |
| <span data-ttu-id="ec33f-121">Compte/Mailbox/boîte de réception/'re : Bonjour ! '</span><span class="sxs-lookup"><span data-stu-id="ec33f-121">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="ec33f-122">Compte/Mailbox/boîte de réception</span><span class="sxs-lookup"><span data-stu-id="ec33f-122">/Mailbox Account/Inbox</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="ec33f-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ec33f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec33f-124">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="ec33f-124">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="ec33f-125">searchInfo</span><span class="sxs-lookup"><span data-stu-id="ec33f-125">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="ec33f-126">labelInfo</span><span class="sxs-lookup"><span data-stu-id="ec33f-126">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="ec33f-127">typeInfo</span><span class="sxs-lookup"><span data-stu-id="ec33f-127">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="ec33f-128">displayInfo</span><span class="sxs-lookup"><span data-stu-id="ec33f-128">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="ec33f-129">stringFormat</span><span class="sxs-lookup"><span data-stu-id="ec33f-129">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="ec33f-130">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="ec33f-130">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="ec33f-131">numberFormat</span><span class="sxs-lookup"><span data-stu-id="ec33f-131">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="ec33f-132">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="ec33f-132">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="ec33f-133">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="ec33f-133">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="ec33f-134">drawControl</span><span class="sxs-lookup"><span data-stu-id="ec33f-134">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="ec33f-135">editControl</span><span class="sxs-lookup"><span data-stu-id="ec33f-135">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="ec33f-136">filterControl</span><span class="sxs-lookup"><span data-stu-id="ec33f-136">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="ec33f-137">queryControl</span><span class="sxs-lookup"><span data-stu-id="ec33f-137">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
