---
title: TEXT. Cursor
description: L’attribut Cursor spécifie ou récupère une valeur indiquant le curseur qui apparaît lorsque la souris se trouve sur le contrôle Text.
ms.assetid: 360d4ed1-9c4f-4210-8e77-2dfbe7573869
keywords:
- TEXT. Cursor lecteur Windows Media
topic_type:
- apiref
api_name:
- TEXT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8cf7b135ed0a99b5c65f760a08e4e7083234674
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528640"
---
# <a name="textcursor"></a><span data-ttu-id="c4398-104">TEXT. Cursor</span><span class="sxs-lookup"><span data-stu-id="c4398-104">TEXT.cursor</span></span>

<span data-ttu-id="c4398-105">L’attribut **Cursor** spécifie ou récupère une valeur indiquant le curseur qui apparaît lorsque la souris se trouve sur le contrôle Text.</span><span class="sxs-lookup"><span data-stu-id="c4398-105">The **cursor** attribute specifies or retrieves a value indicating which cursor appears when the mouse is over the Text control.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="c4398-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="c4398-106">Possible Values</span></span>

<span data-ttu-id="c4398-107">Cet attribut est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c4398-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="c4398-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4398-108">Value</span></span>            | <span data-ttu-id="c4398-109">Description</span><span class="sxs-lookup"><span data-stu-id="c4398-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4398-110">système</span><span class="sxs-lookup"><span data-stu-id="c4398-110">system</span></span>           | <span data-ttu-id="c4398-111">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="c4398-111">Default.</span></span> <span data-ttu-id="c4398-112">Curseur dépendant de la plateforme (généralement une flèche).</span><span class="sxs-lookup"><span data-stu-id="c4398-112">Platform-dependent cursor (usually an arrow).</span></span>                                      |
| <span data-ttu-id="c4398-113">Toutefois</span><span class="sxs-lookup"><span data-stu-id="c4398-113">hand</span></span>             | <span data-ttu-id="c4398-114">Toutefois.</span><span class="sxs-lookup"><span data-stu-id="c4398-114">Hand.</span></span>                                                                                       |
| <span data-ttu-id="c4398-115">help</span><span class="sxs-lookup"><span data-stu-id="c4398-115">help</span></span>             | <span data-ttu-id="c4398-116">Flèche avec un point d’interrogation indiquant que l’aide est disponible.</span><span class="sxs-lookup"><span data-stu-id="c4398-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="c4398-117">sizeall</span><span class="sxs-lookup"><span data-stu-id="c4398-117">sizeall</span></span>          | <span data-ttu-id="c4398-118">Flèche à quatre pointes pointant vers le Nord, le sud, l’est et l’Ouest.</span><span class="sxs-lookup"><span data-stu-id="c4398-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="c4398-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="c4398-119">sizenesw</span></span>         | <span data-ttu-id="c4398-120">Flèche à deux pointes pointant vers le nord-est et le sud-ouest.</span><span class="sxs-lookup"><span data-stu-id="c4398-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="c4398-121">sizens</span><span class="sxs-lookup"><span data-stu-id="c4398-121">sizens</span></span>           | <span data-ttu-id="c4398-122">Flèche à deux pointes pointant vers le Nord et le sud.</span><span class="sxs-lookup"><span data-stu-id="c4398-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="c4398-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="c4398-123">sizenwse</span></span>         | <span data-ttu-id="c4398-124">Flèche à deux pointes pointant vers le Nord-Ouest et le sud-est.</span><span class="sxs-lookup"><span data-stu-id="c4398-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="c4398-125">sizewe</span><span class="sxs-lookup"><span data-stu-id="c4398-125">sizewe</span></span>           | <span data-ttu-id="c4398-126">Flèche à deux pointes pointant vers l’Ouest et l’est.</span><span class="sxs-lookup"><span data-stu-id="c4398-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="c4398-127">haut</span><span class="sxs-lookup"><span data-stu-id="c4398-127">uparrow</span></span>          | <span data-ttu-id="c4398-128">Flèche verticale pointant vers le haut.</span><span class="sxs-lookup"><span data-stu-id="c4398-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="c4398-129">\*. ani ou \* . cur</span><span class="sxs-lookup"><span data-stu-id="c4398-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="c4398-130">Tout fichier. ani ou. cur (doit se trouver dans le même répertoire que le fichier. WMS ou dans le fichier. WMZ).</span><span class="sxs-lookup"><span data-stu-id="c4398-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

<span data-ttu-id="c4398-131">Pour obtenir un exemple illustrant l’utilisation des attributs de l’élément de **texte** , consultez l’attribut [value](text-value.md) .</span><span class="sxs-lookup"><span data-stu-id="c4398-131">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4398-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4398-132">Requirements</span></span>



| <span data-ttu-id="c4398-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4398-133">Requirement</span></span> | <span data-ttu-id="c4398-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4398-134">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c4398-135">Version</span><span class="sxs-lookup"><span data-stu-id="c4398-135">Version</span></span><br/> | <span data-ttu-id="c4398-136">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="c4398-136">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c4398-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4398-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4398-138">**Élément de texte**</span><span class="sxs-lookup"><span data-stu-id="c4398-138">**TEXT Element**</span></span>](text-element.md)
</dt> </dl>

 

 





