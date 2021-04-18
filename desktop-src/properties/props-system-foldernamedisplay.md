---
description: Cette propriété est similaire à System. ItemNameDisplay, sauf qu’elle est définie uniquement pour les dossiers, mais pour les fichiers, elle sera vide.
ms.assetid: 4517a4bf-3cc1-4835-b21b-03de5b33db0c
title: System. FolderNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60922054e80a6589bcb04c3962a4527ee62eaf7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533950"
---
# <a name="systemfoldernamedisplay"></a><span data-ttu-id="92467-103">System. FolderNameDisplay</span><span class="sxs-lookup"><span data-stu-id="92467-103">System.FolderNameDisplay</span></span>

<span data-ttu-id="92467-104">Cette propriété est similaire à System. ItemNameDisplay, sauf qu’elle est définie uniquement pour les dossiers, mais pour les fichiers, elle sera vide.</span><span class="sxs-lookup"><span data-stu-id="92467-104">This property is similar to System.ItemNameDisplay except it is only set for folders, for files it will be empty.</span></span> <span data-ttu-id="92467-105">Cela est utile pour séparer les fichiers et les dossiers en utilisant ce comme première clé de tri.</span><span class="sxs-lookup"><span data-stu-id="92467-105">This is useful to segregate files and folders by using this as the first sort key.</span></span> <span data-ttu-id="92467-106">Quand System. ItemDate est utilisé en tant que deuxième clé de tri, il produit des résultats avec des dossiers classés d’abord par nom, puis par fichiers classés par date.</span><span class="sxs-lookup"><span data-stu-id="92467-106">When System.ItemDate is used as a second sort key it produces results with folders first ordered by name, then files ordered by date.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a><span data-ttu-id="92467-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="92467-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1</span></span>

```
propertyDescription
   name = System.FolderNameDisplay
   shellPKey = PKEY_FolderNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 25
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="92467-108">Notes</span><span class="sxs-lookup"><span data-stu-id="92467-108">Remarks</span></span>

<span data-ttu-id="92467-109">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="92467-109">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92467-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="92467-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92467-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="92467-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="92467-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="92467-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="92467-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="92467-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="92467-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="92467-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="92467-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="92467-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="92467-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="92467-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="92467-117">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="92467-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="92467-118">numberFormat</span><span class="sxs-lookup"><span data-stu-id="92467-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="92467-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="92467-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="92467-120">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="92467-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="92467-121">drawControl</span><span class="sxs-lookup"><span data-stu-id="92467-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="92467-122">editControl</span><span class="sxs-lookup"><span data-stu-id="92467-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="92467-123">filterControl</span><span class="sxs-lookup"><span data-stu-id="92467-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="92467-124">queryControl</span><span class="sxs-lookup"><span data-stu-id="92467-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
