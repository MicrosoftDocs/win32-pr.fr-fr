---
title: AmbientAttributes. Width
description: L’attribut width spécifie ou récupère la largeur du contrôle.
ms.assetid: f246958a-563c-40c0-8a74-4511103b95b2
keywords:
- Lecteur Windows Media AmbientAttributes. Width
topic_type:
- apiref
api_name:
- AmbientAttributes.width
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c3f91ee47277dc511d54747197edfa44e80e251
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539180"
---
# <a name="ambientattributeswidth"></a><span data-ttu-id="7def7-104">AmbientAttributes. Width</span><span class="sxs-lookup"><span data-stu-id="7def7-104">AmbientAttributes.width</span></span>

<span data-ttu-id="7def7-105">L’attribut **Width** spécifie ou récupère la largeur du contrôle.</span><span class="sxs-lookup"><span data-stu-id="7def7-105">The **width** attribute specifies or retrieves the width of the control.</span></span>

``` syntax
        elementID.width
```

## <a name="possible-values"></a><span data-ttu-id="7def7-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="7def7-106">Possible Values</span></span>

<span data-ttu-id="7def7-107">Cet attribut est un **entier** 16 bits en lecture/écriture (0 à 32 767) représentant la largeur du contrôle en pixels.</span><span class="sxs-lookup"><span data-stu-id="7def7-107">This attribute is a read/write 16-bit **Integer** (0 to 32,767) representing the width of the control in pixels.</span></span> <span data-ttu-id="7def7-108">La valeur par défaut est zéro ou la largeur de l’image spécifiée dans l’attribut **image** du contrôle.</span><span class="sxs-lookup"><span data-stu-id="7def7-108">The default value is zero or the width of the image specified in the control's **image** attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="7def7-109">Notes</span><span class="sxs-lookup"><span data-stu-id="7def7-109">Remarks</span></span>

<span data-ttu-id="7def7-110">Si la largeur spécifiée est plus étroite que la largeur de l’image fournie, l’image est découpée.</span><span class="sxs-lookup"><span data-stu-id="7def7-110">If the width specified is narrower than the width of the image provided, then the image will be clipped.</span></span> <span data-ttu-id="7def7-111">Si la largeur est plus large que la largeur de l’image, la zone de clic va au-delà de la limite de l’image.</span><span class="sxs-lookup"><span data-stu-id="7def7-111">If the width is wider than the width of the image, then the click region will go beyond the image boundary.</span></span> <span data-ttu-id="7def7-112">Quelle que soit la valeur attribuée à cet attribut, l’image ne peut pas croître au-delà de la **vue** ou de la sous- **vue** parente.</span><span class="sxs-lookup"><span data-stu-id="7def7-112">No matter what value is given to this attribute, the image cannot grow beyond its parent **VIEW** or **SUBVIEW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7def7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7def7-113">Requirements</span></span>



| <span data-ttu-id="7def7-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7def7-114">Requirement</span></span> | <span data-ttu-id="7def7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="7def7-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="7def7-116">Version</span><span class="sxs-lookup"><span data-stu-id="7def7-116">Version</span></span><br/> | <span data-ttu-id="7def7-117">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="7def7-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7def7-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7def7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7def7-119">**Attributs ambiants**</span><span class="sxs-lookup"><span data-stu-id="7def7-119">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





