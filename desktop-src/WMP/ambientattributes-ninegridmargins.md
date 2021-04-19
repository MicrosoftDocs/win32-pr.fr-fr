---
title: AmbientAttributes.nineGridMargins
description: L’attribut nineGridMargins spécifie des largeurs de marge pour la mise à l’échelle non uniforme de l’élément Skin.
ms.assetid: b8a7efd0-6c12-4436-9d53-0dcfa1600aa5
keywords:
- Lecteur Windows Media AmbientAttributes. nineGridMargins
topic_type:
- apiref
api_name:
- AmbientAttributes.nineGridMargins
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cf77c1fcfdb64fb9e4b0dde8753572255c17eda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530443"
---
# <a name="ambientattributesninegridmargins"></a><span data-ttu-id="5f26f-104">AmbientAttributes.nineGridMargins</span><span class="sxs-lookup"><span data-stu-id="5f26f-104">AmbientAttributes.nineGridMargins</span></span>

<span data-ttu-id="5f26f-105">L’attribut **nineGridMargins** spécifie des largeurs de marge pour la mise à l’échelle non uniforme de l’élément Skin.</span><span class="sxs-lookup"><span data-stu-id="5f26f-105">The **nineGridMargins** attribute specifies margin widths for non-uniform scaling of the skin element.</span></span>

``` syntax
        elementID.nineGridMargins
```

## <a name="possible-values"></a><span data-ttu-id="5f26f-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="5f26f-106">Possible Values</span></span>

<span data-ttu-id="5f26f-107">Cet attribut est une **chaîne** en lecture/écriture qui contient les largeurs des marges sous la forme «*widthLeft*,*widthTop*,*widthRight*,*widthBottom*».</span><span class="sxs-lookup"><span data-stu-id="5f26f-107">This attribute is a read/write **String** that contains the widths of the margins in the form "*widthLeft*,*widthTop*,*widthRight*,*widthBottom*".</span></span> <span data-ttu-id="5f26f-108">Chaque valeur de largeur est un nombre qui représente la largeur, en pixels, d’une marge pour la grille neuf.</span><span class="sxs-lookup"><span data-stu-id="5f26f-108">Each width value is a number representing the width, in pixels, of a margin for the nine grid.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f26f-109">Notes</span><span class="sxs-lookup"><span data-stu-id="5f26f-109">Remarks</span></span>

<span data-ttu-id="5f26f-110">Une *grille de neuf* est une technique utilisée pour diviser les éléments de l’interface utilisateur en neuf régions rectangulaires, organisées en 3 et 3 matrices.</span><span class="sxs-lookup"><span data-stu-id="5f26f-110">A *nine grid* is a technique used to divide user interface elements into nine rectangular regions arranged in a 3 by 3 matrix.</span></span> <span data-ttu-id="5f26f-111">Lorsqu’un élément est redimensionné, les neuf régions de grille peuvent être mises à l’échelle selon un facteur différent.</span><span class="sxs-lookup"><span data-stu-id="5f26f-111">When an element is resized, the nine grid regions can each scale by a different factor.</span></span>

<span data-ttu-id="5f26f-112">Chacune des quatre valeurs de largeur que vous spécifiez représente la largeur d’une ligne ou d’une colonne de trois régions adjacentes.</span><span class="sxs-lookup"><span data-stu-id="5f26f-112">Each of the four width values you specify represents the width of a row or column of three adjacent regions.</span></span> <span data-ttu-id="5f26f-113">Chaque ligne ou colonne forme le côté gauche, le haut, le côté droit ou le bas de la grille neuf.</span><span class="sxs-lookup"><span data-stu-id="5f26f-113">Each row or column forms the left side, top, right side, or bottom of the nine grid.</span></span>

<span data-ttu-id="5f26f-114">[AmbientAttributes. resizeImages](ambientattributes-resizeimages.md) doit avoir la valeur true pour que cet attribut fonctionne.</span><span class="sxs-lookup"><span data-stu-id="5f26f-114">[AmbientAttributes.resizeImages](ambientattributes-resizeimages.md) must be set to true for this attribute to work.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f26f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f26f-115">Requirements</span></span>



| <span data-ttu-id="5f26f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f26f-116">Requirement</span></span> | <span data-ttu-id="5f26f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f26f-117">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="5f26f-118">Version</span><span class="sxs-lookup"><span data-stu-id="5f26f-118">Version</span></span><br/> | <span data-ttu-id="5f26f-119">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="5f26f-119">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5f26f-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f26f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f26f-121">**Attributs ambiants**</span><span class="sxs-lookup"><span data-stu-id="5f26f-121">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





