---
description: Chemin d’accès d’affichage convivial de l’élément.
ms.assetid: 27e4490b-7914-4b38-9799-e9d5dc407f13
title: System. ItemPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb76a4218e7e7580ec70cb57dd16c635ca024ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115458"
---
# <a name="systemitempathdisplay"></a><span data-ttu-id="0ea80-103">System. ItemPathDisplay</span><span class="sxs-lookup"><span data-stu-id="0ea80-103">System.ItemPathDisplay</span></span>

<span data-ttu-id="0ea80-104">Chemin d’accès d’affichage convivial de l’élément.</span><span class="sxs-lookup"><span data-stu-id="0ea80-104">The user-friendly display path to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="0ea80-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0ea80-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemPathDisplay
   shellPKey = PKEY_ItemPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 7
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="0ea80-106">Notes</span><span class="sxs-lookup"><span data-stu-id="0ea80-106">Remarks</span></span>

<span data-ttu-id="0ea80-107">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="0ea80-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="0ea80-108">Si l’élément est un fichier ou un dossier, cette propriété comprend l’extension dans tous les cas, et est localisée si un nom localisé est disponible.</span><span class="sxs-lookup"><span data-stu-id="0ea80-108">If the item is a file or folder, this property includes the extension in all cases, and is localized if a localized name is available.</span></span> <span data-ttu-id="0ea80-109">Pour les autres éléments, il s’agit de l’équivalent convivial de l’utilisateur, en supposant que l’élément existe dans le stockage hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="0ea80-109">For other items, this is the user-friendly equivalent, assuming that the item exists in hierarchical storage.</span></span>

<span data-ttu-id="0ea80-110">Contrairement à [System. ItemUrl](./props-system-itemurl.md), cette valeur de propriété n’inclut pas le schéma d’URL.</span><span class="sxs-lookup"><span data-stu-id="0ea80-110">Unlike [System.ItemUrl](./props-system-itemurl.md), this property value does not include the URL scheme.</span></span> <span data-ttu-id="0ea80-111">Pour analyser un chemin d’accès à un élément, utilisez System. ItemUrl ou [System. ParsingPath](./props-system-parsingpath.md).</span><span class="sxs-lookup"><span data-stu-id="0ea80-111">To parse an item path, use System.ItemUrl or [System.ParsingPath](./props-system-parsingpath.md).</span></span> <span data-ttu-id="0ea80-112">Pour référencer des éléments d’espace de noms Shell à l’aide d’API Shell, utilisez System. ParsingPath.</span><span class="sxs-lookup"><span data-stu-id="0ea80-112">To reference Shell namespace items using Shell APIs, use System.ParsingPath.</span></span>

<span data-ttu-id="0ea80-113">Exemples de valeurs</span><span class="sxs-lookup"><span data-stu-id="0ea80-113">Example values:</span></span>



| <span data-ttu-id="0ea80-114">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="0ea80-114">Path</span></span>                                   | <span data-ttu-id="0ea80-115">ItemPathDisplay</span><span class="sxs-lookup"><span data-stu-id="0ea80-115">ItemPathDisplay</span></span>                        |
|----------------------------------------|----------------------------------------|
| <span data-ttu-id="0ea80-116">c : \\hello.txt de la \\ barre mydir \\</span><span class="sxs-lookup"><span data-stu-id="0ea80-116">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="0ea80-117">c : \\hello.txt de la \\ barre mydir \\</span><span class="sxs-lookup"><span data-stu-id="0ea80-117">c:\\mydir\\bar\\hello.txt</span></span>              |
| <span data-ttu-id="0ea80-118">\\\\goodnews.doc du partage de serveur \\ \\ mydir \\</span><span class="sxs-lookup"><span data-stu-id="0ea80-118">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="0ea80-119">\\\\goodnews.doc du partage de serveur \\ \\ mydir \\</span><span class="sxs-lookup"><span data-stu-id="0ea80-119">\\\\server\\share\\mydir\\goodnews.doc</span></span> |
| <span data-ttu-id="0ea80-120">\\\\\\numbers.xls de partage de serveur \\</span><span class="sxs-lookup"><span data-stu-id="0ea80-120">\\\\server\\share\\numbers.xls</span></span>         | <span data-ttu-id="0ea80-121">\\\\\\numbers.xls de partage de serveur \\</span><span class="sxs-lookup"><span data-stu-id="0ea80-121">\\\\server\\share\\numbers.xls</span></span>         |
| <span data-ttu-id="0ea80-122">c : \\ mydir \\ mondossier</span><span class="sxs-lookup"><span data-stu-id="0ea80-122">c:\\mydir\\MyFolder</span></span>                    | <span data-ttu-id="0ea80-123">c : \\ mydir \\ mondossier</span><span class="sxs-lookup"><span data-stu-id="0ea80-123">c:\\mydir\\MyFolder</span></span>                    |
| <span data-ttu-id="0ea80-124">Compte/Mailbox/boîte de réception/'re : Bonjour ! '</span><span class="sxs-lookup"><span data-stu-id="0ea80-124">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="0ea80-125">Compte/Mailbox/boîte de réception/'re : Bonjour ! '</span><span class="sxs-lookup"><span data-stu-id="0ea80-125">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="0ea80-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0ea80-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ea80-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="0ea80-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="0ea80-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="0ea80-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="0ea80-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="0ea80-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="0ea80-130">typeInfo</span><span class="sxs-lookup"><span data-stu-id="0ea80-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="0ea80-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="0ea80-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="0ea80-132">stringFormat</span><span class="sxs-lookup"><span data-stu-id="0ea80-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="0ea80-133">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="0ea80-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="0ea80-134">numberFormat</span><span class="sxs-lookup"><span data-stu-id="0ea80-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="0ea80-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="0ea80-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="0ea80-136">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="0ea80-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="0ea80-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="0ea80-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="0ea80-138">editControl</span><span class="sxs-lookup"><span data-stu-id="0ea80-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="0ea80-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="0ea80-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="0ea80-140">queryControl</span><span class="sxs-lookup"><span data-stu-id="0ea80-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
