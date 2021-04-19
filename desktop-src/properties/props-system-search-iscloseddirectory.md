---
description: Émis comme TRUE par un élément conteneur pour indiquer que ses éléments enfants n’ont pas besoin d’être énumérés par un indexeur si l’élément conteneur n’a pas été modifié depuis la dernière analyse incrémentielle de vérification de l’index.
ms.assetid: 8bb487b9-4a51-4a6b-939e-946a8aad85de
title: System. Search. IsClosedDirectory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea97aeb8d0192eea7d71ca65fd0ec109780702f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538704"
---
# <a name="systemsearchiscloseddirectory"></a><span data-ttu-id="2b5f2-103">System. Search. IsClosedDirectory</span><span class="sxs-lookup"><span data-stu-id="2b5f2-103">System.Search.IsClosedDirectory</span></span>

<span data-ttu-id="2b5f2-104">Émis comme **true** par un élément conteneur pour indiquer que ses éléments enfants n’ont pas besoin d’être énumérés par un indexeur si l’élément conteneur n’a pas été modifié depuis la dernière analyse incrémentielle de vérification de l’index.</span><span class="sxs-lookup"><span data-stu-id="2b5f2-104">Emitted as **TRUE** by a container item to indicate that its child items do not need to be enumerated by an indexer if the container item has not changed since the last incremental index verification crawl.</span></span> <span data-ttu-id="2b5f2-105">Cela contribue à l’optimisation des performances de l’indexeur.</span><span class="sxs-lookup"><span data-stu-id="2b5f2-105">This contributes to the optimization of indexer performance.</span></span> <span data-ttu-id="2b5f2-106">Dans ces cas de conteneurs (par exemple, un courrier électronique avec des pièces jointes ou un fichier compressé avec une extension de nom. zip), les éléments enfants sont inséparables de leur élément parent.</span><span class="sxs-lookup"><span data-stu-id="2b5f2-106">In these container cases (examples are an e-mail with attachments or a compressed file with a .zip name extension), child items are inseparable from their parent item.</span></span> <span data-ttu-id="2b5f2-107">Par exemple, si la propriété [System. DateModified](./props-system-datemodified.md) d’un élément contenu change, la valeur System. DateModified du conteneur est modifiée pour correspondre à.</span><span class="sxs-lookup"><span data-stu-id="2b5f2-107">For instance, if the [System.DateModified](./props-system-datemodified.md) property of a contained item changes, then the System.DateModified value of the container changes to match.</span></span> <span data-ttu-id="2b5f2-108">En outre, si un élément parent est supprimé, tous les éléments enfants sont également supprimés.</span><span class="sxs-lookup"><span data-stu-id="2b5f2-108">Also, if a parent item is deleted, all of the child items are deleted as well.</span></span> <span data-ttu-id="2b5f2-109">Par conséquent, si le conteneur n’a pas changé, l’indexeur sait que rien dans celui-ci n’a changé et n’a pas besoin d’ouvrir le conteneur pour examiner le contenu individuellement.</span><span class="sxs-lookup"><span data-stu-id="2b5f2-109">Therefore, if the container has not changed, the indexer knows that nothing within it has changed and does not need to open the container to examine the contents individually.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="2b5f2-110">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2b5f2-110">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.IsClosedDirectory
   shellPKey = PKEY_Search_IsClosedDirectory
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 23
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a><span data-ttu-id="2b5f2-111">Notes</span><span class="sxs-lookup"><span data-stu-id="2b5f2-111">Remarks</span></span>

<span data-ttu-id="2b5f2-112">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="2b5f2-112">PKEY values are defined in Propkey.h.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2b5f2-113">Si un élément émet la **valeur true** pour cette propriété, chacun de ses éléments enfants doit émettre la propriété [System. Search. IsFullyContained](./props-system-search-isfullycontained.md) comme **true** pour empêcher la suppression de ces éléments de l’index.</span><span class="sxs-lookup"><span data-stu-id="2b5f2-113">If an item emits **TRUE** for this property, each of its child items must emit the [System.Search.IsFullyContained](./props-system-search-isfullycontained.md) property as **TRUE** to prevent those items from being deleted from the index.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2b5f2-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2b5f2-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b5f2-115">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="2b5f2-115">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="2b5f2-116">searchInfo</span><span class="sxs-lookup"><span data-stu-id="2b5f2-116">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="2b5f2-117">labelInfo</span><span class="sxs-lookup"><span data-stu-id="2b5f2-117">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="2b5f2-118">typeInfo</span><span class="sxs-lookup"><span data-stu-id="2b5f2-118">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="2b5f2-119">displayInfo</span><span class="sxs-lookup"><span data-stu-id="2b5f2-119">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="2b5f2-120">stringFormat</span><span class="sxs-lookup"><span data-stu-id="2b5f2-120">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="2b5f2-121">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="2b5f2-121">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="2b5f2-122">numberFormat</span><span class="sxs-lookup"><span data-stu-id="2b5f2-122">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="2b5f2-123">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="2b5f2-123">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="2b5f2-124">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="2b5f2-124">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="2b5f2-125">drawControl</span><span class="sxs-lookup"><span data-stu-id="2b5f2-125">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="2b5f2-126">editControl</span><span class="sxs-lookup"><span data-stu-id="2b5f2-126">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="2b5f2-127">filterControl</span><span class="sxs-lookup"><span data-stu-id="2b5f2-127">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="2b5f2-128">queryControl</span><span class="sxs-lookup"><span data-stu-id="2b5f2-128">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
