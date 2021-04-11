---
description: Cette chaîne doit être définie sur la version phonétique du nom complet telle que définie dans System. ItemNameDisplay dans les paramètres régionaux CJC (CHS pinyin, JPN hiragana, KOR Hangul, etc.).
ms.assetid: eb491644-bf59-4439-9e9b-bcafde619d66
title: System. ItemNameSortOverride
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d79f9bb07eb15eb5d25fbfa1e95d4c0f80b35611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204050"
---
# <a name="systemitemnamesortoverride"></a><span data-ttu-id="e7158-103">System. ItemNameSortOverride</span><span class="sxs-lookup"><span data-stu-id="e7158-103">System.ItemNameSortOverride</span></span>

<span data-ttu-id="e7158-104">Cette chaîne doit être définie sur la version phonétique du nom complet telle que définie dans System. ItemNameDisplay dans les paramètres régionaux CJC (CHS pinyin, JPN hiragana, KOR Hangul, etc.).</span><span class="sxs-lookup"><span data-stu-id="e7158-104">This string should be set to the phonetic version of the display name as defined in System.ItemNameDisplay in CJK locales(CHS Pinyin, JPN Hiragana, KOR Hangul, etc.).</span></span> <span data-ttu-id="e7158-105">Le premier caractère de ce champ est également utilisé pour regrouper les noms par FirstLetter.</span><span class="sxs-lookup"><span data-stu-id="e7158-105">The first character of this field is also used for grouping names by firstletter.</span></span> <span data-ttu-id="e7158-106">Pour la plupart des langues autres que CJK, ce champ n’a pas besoin d’être défini (auquel cas System. ItemNameDisplay sera utilisé). Toutefois, s’il est souhaitable de remplacer la lettre de regroupement (par exemple, pour supprimer des Articles de début tels que « a » et « The »), une chaîne de remplacement peut être fournie ici.</span><span class="sxs-lookup"><span data-stu-id="e7158-106">For most non-CJK languages, this field does not need to be set (in which case System.ItemNameDisplay will be used).However, if it is desirable to override the grouping letter (for example, to remove leading articles such as "a" and "the"),an alternate string can be provided here.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="e7158-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="e7158-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.ItemNameSortOverride
   shellPKey = PKEY_ItemNameSortOverride
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 23
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="e7158-108">Notes</span><span class="sxs-lookup"><span data-stu-id="e7158-108">Remarks</span></span>

<span data-ttu-id="e7158-109">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="e7158-109">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7158-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e7158-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7158-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="e7158-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="e7158-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="e7158-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="e7158-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="e7158-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="e7158-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="e7158-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="e7158-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="e7158-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="e7158-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="e7158-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="e7158-117">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="e7158-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="e7158-118">numberFormat</span><span class="sxs-lookup"><span data-stu-id="e7158-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="e7158-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="e7158-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="e7158-120">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="e7158-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="e7158-121">drawControl</span><span class="sxs-lookup"><span data-stu-id="e7158-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="e7158-122">editControl</span><span class="sxs-lookup"><span data-stu-id="e7158-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="e7158-123">filterControl</span><span class="sxs-lookup"><span data-stu-id="e7158-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="e7158-124">queryControl</span><span class="sxs-lookup"><span data-stu-id="e7158-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
