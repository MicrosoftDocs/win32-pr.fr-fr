---
title: AmbientAttributes.alphaBlendTo
description: La méthode alphaBlendTo ajuste la propriété alphaBlend sur une période donnée.
ms.assetid: 5cb259bd-3010-4086-be9d-65022be297b7
keywords:
- Lecteur Windows Media AmbientAttributes. alphaBlendTo
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlendTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16b21e78de3510e2e4a58c7214995f7888f778c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545425"
---
# <a name="ambientattributesalphablendto"></a><span data-ttu-id="989dc-104">AmbientAttributes.alphaBlendTo</span><span class="sxs-lookup"><span data-stu-id="989dc-104">AmbientAttributes.alphaBlendTo</span></span>

<span data-ttu-id="989dc-105">La méthode **alphaBlendTo** ajuste la propriété **alphaBlend** sur une période donnée.</span><span class="sxs-lookup"><span data-stu-id="989dc-105">The **alphaBlendTo** method adjusts the **alphaBlend** property over a period of time.</span></span>

``` syntax
        elementID.alphaBlendTo(newVal, alphaTime)
```

## <a name="parameters"></a><span data-ttu-id="989dc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="989dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="989dc-107"><span id="newVal"></span><span id="newval"></span><span id="NEWVAL"></span>*newVal*</span><span class="sxs-lookup"><span data-stu-id="989dc-107"><span id="newVal"></span><span id="newval"></span><span id="NEWVAL"></span>*newVal*</span></span>
</dt> <dd>

<span data-ttu-id="989dc-108">**Nombre** (long) spécifiant la nouvelle valeur d’opacité.</span><span class="sxs-lookup"><span data-stu-id="989dc-108">**Number** (long) specifying the new opacity value.</span></span> <span data-ttu-id="989dc-109">La plage est comprise entre 0 (aucune opacité) et 255 (opacité complète).</span><span class="sxs-lookup"><span data-stu-id="989dc-109">Ranges from 0 (no opacity) to 255 (full opacity).</span></span>

</dd> <dt>

<span data-ttu-id="989dc-110"><span id="alphaTime"></span><span id="alphatime"></span><span id="ALPHATIME"></span>*alphaTime*</span><span class="sxs-lookup"><span data-stu-id="989dc-110"><span id="alphaTime"></span><span id="alphatime"></span><span id="ALPHATIME"></span>*alphaTime*</span></span>
</dt> <dd>

<span data-ttu-id="989dc-111">**Nombre** (**long**) spécifiant la durée, en millisecondes, nécessaire à l’élément pour modifier l’opacité.</span><span class="sxs-lookup"><span data-stu-id="989dc-111">**Number** (**long**) specifying the time, in milliseconds, that it takes the element to change opacity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="989dc-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="989dc-112">Return Value</span></span>

<span data-ttu-id="989dc-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="989dc-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="989dc-114">Notes</span><span class="sxs-lookup"><span data-stu-id="989dc-114">Remarks</span></span>

<span data-ttu-id="989dc-115">Cette méthode est utile pour faire apparaître ou disparaître progressivement des éléments.</span><span class="sxs-lookup"><span data-stu-id="989dc-115">This method is useful for making elements gradually appear or disappear.</span></span>

<span data-ttu-id="989dc-116">Quand vous utilisez **alphaBlendTo** avec un élément de **texte** pour lequel le **backgroundColor** n’est pas spécifié, une couleur d’arrière-plan noire est utilisée.</span><span class="sxs-lookup"><span data-stu-id="989dc-116">When you use **alphaBlendTo** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="989dc-117">Si la couleur de premier plan est également noire (valeur par défaut pour le *texte*).**foregroundColor**), votre texte peut devenir illisible.</span><span class="sxs-lookup"><span data-stu-id="989dc-117">If the foreground color is also black (which is the default value for *TEXT*.**foregroundColor**), your text may become unreadable.</span></span> <span data-ttu-id="989dc-118">Pour éviter cela, spécifiez toujours l’attribut **backgroundColor** ou définissez **foregroundColor** sur une couleur autre que Black.</span><span class="sxs-lookup"><span data-stu-id="989dc-118">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

> [!Note]  
> <span data-ttu-id="989dc-119">Cet attribut n’est pas pris en charge dans Windows 98.</span><span class="sxs-lookup"><span data-stu-id="989dc-119">This attribute is not supported in Windows 98.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="989dc-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="989dc-120">Requirements</span></span>



| <span data-ttu-id="989dc-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="989dc-121">Requirement</span></span> | <span data-ttu-id="989dc-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="989dc-122">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="989dc-123">Version</span><span class="sxs-lookup"><span data-stu-id="989dc-123">Version</span></span><br/> | <span data-ttu-id="989dc-124">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="989dc-124">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="989dc-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="989dc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="989dc-126">**Attributs ambiants**</span><span class="sxs-lookup"><span data-stu-id="989dc-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="989dc-127">**AmbientAttributes. alphaBlend**</span><span class="sxs-lookup"><span data-stu-id="989dc-127">**AmbientAttributes.alphaBlend**</span></span>](ambientattributes-alphablend.md)
</dt> <dt>

[<span data-ttu-id="989dc-128">**Élément de texte**</span><span class="sxs-lookup"><span data-stu-id="989dc-128">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="989dc-129">**TEXT. backgroundColor**</span><span class="sxs-lookup"><span data-stu-id="989dc-129">**TEXT.backgroundColor**</span></span>](text-backgroundcolor.md)
</dt> <dt>

[<span data-ttu-id="989dc-130">**TEXT. foregroundColor**</span><span class="sxs-lookup"><span data-stu-id="989dc-130">**TEXT.foregroundColor**</span></span>](text-foregroundcolor.md)
</dt> </dl>

 

 





