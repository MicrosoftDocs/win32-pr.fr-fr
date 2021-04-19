---
title: CUSTOMSLIDER. Cursor
description: L’attribut Cursor spécifie ou récupère la valeur du curseur de contrôle Slider qui apparaît lorsque la souris se trouve sur le curseur.
ms.assetid: 965c21ab-18a0-4459-9d5b-0a35ea2c212f
keywords:
- Lecteur Windows Media CUSTOMSLIDER. Cursor
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e836dc7ec6efececf81789efe43d8b19d0df1783
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538154"
---
# <a name="customslidercursor"></a><span data-ttu-id="a9bcb-104">CUSTOMSLIDER. Cursor</span><span class="sxs-lookup"><span data-stu-id="a9bcb-104">CUSTOMSLIDER.cursor</span></span>

<span data-ttu-id="a9bcb-105">L’attribut **Cursor** spécifie ou récupère la valeur du curseur de contrôle Slider qui apparaît lorsque la souris se trouve sur le curseur.</span><span class="sxs-lookup"><span data-stu-id="a9bcb-105">The **cursor** attribute specifies or retrieves the value of the slider control cursor that appears when the mouse is over the slider.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="a9bcb-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="a9bcb-106">Possible Values</span></span>

<span data-ttu-id="a9bcb-107">Cet attribut est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a9bcb-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="a9bcb-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9bcb-108">Value</span></span>            | <span data-ttu-id="a9bcb-109">Description</span><span class="sxs-lookup"><span data-stu-id="a9bcb-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9bcb-110">système</span><span class="sxs-lookup"><span data-stu-id="a9bcb-110">system</span></span>           | <span data-ttu-id="a9bcb-111">Curseur dépendant de la plateforme (généralement une flèche).</span><span class="sxs-lookup"><span data-stu-id="a9bcb-111">Platform-dependent cursor (usually an arrow).</span></span>                                               |
| <span data-ttu-id="a9bcb-112">Toutefois</span><span class="sxs-lookup"><span data-stu-id="a9bcb-112">hand</span></span>             | <span data-ttu-id="a9bcb-113">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="a9bcb-113">Default.</span></span> <span data-ttu-id="a9bcb-114">Le curseur est une main.</span><span class="sxs-lookup"><span data-stu-id="a9bcb-114">Cursor is a hand.</span></span>                                                                  |
| <span data-ttu-id="a9bcb-115">help</span><span class="sxs-lookup"><span data-stu-id="a9bcb-115">help</span></span>             | <span data-ttu-id="a9bcb-116">Flèche avec un point d’interrogation indiquant que l’aide est disponible.</span><span class="sxs-lookup"><span data-stu-id="a9bcb-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="a9bcb-117">sizeall</span><span class="sxs-lookup"><span data-stu-id="a9bcb-117">sizeall</span></span>          | <span data-ttu-id="a9bcb-118">Flèche à quatre pointes pointant vers le Nord, le sud, l’est et l’Ouest.</span><span class="sxs-lookup"><span data-stu-id="a9bcb-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="a9bcb-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="a9bcb-119">sizenesw</span></span>         | <span data-ttu-id="a9bcb-120">Flèche à deux pointes pointant vers le nord-est et le sud-ouest.</span><span class="sxs-lookup"><span data-stu-id="a9bcb-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="a9bcb-121">sizens</span><span class="sxs-lookup"><span data-stu-id="a9bcb-121">sizens</span></span>           | <span data-ttu-id="a9bcb-122">Flèche à deux pointes pointant vers le Nord et le sud.</span><span class="sxs-lookup"><span data-stu-id="a9bcb-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="a9bcb-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="a9bcb-123">sizenwse</span></span>         | <span data-ttu-id="a9bcb-124">Flèche à deux pointes pointant vers le Nord-Ouest et le sud-est.</span><span class="sxs-lookup"><span data-stu-id="a9bcb-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="a9bcb-125">sizewe</span><span class="sxs-lookup"><span data-stu-id="a9bcb-125">sizewe</span></span>           | <span data-ttu-id="a9bcb-126">Flèche à deux pointes pointant vers l’Ouest et l’est.</span><span class="sxs-lookup"><span data-stu-id="a9bcb-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="a9bcb-127">haut</span><span class="sxs-lookup"><span data-stu-id="a9bcb-127">uparrow</span></span>          | <span data-ttu-id="a9bcb-128">Flèche verticale pointant vers le haut.</span><span class="sxs-lookup"><span data-stu-id="a9bcb-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="a9bcb-129">\*. ani ou \* . cur</span><span class="sxs-lookup"><span data-stu-id="a9bcb-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="a9bcb-130">Tout fichier. ani ou. cur (doit se trouver dans le même répertoire que le fichier. WMS ou dans le fichier. WMZ).</span><span class="sxs-lookup"><span data-stu-id="a9bcb-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="a9bcb-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9bcb-131">Requirements</span></span>



| <span data-ttu-id="a9bcb-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9bcb-132">Requirement</span></span> | <span data-ttu-id="a9bcb-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9bcb-133">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="a9bcb-134">Version</span><span class="sxs-lookup"><span data-stu-id="a9bcb-134">Version</span></span><br/> | <span data-ttu-id="a9bcb-135">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="a9bcb-135">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a9bcb-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9bcb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9bcb-137">**Élément CUSTOMSLIDER**</span><span class="sxs-lookup"><span data-stu-id="a9bcb-137">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> </dl>

 

 





