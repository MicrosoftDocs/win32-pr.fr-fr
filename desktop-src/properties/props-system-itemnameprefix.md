---
description: 'Préfixe d’un élément, utilisé pour les messages électroniques où le sujet commence par le préfixe &\# 0034 ; Re : &\# 0034 ;.'
ms.assetid: 3c257edc-b7f7-498d-8347-0be4fca41023
title: System. ItemNamePrefix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf669dd867c8cf60046f226e33dae18f46060cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951378"
---
# <a name="systemitemnameprefix"></a><span data-ttu-id="361bb-103">System. ItemNamePrefix</span><span class="sxs-lookup"><span data-stu-id="361bb-103">System.ItemNamePrefix</span></span>

<span data-ttu-id="361bb-104">Préfixe d’un élément, utilisé pour les messages électroniques où le sujet commence par le préfixe « re : ».</span><span class="sxs-lookup"><span data-stu-id="361bb-104">The prefix of an item, used for e-mail messages where the subject begins with the prefix "Re:".</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="361bb-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="361bb-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemNamePrefix
   shellPKey = PKEY_ItemNamePrefix
   formatID = D7313FF1-A77A-401C-8C99-3DBDD68ADD36
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="361bb-106">Notes</span><span class="sxs-lookup"><span data-stu-id="361bb-106">Remarks</span></span>

<span data-ttu-id="361bb-107">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="361bb-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="361bb-108">Si l’élément est un fichier, la valeur de cette propriété est VT \_ vide.</span><span class="sxs-lookup"><span data-stu-id="361bb-108">If the item is a file, then the value of this property is VT\_EMPTY.</span></span> <span data-ttu-id="361bb-109">Si l’élément est un message, la valeur de cette propriété est le préfixe de transfert ou de réponse (y compris le signe deux-points, mais aucun espace blanc), ou VT \_ vide s’il n’y a aucun préfixe.</span><span class="sxs-lookup"><span data-stu-id="361bb-109">If the item is a message, then the value of this property is the forwarding or reply prefixes (including the delimiting colon, but no whitespace), or VT\_EMPTY if there is no prefix.</span></span>

<span data-ttu-id="361bb-110">Exemples de valeurs</span><span class="sxs-lookup"><span data-stu-id="361bb-110">Example values:</span></span>



| <span data-ttu-id="361bb-111">System. ItemNamePrefix</span><span class="sxs-lookup"><span data-stu-id="361bb-111">System.ItemNamePrefix</span></span> | <span data-ttu-id="361bb-112">System. ItemName</span><span class="sxs-lookup"><span data-stu-id="361bb-112">System.ItemName</span></span>  | <span data-ttu-id="361bb-113">System.ItemNameDisplay</span><span class="sxs-lookup"><span data-stu-id="361bb-113">System.ItemNameDisplay</span></span> |
|-----------------------|------------------|------------------------|
| <span data-ttu-id="361bb-114">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="361bb-114">VT\_EMPTY</span></span>             | <span data-ttu-id="361bb-115">« Bonne journée »</span><span class="sxs-lookup"><span data-stu-id="361bb-115">"Great day"</span></span>      | <span data-ttu-id="361bb-116">« Bonne journée »</span><span class="sxs-lookup"><span data-stu-id="361bb-116">"Great day"</span></span>            |
| <span data-ttu-id="361bb-117">« Re : »</span><span class="sxs-lookup"><span data-stu-id="361bb-117">"Re:"</span></span>                 | <span data-ttu-id="361bb-118">« Bonne journée »</span><span class="sxs-lookup"><span data-stu-id="361bb-118">"Great day"</span></span>      | <span data-ttu-id="361bb-119">« Re : excellent jour »</span><span class="sxs-lookup"><span data-stu-id="361bb-119">"Re: Great day"</span></span>        |
| <span data-ttu-id="361bb-120">« FWD : »</span><span class="sxs-lookup"><span data-stu-id="361bb-120">"Fwd: "</span></span>               | <span data-ttu-id="361bb-121">« Budget mensuel »</span><span class="sxs-lookup"><span data-stu-id="361bb-121">"Monthly budget"</span></span> | <span data-ttu-id="361bb-122">« FWD : budget mensuel »</span><span class="sxs-lookup"><span data-stu-id="361bb-122">"Fwd: Monthly budget"</span></span>  |
| <span data-ttu-id="361bb-123">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="361bb-123">VT\_EMPTY</span></span>             | <span data-ttu-id="361bb-124">accounts.xls</span><span class="sxs-lookup"><span data-stu-id="361bb-124">accounts.xls</span></span>     | <span data-ttu-id="361bb-125">accounts.xls</span><span class="sxs-lookup"><span data-stu-id="361bb-125">accounts.xls</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="361bb-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="361bb-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="361bb-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="361bb-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="361bb-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="361bb-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="361bb-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="361bb-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="361bb-130">typeInfo</span><span class="sxs-lookup"><span data-stu-id="361bb-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="361bb-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="361bb-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="361bb-132">stringFormat</span><span class="sxs-lookup"><span data-stu-id="361bb-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="361bb-133">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="361bb-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="361bb-134">numberFormat</span><span class="sxs-lookup"><span data-stu-id="361bb-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="361bb-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="361bb-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="361bb-136">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="361bb-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="361bb-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="361bb-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="361bb-138">editControl</span><span class="sxs-lookup"><span data-stu-id="361bb-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="361bb-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="361bb-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="361bb-140">queryControl</span><span class="sxs-lookup"><span data-stu-id="361bb-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
