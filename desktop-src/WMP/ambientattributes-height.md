---
title: AmbientAttributes. Height
description: L’attribut Height spécifie ou récupère la hauteur du contrôle.
ms.assetid: a5c85d86-15d4-451d-b8bc-ed3b6e0dfd7d
keywords:
- Lecteur Windows Media AmbientAttributes. Height
topic_type:
- apiref
api_name:
- AmbientAttributes.height
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 662268bfeaf00b3185d531ff10d8dd17c9127a66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537613"
---
# <a name="ambientattributesheight"></a><span data-ttu-id="bcbbd-104">AmbientAttributes. Height</span><span class="sxs-lookup"><span data-stu-id="bcbbd-104">AmbientAttributes.height</span></span>

<span data-ttu-id="bcbbd-105">L’attribut **Height** spécifie ou récupère la hauteur du contrôle.</span><span class="sxs-lookup"><span data-stu-id="bcbbd-105">The **height** attribute specifies or retrieves the height of the control.</span></span>

``` syntax
        elementID.height
```

## <a name="possible-values"></a><span data-ttu-id="bcbbd-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="bcbbd-106">Possible Values</span></span>

<span data-ttu-id="bcbbd-107">Cet attribut est un **nombre** en lecture/écriture (**long**) représentant la hauteur du contrôle en pixels.</span><span class="sxs-lookup"><span data-stu-id="bcbbd-107">This attribute is a read/write **Number** (**long**) representing the height of the control in pixels.</span></span> <span data-ttu-id="bcbbd-108">La valeur par défaut est zéro ou la hauteur de l’image spécifiée dans l’attribut **image** du contrôle.</span><span class="sxs-lookup"><span data-stu-id="bcbbd-108">The default value is zero or the height of the image specified in the control's **image** attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcbbd-109">Notes</span><span class="sxs-lookup"><span data-stu-id="bcbbd-109">Remarks</span></span>

<span data-ttu-id="bcbbd-110">Si la hauteur spécifiée est inférieure à la hauteur de l’image fournie, l’image est découpée.</span><span class="sxs-lookup"><span data-stu-id="bcbbd-110">If the height specified is smaller than the height of the image provided, then the image will be clipped.</span></span> <span data-ttu-id="bcbbd-111">Si la hauteur est supérieure à la hauteur de l’image, la zone de clic va au-delà de la limite de l’image.</span><span class="sxs-lookup"><span data-stu-id="bcbbd-111">If the height is larger than the height of the image, then the click region will go beyond the image boundary.</span></span> <span data-ttu-id="bcbbd-112">Quelle que soit la valeur attribuée à cet attribut, l’image ne peut pas croître au-delà de la **vue** ou de la sous- **vue** parente.</span><span class="sxs-lookup"><span data-stu-id="bcbbd-112">No matter what value is given to this attribute, the image cannot grow beyond its parent **VIEW** or **SUBVIEW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcbbd-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bcbbd-113">Requirements</span></span>



| <span data-ttu-id="bcbbd-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bcbbd-114">Requirement</span></span> | <span data-ttu-id="bcbbd-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="bcbbd-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="bcbbd-116">Version</span><span class="sxs-lookup"><span data-stu-id="bcbbd-116">Version</span></span><br/> | <span data-ttu-id="bcbbd-117">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="bcbbd-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bcbbd-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcbbd-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcbbd-119">**Attributs ambiants**</span><span class="sxs-lookup"><span data-stu-id="bcbbd-119">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





