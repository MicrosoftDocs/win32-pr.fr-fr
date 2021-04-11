---
description: Chemin d’accès d’affichage convivial de l’élément.
ms.assetid: 5dd44e13-bc5c-4e32-b5eb-2c7c40e10dfb
title: System. ItemPathDisplayNarrow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ef7b9d03a78a23e955c20f52e32062a8bcabd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209768"
---
# <a name="systemitempathdisplaynarrow"></a><span data-ttu-id="78490-103">System. ItemPathDisplayNarrow</span><span class="sxs-lookup"><span data-stu-id="78490-103">System.ItemPathDisplayNarrow</span></span>

<span data-ttu-id="78490-104">Chemin d’accès d’affichage convivial de l’élément.</span><span class="sxs-lookup"><span data-stu-id="78490-104">The user-friendly display path to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="78490-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78490-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemPathDisplayNarrow
   shellPKey = PKEY_ItemPathDisplayNarrow
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 8
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="78490-106">Notes</span><span class="sxs-lookup"><span data-stu-id="78490-106">Remarks</span></span>

<span data-ttu-id="78490-107">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="78490-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="78490-108">Pour optimiser pour une colonne d’affichage étroite, le format de la chaîne doit être adapté afin que le nom soit d’abord.</span><span class="sxs-lookup"><span data-stu-id="78490-108">To optimize for a narrow viewing column, the format of the string should be tailored so that the name comes first.</span></span>

<span data-ttu-id="78490-109">Si l’élément est un fichier, la valeur de la propriété exclut l’extension de fichier, mais inclut les noms localisés s’ils sont présents.</span><span class="sxs-lookup"><span data-stu-id="78490-109">If the item is a file, the property value excludes the file extension, but includes localized names if they are present.</span></span> <span data-ttu-id="78490-110">Si l’élément est un message, la valeur comprend [System. ItemNamePrefix](./props-system-itemnameprefix.md).</span><span class="sxs-lookup"><span data-stu-id="78490-110">If the item is a message, the value includes the [System.ItemNamePrefix](./props-system-itemnameprefix.md).</span></span> <span data-ttu-id="78490-111">Pour analyser un chemin d’accès à un élément, utilisez [System. ItemUrl](./props-system-itemurl.md) ou [System. ParsingPath](./props-system-parsingpath.md).</span><span class="sxs-lookup"><span data-stu-id="78490-111">To parse an item path, use [System.ItemUrl](./props-system-itemurl.md) or [System.ParsingPath](./props-system-parsingpath.md).</span></span>

<span data-ttu-id="78490-112">Exemples de valeurs</span><span class="sxs-lookup"><span data-stu-id="78490-112">Example values:</span></span>



| <span data-ttu-id="78490-113">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="78490-113">Path</span></span>                                   | <span data-ttu-id="78490-114">ItemPathDisplayName</span><span class="sxs-lookup"><span data-stu-id="78490-114">ItemPathDisplayName</span></span>                 |
|----------------------------------------|-------------------------------------|
| <span data-ttu-id="78490-115">c : \\hello.txt de la \\ barre mydir \\</span><span class="sxs-lookup"><span data-stu-id="78490-115">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="78490-116">Bonjour (c : \\ mydir \\ bar)</span><span class="sxs-lookup"><span data-stu-id="78490-116">hello (c:\\mydir\\bar)</span></span>              |
| <span data-ttu-id="78490-117">\\\\goodnews.doc du partage de serveur \\ \\ mydir \\</span><span class="sxs-lookup"><span data-stu-id="78490-117">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="78490-118">goodnews ( \\ \\ partage de serveur \\ \\ mydir)</span><span class="sxs-lookup"><span data-stu-id="78490-118">goodnews (\\\\server\\share\\mydir)</span></span> |
| <span data-ttu-id="78490-119">\\\\\\dossier partage du serveur \\</span><span class="sxs-lookup"><span data-stu-id="78490-119">\\\\server\\share\\folder</span></span>              | <span data-ttu-id="78490-120">dossier ( \\ \\ partage de serveur \\ )</span><span class="sxs-lookup"><span data-stu-id="78490-120">folder (\\\\server\\share)</span></span>          |
| <span data-ttu-id="78490-121">c : \\ mydir \\ mondossier</span><span class="sxs-lookup"><span data-stu-id="78490-121">c:\\MyDir\\MyFolder</span></span>                    | <span data-ttu-id="78490-122">Mondossier (c : \\ mydir)</span><span class="sxs-lookup"><span data-stu-id="78490-122">MyFolder (c:\\mydir)</span></span>                |
| <span data-ttu-id="78490-123">Compte/Mailbox/boîte de réception/'re : Bonjour ! '</span><span class="sxs-lookup"><span data-stu-id="78490-123">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="78490-124">Re : Bonjour !</span><span class="sxs-lookup"><span data-stu-id="78490-124">Re: Hello!</span></span> <span data-ttu-id="78490-125">(Compte/Mailbox/boîte de réception)</span><span class="sxs-lookup"><span data-stu-id="78490-125">(/Mailbox Account/Inbox)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="78490-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="78490-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78490-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="78490-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="78490-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="78490-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="78490-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="78490-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="78490-130">typeInfo</span><span class="sxs-lookup"><span data-stu-id="78490-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="78490-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="78490-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="78490-132">stringFormat</span><span class="sxs-lookup"><span data-stu-id="78490-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="78490-133">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="78490-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="78490-134">numberFormat</span><span class="sxs-lookup"><span data-stu-id="78490-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="78490-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="78490-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="78490-136">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="78490-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="78490-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="78490-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="78490-138">editControl</span><span class="sxs-lookup"><span data-stu-id="78490-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="78490-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="78490-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="78490-140">queryControl</span><span class="sxs-lookup"><span data-stu-id="78490-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
