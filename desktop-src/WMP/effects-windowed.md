---
title: EFFECTs. fenêtre
description: L’attribut Windowed spécifie ou récupère une valeur indiquant si la visualisation sera affichée ou sans fenêtre, c’est-à-dire si le rectangle entier du contrôle sera visible à tout moment, ou s’il peut être coupé.
ms.assetid: bc535274-8bc3-43bb-aab0-11899134d71e
keywords:
- EFFECTs. Windows Media Player avec fenêtres
topic_type:
- apiref
api_name:
- EFFECTS.windowed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3e30ae511c3e80e5e560f864baa8d797903fe2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534906"
---
# <a name="effectswindowed"></a><span data-ttu-id="7ef0f-104">EFFECTs. fenêtre</span><span class="sxs-lookup"><span data-stu-id="7ef0f-104">EFFECTS.windowed</span></span>

<span data-ttu-id="7ef0f-105">L’attribut **Windowed** spécifie ou récupère une valeur indiquant si la visualisation sera affichée ou sans fenêtre, c’est-à-dire si le rectangle entier du contrôle sera visible à tout moment, ou s’il peut être coupé.</span><span class="sxs-lookup"><span data-stu-id="7ef0f-105">The **windowed** attribute specifies or retrieves a value indicating whether the visualization will be windowed or windowless, that is, whether the entire rectangle of the control will be visible at all times, or whether it can be clipped.</span></span> <span data-ttu-id="7ef0f-106">Cet attribut ne peut être défini qu’au moment de la conception.</span><span class="sxs-lookup"><span data-stu-id="7ef0f-106">This attribute can only be set at design time.</span></span>

``` syntax
        elementID.windowed
```

## <a name="possible-values"></a><span data-ttu-id="7ef0f-107">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="7ef0f-107">Possible Values</span></span>

<span data-ttu-id="7ef0f-108">Cet attribut est une **valeur booléenne** spécifiée au moment de la conception et en lecture seule par la suite.</span><span class="sxs-lookup"><span data-stu-id="7ef0f-108">This attribute is a **Boolean** specified at design time and read-only thereafter.</span></span>



| <span data-ttu-id="7ef0f-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ef0f-109">Value</span></span> | <span data-ttu-id="7ef0f-110">Description</span><span class="sxs-lookup"><span data-stu-id="7ef0f-110">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="7ef0f-111">true</span><span class="sxs-lookup"><span data-stu-id="7ef0f-111">true</span></span>  | <span data-ttu-id="7ef0f-112">Le contrôle sera fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7ef0f-112">The control will be windowed.</span></span>            |
| <span data-ttu-id="7ef0f-113">false</span><span class="sxs-lookup"><span data-stu-id="7ef0f-113">false</span></span> | <span data-ttu-id="7ef0f-114">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="7ef0f-114">Default.</span></span> <span data-ttu-id="7ef0f-115">Le contrôle ne sera pas sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7ef0f-115">The control will be windowless.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7ef0f-116">Notes</span><span class="sxs-lookup"><span data-stu-id="7ef0f-116">Remarks</span></span>

<span data-ttu-id="7ef0f-117">Si vous souhaitez une fenêtre de visualisation non rectangulaire ou si une partie de la fenêtre est couverte par une image, cet attribut doit avoir la valeur false.</span><span class="sxs-lookup"><span data-stu-id="7ef0f-117">If a non-rectangular visualization window is desired, or if any part of the window is covered by an image, this attribute must be set to false.</span></span> <span data-ttu-id="7ef0f-118">Cela sacrifie certaines performances pour effectuer l’écrêtage nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7ef0f-118">This sacrifices some performance to do the necessary clipping.</span></span>

<span data-ttu-id="7ef0f-119">Si **Windowed** a la valeur true, toute image qui recouvre la fenêtre de visualisation est ignorée et la fenêtre de visualisation a l’ordre de plan le plus haut niveau.</span><span class="sxs-lookup"><span data-stu-id="7ef0f-119">If **windowed** is set to true, any image covering the visualization window is ignored, and the visualization window has the highest-level z-order.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ef0f-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ef0f-120">Requirements</span></span>



| <span data-ttu-id="7ef0f-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ef0f-121">Requirement</span></span> | <span data-ttu-id="7ef0f-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ef0f-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="7ef0f-123">Version</span><span class="sxs-lookup"><span data-stu-id="7ef0f-123">Version</span></span><br/> | <span data-ttu-id="7ef0f-124">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="7ef0f-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7ef0f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ef0f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ef0f-126">**Élément EFFECTs**</span><span class="sxs-lookup"><span data-stu-id="7ef0f-126">**EFFECTS Element**</span></span>](effects-element.md)
</dt> </dl>

 

 





