---
title: BOUTON. curseur
description: L’attribut Cursor spécifie ou récupère le curseur qui apparaît lorsque le pointeur de la souris est positionné sur le bouton.
ms.assetid: 19bdbb23-00e2-45cf-b67d-9ada036b9c3b
keywords:
- BUTTON. curseur lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTON.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2641491a5a73498da2c43fd74d4187b5594e177
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526050"
---
# <a name="buttoncursor"></a><span data-ttu-id="70266-104">BOUTON. curseur</span><span class="sxs-lookup"><span data-stu-id="70266-104">BUTTON.cursor</span></span>

<span data-ttu-id="70266-105">L’attribut **Cursor** spécifie ou récupère le curseur qui apparaît lorsque le pointeur de la souris est positionné sur le **bouton**.</span><span class="sxs-lookup"><span data-stu-id="70266-105">The **cursor** attribute specifies or retrieves the cursor that appears when the mouse pointer hovers over the **BUTTON**.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="70266-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="70266-106">Possible Values</span></span>

<span data-ttu-id="70266-107">Cet attribut est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="70266-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="70266-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="70266-108">Value</span></span>            | <span data-ttu-id="70266-109">Description</span><span class="sxs-lookup"><span data-stu-id="70266-109">Description</span></span>                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="70266-110">système</span><span class="sxs-lookup"><span data-stu-id="70266-110">system</span></span>           | <span data-ttu-id="70266-111">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="70266-111">Default.</span></span> <span data-ttu-id="70266-112">Curseur dépendant de la plateforme (généralement une flèche).</span><span class="sxs-lookup"><span data-stu-id="70266-112">Platform-dependent cursor (usually an arrow).</span></span>                                     |
| <span data-ttu-id="70266-113">Toutefois</span><span class="sxs-lookup"><span data-stu-id="70266-113">hand</span></span>             | <span data-ttu-id="70266-114">Toutefois.</span><span class="sxs-lookup"><span data-stu-id="70266-114">Hand.</span></span>                                                                                      |
| <span data-ttu-id="70266-115">help</span><span class="sxs-lookup"><span data-stu-id="70266-115">help</span></span>             | <span data-ttu-id="70266-116">Flèche avec un point d’interrogation indiquant que l’aide est disponible.</span><span class="sxs-lookup"><span data-stu-id="70266-116">Arrow with question mark indicating Help is available.</span></span>                                     |
| <span data-ttu-id="70266-117">sizeall</span><span class="sxs-lookup"><span data-stu-id="70266-117">sizeall</span></span>          | <span data-ttu-id="70266-118">Flèche à quatre pointes pointant vers le Nord, le sud, l’est et l’Ouest.</span><span class="sxs-lookup"><span data-stu-id="70266-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                  |
| <span data-ttu-id="70266-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="70266-119">sizenesw</span></span>         | <span data-ttu-id="70266-120">Flèche à deux pointes pointant vers le nord-est et le sud-ouest.</span><span class="sxs-lookup"><span data-stu-id="70266-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                     |
| <span data-ttu-id="70266-121">sizens</span><span class="sxs-lookup"><span data-stu-id="70266-121">sizens</span></span>           | <span data-ttu-id="70266-122">Flèche à deux pointes pointant vers le Nord et le sud.</span><span class="sxs-lookup"><span data-stu-id="70266-122">Double-pointed arrow pointing north and south.</span></span>                                             |
| <span data-ttu-id="70266-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="70266-123">sizenwse</span></span>         | <span data-ttu-id="70266-124">Flèche à deux pointes pointant vers le Nord-Ouest et le sud-est.</span><span class="sxs-lookup"><span data-stu-id="70266-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                     |
| <span data-ttu-id="70266-125">sizewe</span><span class="sxs-lookup"><span data-stu-id="70266-125">sizewe</span></span>           | <span data-ttu-id="70266-126">Flèche à deux pointes pointant vers l’Ouest et l’est.</span><span class="sxs-lookup"><span data-stu-id="70266-126">Double-pointed arrow pointing west and east.</span></span>                                               |
| <span data-ttu-id="70266-127">haut</span><span class="sxs-lookup"><span data-stu-id="70266-127">uparrow</span></span>          | <span data-ttu-id="70266-128">Flèche verticale pointant vers le haut.</span><span class="sxs-lookup"><span data-stu-id="70266-128">Vertical arrow pointing upward.</span></span>                                                            |
| <span data-ttu-id="70266-129">\*. ani ou \* . cur</span><span class="sxs-lookup"><span data-stu-id="70266-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="70266-130">Tout fichier. ani ou. cur (doit se trouver dans le même répertoire que le fichier. WMS ou dans le fichier. WMZ)</span><span class="sxs-lookup"><span data-stu-id="70266-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="70266-131">Notes</span><span class="sxs-lookup"><span data-stu-id="70266-131">Remarks</span></span>

<span data-ttu-id="70266-132">Si le système ne reconnaît pas la valeur de curseur spécifiée, la valeur de curseur reste à la valeur précédemment définie.</span><span class="sxs-lookup"><span data-stu-id="70266-132">If the system does not recognize the cursor value specified, the cursor value remains at the previously set value.</span></span>

<span data-ttu-id="70266-133">Les chemins d’accès aux noms de fichiers de curseur sont ignorés, donc le fichier curseur doit se trouver dans le répertoire par défaut.</span><span class="sxs-lookup"><span data-stu-id="70266-133">Cursor file name paths are ignored, so the cursor file must reside in the default directory.</span></span>

## <a name="requirements"></a><span data-ttu-id="70266-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70266-134">Requirements</span></span>



| <span data-ttu-id="70266-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70266-135">Requirement</span></span> | <span data-ttu-id="70266-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="70266-136">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="70266-137">Version</span><span class="sxs-lookup"><span data-stu-id="70266-137">Version</span></span><br/> | <span data-ttu-id="70266-138">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="70266-138">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="70266-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70266-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70266-140">**BUTTON, élément**</span><span class="sxs-lookup"><span data-stu-id="70266-140">**BUTTON Element**</span></span>](button-element.md)
</dt> </dl>

 

 





