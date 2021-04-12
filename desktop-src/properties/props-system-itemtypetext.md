---
description: Nom de type convivial de l’élément.
ms.assetid: 5d4c86da-6317-4a34-88d6-caf794aaa165
title: System. ItemTypeText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699a953392054cb2344c5f3b3d652e64a9a2c1f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202617"
---
# <a name="systemitemtypetext"></a><span data-ttu-id="c3de2-103">System. ItemTypeText</span><span class="sxs-lookup"><span data-stu-id="c3de2-103">System.ItemTypeText</span></span>

<span data-ttu-id="c3de2-104">Nom de type convivial de l’élément.</span><span class="sxs-lookup"><span data-stu-id="c3de2-104">The user-friendly type name of the item.</span></span> <span data-ttu-id="c3de2-105">Cette valeur n’est pas destinée à être analysée par programmation.</span><span class="sxs-lookup"><span data-stu-id="c3de2-105">This value is not intended to be programmatically parsed.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="c3de2-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c3de2-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemTypeText
   shellPKey = PKEY_ItemTypeText
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 4
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="c3de2-107">Notes</span><span class="sxs-lookup"><span data-stu-id="c3de2-107">Remarks</span></span>

<span data-ttu-id="c3de2-108">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="c3de2-108">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="c3de2-109">Si [System. ItemType](./props-system-itemtype.md) est \_ un VT vide, la valeur de cette propriété est également une valeur VT \_ vide.</span><span class="sxs-lookup"><span data-stu-id="c3de2-109">If [System.ItemType](./props-system-itemtype.md) is VT\_EMPTY, the value of this property is also VT\_EMPTY.</span></span> <span data-ttu-id="c3de2-110">Si l’élément est un fichier, la valeur de cette propriété est la même que si vous avez passé la valeur System. ItemType du fichier à [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay).</span><span class="sxs-lookup"><span data-stu-id="c3de2-110">If the item is a file, the value of this property is the same as if you passed the file's System.ItemType value to [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay).</span></span>

<span data-ttu-id="c3de2-111">Cette propriété ne doit pas être confondue avec [System. Kind](./props-system-kind.md), qui est un nom de type de haut niveau et convivial.</span><span class="sxs-lookup"><span data-stu-id="c3de2-111">This property should not be confused with [System.Kind](./props-system-kind.md), which is a high-level, user-friendly kind name.</span></span> <span data-ttu-id="c3de2-112">Par exemple, pour un fichier de document. doc, les différentes propriétés sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="c3de2-112">For example, for a .doc document file, the various properties are as shown here:</span></span>



| <span data-ttu-id="c3de2-113">Propriété</span><span class="sxs-lookup"><span data-stu-id="c3de2-113">Property</span></span>                                               | <span data-ttu-id="c3de2-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3de2-114">Value</span></span>                   |
|--------------------------------------------------------|-------------------------|
| [<span data-ttu-id="c3de2-115">System. Kind</span><span class="sxs-lookup"><span data-stu-id="c3de2-115">System.Kind</span></span>](./props-system-kind.md)                 | <span data-ttu-id="c3de2-116">Document</span><span class="sxs-lookup"><span data-stu-id="c3de2-116">Document</span></span>                |
| [<span data-ttu-id="c3de2-117">System. ItemType</span><span class="sxs-lookup"><span data-stu-id="c3de2-117">System.ItemType</span></span>](./props-system-itemtype.md)         | <span data-ttu-id="c3de2-118">.doc</span><span class="sxs-lookup"><span data-stu-id="c3de2-118">.doc</span></span>                    |
| [<span data-ttu-id="c3de2-119">System. ItemTypeText</span><span class="sxs-lookup"><span data-stu-id="c3de2-119">System.ItemTypeText</span></span>]() | <span data-ttu-id="c3de2-120">Document Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="c3de2-120">Microsoft Word Document</span></span> |



 

<span data-ttu-id="c3de2-121">Exemples de valeurs</span><span class="sxs-lookup"><span data-stu-id="c3de2-121">Example values:</span></span>



| <span data-ttu-id="c3de2-122">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c3de2-122">Path</span></span>                                   | <span data-ttu-id="c3de2-123">ItemTypeText</span><span class="sxs-lookup"><span data-stu-id="c3de2-123">ItemTypeText</span></span>            |
|----------------------------------------|-------------------------|
| <span data-ttu-id="c3de2-124">c : \\hello.txt de la \\ barre mydir \\</span><span class="sxs-lookup"><span data-stu-id="c3de2-124">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="c3de2-125">Fichier texte</span><span class="sxs-lookup"><span data-stu-id="c3de2-125">Text File</span></span>               |
| <span data-ttu-id="c3de2-126">\\\\goodnews.doc du partage de serveur \\ \\ mydir \\</span><span class="sxs-lookup"><span data-stu-id="c3de2-126">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="c3de2-127">Document Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="c3de2-127">Microsoft Word Document</span></span> |
| <span data-ttu-id="c3de2-128">\\\\\\dossier partage du serveur \\</span><span class="sxs-lookup"><span data-stu-id="c3de2-128">\\\\server\\share\\folder</span></span>              | <span data-ttu-id="c3de2-129">Dossier de fichiers</span><span class="sxs-lookup"><span data-stu-id="c3de2-129">File Folder</span></span>             |
| <span data-ttu-id="c3de2-130">c : \\ mydir \\ mondossier</span><span class="sxs-lookup"><span data-stu-id="c3de2-130">c:\\MyDir\\MyFolder</span></span>                    | <span data-ttu-id="c3de2-131">Dossier de fichiers</span><span class="sxs-lookup"><span data-stu-id="c3de2-131">File Folder</span></span>             |
| <span data-ttu-id="c3de2-132">Compte/Mailbox/boîte de réception/'re : Bonjour ! '</span><span class="sxs-lookup"><span data-stu-id="c3de2-132">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="c3de2-133">Message électronique Outlook</span><span class="sxs-lookup"><span data-stu-id="c3de2-133">Outlook E-Mail Message</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="c3de2-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c3de2-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3de2-135">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="c3de2-135">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="c3de2-136">searchInfo</span><span class="sxs-lookup"><span data-stu-id="c3de2-136">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="c3de2-137">labelInfo</span><span class="sxs-lookup"><span data-stu-id="c3de2-137">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="c3de2-138">typeInfo</span><span class="sxs-lookup"><span data-stu-id="c3de2-138">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="c3de2-139">displayInfo</span><span class="sxs-lookup"><span data-stu-id="c3de2-139">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="c3de2-140">stringFormat</span><span class="sxs-lookup"><span data-stu-id="c3de2-140">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="c3de2-141">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="c3de2-141">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="c3de2-142">numberFormat</span><span class="sxs-lookup"><span data-stu-id="c3de2-142">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="c3de2-143">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="c3de2-143">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="c3de2-144">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="c3de2-144">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="c3de2-145">drawControl</span><span class="sxs-lookup"><span data-stu-id="c3de2-145">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="c3de2-146">editControl</span><span class="sxs-lookup"><span data-stu-id="c3de2-146">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="c3de2-147">filterControl</span><span class="sxs-lookup"><span data-stu-id="c3de2-147">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="c3de2-148">queryControl</span><span class="sxs-lookup"><span data-stu-id="c3de2-148">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
