---
title: BUTTONELEMENT. Cursor
description: L’attribut Cursor spécifie ou récupère la valeur du curseur BUTTONELEMENT qui apparaît lorsque la souris se trouve sur le BUTTONELEMENT.
ms.assetid: 29e7fadb-30d8-40e4-9a64-6b6f45eac80a
keywords:
- BUTTONELEMENT. Cursor lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTONELEMENT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f267cd54c36ad8f89a7242d7f428fd0d52b75fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541780"
---
# <a name="buttonelementcursor"></a><span data-ttu-id="5589a-104">BUTTONELEMENT. Cursor</span><span class="sxs-lookup"><span data-stu-id="5589a-104">BUTTONELEMENT.cursor</span></span>

<span data-ttu-id="5589a-105">L’attribut **Cursor** spécifie ou récupère la valeur du curseur **BUTTONELEMENT** qui apparaît lorsque la souris se trouve sur le **BUTTONELEMENT**.</span><span class="sxs-lookup"><span data-stu-id="5589a-105">The **cursor** attribute specifies or retrieves the value of the **BUTTONELEMENT** cursor that appears when the mouse is over the **BUTTONELEMENT**.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="5589a-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="5589a-106">Possible Values</span></span>

<span data-ttu-id="5589a-107">Cet attribut est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="5589a-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="5589a-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="5589a-108">Value</span></span>            | <span data-ttu-id="5589a-109">Description</span><span class="sxs-lookup"><span data-stu-id="5589a-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5589a-110">système</span><span class="sxs-lookup"><span data-stu-id="5589a-110">system</span></span>           | <span data-ttu-id="5589a-111">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="5589a-111">Default.</span></span> <span data-ttu-id="5589a-112">Curseur dépendant de la plateforme (généralement une flèche).</span><span class="sxs-lookup"><span data-stu-id="5589a-112">Platform-dependent cursor (usually an arrow).</span></span>                                      |
| <span data-ttu-id="5589a-113">Toutefois</span><span class="sxs-lookup"><span data-stu-id="5589a-113">hand</span></span>             | <span data-ttu-id="5589a-114">Toutefois.</span><span class="sxs-lookup"><span data-stu-id="5589a-114">Hand.</span></span>                                                                                       |
| <span data-ttu-id="5589a-115">help</span><span class="sxs-lookup"><span data-stu-id="5589a-115">help</span></span>             | <span data-ttu-id="5589a-116">Flèche avec un point d’interrogation indiquant que l’aide est disponible.</span><span class="sxs-lookup"><span data-stu-id="5589a-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="5589a-117">sizeall</span><span class="sxs-lookup"><span data-stu-id="5589a-117">sizeall</span></span>          | <span data-ttu-id="5589a-118">Flèche à quatre pointes pointant vers le Nord, le sud, l’est et l’Ouest.</span><span class="sxs-lookup"><span data-stu-id="5589a-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="5589a-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="5589a-119">sizenesw</span></span>         | <span data-ttu-id="5589a-120">Flèche à deux pointes pointant vers le nord-est et le sud-ouest.</span><span class="sxs-lookup"><span data-stu-id="5589a-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="5589a-121">sizens</span><span class="sxs-lookup"><span data-stu-id="5589a-121">sizens</span></span>           | <span data-ttu-id="5589a-122">Flèche à deux pointes pointant vers le Nord et le sud.</span><span class="sxs-lookup"><span data-stu-id="5589a-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="5589a-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="5589a-123">sizenwse</span></span>         | <span data-ttu-id="5589a-124">Flèche à deux pointes pointant vers le Nord-Ouest et le sud-est.</span><span class="sxs-lookup"><span data-stu-id="5589a-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="5589a-125">sizewe</span><span class="sxs-lookup"><span data-stu-id="5589a-125">sizewe</span></span>           | <span data-ttu-id="5589a-126">Flèche à deux pointes pointant vers l’Ouest et l’est.</span><span class="sxs-lookup"><span data-stu-id="5589a-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="5589a-127">haut</span><span class="sxs-lookup"><span data-stu-id="5589a-127">uparrow</span></span>          | <span data-ttu-id="5589a-128">Flèche verticale pointant vers le haut.</span><span class="sxs-lookup"><span data-stu-id="5589a-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="5589a-129">\*. ani ou \* . cur</span><span class="sxs-lookup"><span data-stu-id="5589a-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="5589a-130">Tout fichier. ani ou. cur (doit se trouver dans le même répertoire que le fichier. WMS ou dans le fichier. WMZ).</span><span class="sxs-lookup"><span data-stu-id="5589a-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5589a-131">Notes</span><span class="sxs-lookup"><span data-stu-id="5589a-131">Remarks</span></span>

<span data-ttu-id="5589a-132">Si une valeur non valide est spécifiée, la valeur précédente est conservée.</span><span class="sxs-lookup"><span data-stu-id="5589a-132">If an invalid value is specified, the previous value is maintained.</span></span>

<span data-ttu-id="5589a-133">Les chemins d’accès aux noms de fichiers de curseur sont ignorés, donc le fichier curseur doit se trouver dans le répertoire par défaut.</span><span class="sxs-lookup"><span data-stu-id="5589a-133">Cursor file name paths are ignored, so the cursor file must reside in the default directory.</span></span>

## <a name="requirements"></a><span data-ttu-id="5589a-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5589a-134">Requirements</span></span>



| <span data-ttu-id="5589a-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5589a-135">Requirement</span></span> | <span data-ttu-id="5589a-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="5589a-136">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="5589a-137">Version</span><span class="sxs-lookup"><span data-stu-id="5589a-137">Version</span></span><br/> | <span data-ttu-id="5589a-138">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="5589a-138">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5589a-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5589a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5589a-140">**Élément BUTTONELEMENT**</span><span class="sxs-lookup"><span data-stu-id="5589a-140">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> </dl>

 

 





