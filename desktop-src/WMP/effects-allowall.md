---
title: EFFECTs. AutoriserTout
description: L’attribut AutoriserTout spécifie ou récupère une valeur indiquant s’il faut inclure toutes les visualisations qui se trouvent dans le registre.
ms.assetid: 8552cc06-05b2-4049-ba7d-f6bd770449e0
keywords:
- EFFECTs. AutoriserTout Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.allowAll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56760021fe34522072677e9524fe6636e519e20f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542492"
---
# <a name="effectsallowall"></a><span data-ttu-id="2ebe1-104">EFFECTs. AutoriserTout</span><span class="sxs-lookup"><span data-stu-id="2ebe1-104">EFFECTS.allowAll</span></span>

<span data-ttu-id="2ebe1-105">L’attribut **AutoriserTout** spécifie ou récupère une valeur indiquant s’il faut inclure toutes les visualisations qui se trouvent dans le registre.</span><span class="sxs-lookup"><span data-stu-id="2ebe1-105">The **allowAll** attribute specifies or retrieves a value indicating whether to include all the visualizations that are in the registry.</span></span>

``` syntax
        elementID.allowAll
```

## <a name="possible-values"></a><span data-ttu-id="2ebe1-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="2ebe1-106">Possible Values</span></span>

<span data-ttu-id="2ebe1-107">Cet attribut est une **valeur booléenne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="2ebe1-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="2ebe1-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ebe1-108">Value</span></span> | <span data-ttu-id="2ebe1-109">Description</span><span class="sxs-lookup"><span data-stu-id="2ebe1-109">Description</span></span>                                                         |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="2ebe1-110">true</span><span class="sxs-lookup"><span data-stu-id="2ebe1-110">true</span></span>  | <span data-ttu-id="2ebe1-111">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="2ebe1-111">Default.</span></span> <span data-ttu-id="2ebe1-112">Autorise le cycle de toutes les visualisations sur le système de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2ebe1-112">Allows cycling of all visualizations on the user's system.</span></span> |
| <span data-ttu-id="2ebe1-113">false</span><span class="sxs-lookup"><span data-stu-id="2ebe1-113">false</span></span> | <span data-ttu-id="2ebe1-114">Limite le cycle aux visualisations apparaissant dans les balises d' **effets** .</span><span class="sxs-lookup"><span data-stu-id="2ebe1-114">Limits cycling to visualizations appearing within **EFFECTS** tags.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2ebe1-115">Notes</span><span class="sxs-lookup"><span data-stu-id="2ebe1-115">Remarks</span></span>

<span data-ttu-id="2ebe1-116">Si cet attribut est défini sur false, seules les visualisations apparaissant dans les balises d' **effets** peuvent être recycles à l’aide du précédent/suivant.</span><span class="sxs-lookup"><span data-stu-id="2ebe1-116">If this attribute is set to false, only the visualizations appearing within **EFFECTS** tags can be cycled through using previous/next.</span></span> <span data-ttu-id="2ebe1-117">Si la valeur est true, toutes les visualisations inscrites sur le système de l’utilisateur peuvent être recyclees.</span><span class="sxs-lookup"><span data-stu-id="2ebe1-117">If it is set to true, then all visualizations that are registered on the user's system can be cycled through.</span></span> <span data-ttu-id="2ebe1-118">Si la valeur est true et que vous spécifiez des visualisations dans les balises d' **effets** , les attributs spécifiés dans ces balises sont appliqués à toutes les visualisations sur le système de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2ebe1-118">If it is set to true and you specify any visualizations within **EFFECTS** tags, then the attributes specified in these tags are applied to all visualizations on the user's system.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ebe1-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ebe1-119">Requirements</span></span>



| <span data-ttu-id="2ebe1-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ebe1-120">Requirement</span></span> | <span data-ttu-id="2ebe1-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ebe1-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="2ebe1-122">Version</span><span class="sxs-lookup"><span data-stu-id="2ebe1-122">Version</span></span><br/> | <span data-ttu-id="2ebe1-123">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="2ebe1-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2ebe1-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ebe1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ebe1-125">**Élément EFFECTs**</span><span class="sxs-lookup"><span data-stu-id="2ebe1-125">**EFFECTS Element**</span></span>](effects-element.md)
</dt> </dl>

 

 





