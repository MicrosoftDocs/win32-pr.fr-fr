---
description: Chemin d’accès d’affichage convivial du dossier parent d’un élément.
ms.assetid: f60b7465-bca4-4c7b-9caf-9cda1bf6eeeb
title: System. ItemFolderPathDisplayNarrow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898927c23aae95b5037919c908a3ae86e020e1fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034585"
---
# <a name="systemitemfolderpathdisplaynarrow"></a><span data-ttu-id="47d99-103">System. ItemFolderPathDisplayNarrow</span><span class="sxs-lookup"><span data-stu-id="47d99-103">System.ItemFolderPathDisplayNarrow</span></span>

<span data-ttu-id="47d99-104">Chemin d’accès d’affichage convivial du dossier parent d’un élément.</span><span class="sxs-lookup"><span data-stu-id="47d99-104">The user-friendly display path of an item's parent folder.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="47d99-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47d99-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemFolderPathDisplayNarrow
   shellPKey = PKEY_ItemFolderPathDisplayNarrow
   formatID = DABD30ED-0043-4789-A7F8-D013A4736622
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="47d99-106">Notes</span><span class="sxs-lookup"><span data-stu-id="47d99-106">Remarks</span></span>

<span data-ttu-id="47d99-107">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="47d99-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="47d99-108">Le format de la chaîne doit être adapté afin que le nom du dossier se présente en premier, afin d’optimiser une colonne d’affichage étroite.</span><span class="sxs-lookup"><span data-stu-id="47d99-108">The format of the string should be tailored so that the folder name comes first, to optimize for a narrow viewing column.</span></span> <span data-ttu-id="47d99-109">Si le dossier est un dossier de fichiers, la valeur comprend tous les noms localisés.</span><span class="sxs-lookup"><span data-stu-id="47d99-109">If the folder is a file folder, the value includes any localized names.</span></span> <span data-ttu-id="47d99-110">Si [System. ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) est un VT \_ vide, cette propriété doit également être vide.</span><span class="sxs-lookup"><span data-stu-id="47d99-110">If [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) is VT\_EMPTY, then this property should also be empty.</span></span> <span data-ttu-id="47d99-111">Dans le cas contraire, elle doit être dérivée de manière appropriée par la source de données à partir de System. ItemFolderPathDisplay.</span><span class="sxs-lookup"><span data-stu-id="47d99-111">Otherwise, it should be derived appropriately by the data source from System.ItemFolderPathDisplay.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47d99-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="47d99-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47d99-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="47d99-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="47d99-114">searchInfo</span><span class="sxs-lookup"><span data-stu-id="47d99-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="47d99-115">labelInfo</span><span class="sxs-lookup"><span data-stu-id="47d99-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="47d99-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="47d99-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="47d99-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="47d99-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="47d99-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="47d99-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="47d99-119">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="47d99-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="47d99-120">numberFormat</span><span class="sxs-lookup"><span data-stu-id="47d99-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="47d99-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="47d99-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="47d99-122">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="47d99-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="47d99-123">drawControl</span><span class="sxs-lookup"><span data-stu-id="47d99-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="47d99-124">editControl</span><span class="sxs-lookup"><span data-stu-id="47d99-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="47d99-125">filterControl</span><span class="sxs-lookup"><span data-stu-id="47d99-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="47d99-126">queryControl</span><span class="sxs-lookup"><span data-stu-id="47d99-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
