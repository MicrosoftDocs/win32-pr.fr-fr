---
title: BOUTON. en mosaïque
description: L’attribut tileed spécifie ou récupère une valeur indiquant si l’image du bouton sera affichée en mosaïque.
ms.assetid: 5526477d-a235-4960-adef-5cf0ef9c46be
keywords:
- BUTTON. lecteur Windows Media en mosaïque
topic_type:
- apiref
api_name:
- BUTTON.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c6c1316f10ce9ae3135f4ac35ab214ecdd1096d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541534"
---
# <a name="buttontiled"></a><span data-ttu-id="0b6bf-104">BOUTON. en mosaïque</span><span class="sxs-lookup"><span data-stu-id="0b6bf-104">BUTTON.tiled</span></span>

<span data-ttu-id="0b6bf-105">L’attribut **tileed** spécifie ou récupère une valeur indiquant si l’image du **bouton** sera affichée en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="0b6bf-105">The **tiled** attribute specifies or retrieves a value indicating whether the **BUTTON** image will be tiled.</span></span>

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a><span data-ttu-id="0b6bf-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="0b6bf-106">Possible Values</span></span>

<span data-ttu-id="0b6bf-107">Cet attribut est une **valeur booléenne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="0b6bf-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="0b6bf-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b6bf-108">Value</span></span> | <span data-ttu-id="0b6bf-109">Description</span><span class="sxs-lookup"><span data-stu-id="0b6bf-109">Description</span></span>                       |
|-------|-----------------------------------|
| <span data-ttu-id="0b6bf-110">true</span><span class="sxs-lookup"><span data-stu-id="0b6bf-110">true</span></span>  | <span data-ttu-id="0b6bf-111">L’image sera affichée en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="0b6bf-111">Image will be tiled.</span></span>              |
| <span data-ttu-id="0b6bf-112">false</span><span class="sxs-lookup"><span data-stu-id="0b6bf-112">false</span></span> | <span data-ttu-id="0b6bf-113">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="0b6bf-113">Default.</span></span> <span data-ttu-id="0b6bf-114">L’image ne sera pas affichée en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="0b6bf-114">Image will not be tiled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0b6bf-115">Notes</span><span class="sxs-lookup"><span data-stu-id="0b6bf-115">Remarks</span></span>

<span data-ttu-id="0b6bf-116">Si l’image est plus petite que la région réelle du contrôle, la mosaïque de l’image se répète jusqu’à ce qu’elle remplisse toute la région.</span><span class="sxs-lookup"><span data-stu-id="0b6bf-116">If the image is smaller than the actual region of the control, then tiling the image will repeat it until it fills the entire region.</span></span> <span data-ttu-id="0b6bf-117">Si une image n’est pas spécifiée ou ne peut pas être récupérée, la **mosaïque** est définie sur false.</span><span class="sxs-lookup"><span data-stu-id="0b6bf-117">If an image is not specified or cannot be retrieved, **tiled** will be set to false.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b6bf-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b6bf-118">Requirements</span></span>



| <span data-ttu-id="0b6bf-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b6bf-119">Requirement</span></span> | <span data-ttu-id="0b6bf-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b6bf-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="0b6bf-121">Version</span><span class="sxs-lookup"><span data-stu-id="0b6bf-121">Version</span></span><br/> | <span data-ttu-id="0b6bf-122">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="0b6bf-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0b6bf-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b6bf-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b6bf-124">**BUTTON, élément**</span><span class="sxs-lookup"><span data-stu-id="0b6bf-124">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="0b6bf-125">**BOUTON. image**</span><span class="sxs-lookup"><span data-stu-id="0b6bf-125">**BUTTON.image**</span></span>](button-image.md)
</dt> </dl>

 

 





