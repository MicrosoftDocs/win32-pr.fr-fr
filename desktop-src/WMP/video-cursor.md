---
title: VIDEO. Cursor
description: L’attribut Cursor spécifie ou récupère la valeur de curseur utilisée lorsque la souris se trouve sur une zone cliquable de la vidéo.
ms.assetid: 2faaf9cd-47be-47d5-ad4e-8f3bb322d812
keywords:
- VIDEO. Cursor lecteur Windows Media
topic_type:
- apiref
api_name:
- VIDEO.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c23ab90b974ad5a7f9cfaf9fcc598371cd0697f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535300"
---
# <a name="videocursor"></a><span data-ttu-id="4ee5d-104">VIDEO. Cursor</span><span class="sxs-lookup"><span data-stu-id="4ee5d-104">VIDEO.cursor</span></span>

<span data-ttu-id="4ee5d-105">L’attribut **Cursor** spécifie ou récupère la valeur de curseur utilisée lorsque la souris se trouve sur une zone cliquable de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="4ee5d-105">The **cursor** attribute specifies or retrieves the cursor value that is used when the mouse is over a clickable area of the video.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="4ee5d-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="4ee5d-106">Possible Values</span></span>

<span data-ttu-id="4ee5d-107">Cet attribut est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="4ee5d-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="4ee5d-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ee5d-108">Value</span></span>            | <span data-ttu-id="4ee5d-109">Description</span><span class="sxs-lookup"><span data-stu-id="4ee5d-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ee5d-110">système</span><span class="sxs-lookup"><span data-stu-id="4ee5d-110">system</span></span>           | <span data-ttu-id="4ee5d-111">Curseur dépendant de la plateforme (généralement une flèche).</span><span class="sxs-lookup"><span data-stu-id="4ee5d-111">Platform-dependent cursor (usually an arrow).</span></span>                                               |
| <span data-ttu-id="4ee5d-112">Toutefois</span><span class="sxs-lookup"><span data-stu-id="4ee5d-112">hand</span></span>             | <span data-ttu-id="4ee5d-113">Toutefois.</span><span class="sxs-lookup"><span data-stu-id="4ee5d-113">Hand.</span></span>                                                                                       |
| <span data-ttu-id="4ee5d-114">help</span><span class="sxs-lookup"><span data-stu-id="4ee5d-114">help</span></span>             | <span data-ttu-id="4ee5d-115">Flèche avec un point d’interrogation indiquant que l’aide est disponible.</span><span class="sxs-lookup"><span data-stu-id="4ee5d-115">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="4ee5d-116">sizeall</span><span class="sxs-lookup"><span data-stu-id="4ee5d-116">sizeall</span></span>          | <span data-ttu-id="4ee5d-117">Flèche à quatre pointes pointant vers le Nord, le sud, l’est et l’Ouest.</span><span class="sxs-lookup"><span data-stu-id="4ee5d-117">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="4ee5d-118">sizenesw</span><span class="sxs-lookup"><span data-stu-id="4ee5d-118">sizenesw</span></span>         | <span data-ttu-id="4ee5d-119">Flèche à deux pointes pointant vers le nord-est et le sud-ouest.</span><span class="sxs-lookup"><span data-stu-id="4ee5d-119">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="4ee5d-120">sizens</span><span class="sxs-lookup"><span data-stu-id="4ee5d-120">sizens</span></span>           | <span data-ttu-id="4ee5d-121">Flèche à deux pointes pointant vers le Nord et le sud.</span><span class="sxs-lookup"><span data-stu-id="4ee5d-121">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="4ee5d-122">sizenwse</span><span class="sxs-lookup"><span data-stu-id="4ee5d-122">sizenwse</span></span>         | <span data-ttu-id="4ee5d-123">Flèche à deux pointes pointant vers le Nord-Ouest et le sud-est.</span><span class="sxs-lookup"><span data-stu-id="4ee5d-123">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="4ee5d-124">sizewe</span><span class="sxs-lookup"><span data-stu-id="4ee5d-124">sizewe</span></span>           | <span data-ttu-id="4ee5d-125">Flèche à deux pointes pointant vers l’Ouest et l’est.</span><span class="sxs-lookup"><span data-stu-id="4ee5d-125">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="4ee5d-126">haut</span><span class="sxs-lookup"><span data-stu-id="4ee5d-126">uparrow</span></span>          | <span data-ttu-id="4ee5d-127">Flèche verticale pointant vers le haut.</span><span class="sxs-lookup"><span data-stu-id="4ee5d-127">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="4ee5d-128">\*. ani ou \* . cur</span><span class="sxs-lookup"><span data-stu-id="4ee5d-128">\*.ani or \*.cur</span></span> | <span data-ttu-id="4ee5d-129">Tout fichier. ani ou. cur (doit se trouver dans le même répertoire que le fichier. WMS ou dans le fichier. WMZ).</span><span class="sxs-lookup"><span data-stu-id="4ee5d-129">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4ee5d-130">Notes</span><span class="sxs-lookup"><span data-stu-id="4ee5d-130">Remarks</span></span>

<span data-ttu-id="4ee5d-131">À des fins de rendu, System est le curseur par défaut.</span><span class="sxs-lookup"><span data-stu-id="4ee5d-131">For rendering purposes, system is the default cursor.</span></span> <span data-ttu-id="4ee5d-132">La valeur par défaut Récupérée à partir de cet attribut est "" (chaîne vide).</span><span class="sxs-lookup"><span data-stu-id="4ee5d-132">The default value retrieved from this attribute is "" (empty string).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ee5d-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ee5d-133">Requirements</span></span>



| <span data-ttu-id="4ee5d-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4ee5d-134">Requirement</span></span> | <span data-ttu-id="4ee5d-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ee5d-135">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="4ee5d-136">Version</span><span class="sxs-lookup"><span data-stu-id="4ee5d-136">Version</span></span><br/> | <span data-ttu-id="4ee5d-137">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="4ee5d-137">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4ee5d-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ee5d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ee5d-139">**Élément VIDEO**</span><span class="sxs-lookup"><span data-stu-id="4ee5d-139">**VIDEO Element**</span></span>](video-element.md)
</dt> </dl>

 

 





