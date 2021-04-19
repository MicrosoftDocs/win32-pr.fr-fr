---
title: AmbientAttributes.moveSizeTo
description: La méthode moveSizeTo déplace le contrôle et spécifie une nouvelle taille pour le contrôle dans le nouvel emplacement. Le contrôle se déplace et se redimensionne de manière animée sur la période spécifiée.
ms.assetid: 89e3bf16-a123-4fb1-8c24-bc22a978e7f6
keywords:
- Lecteur Windows Media AmbientAttributes. moveSizeTo
topic_type:
- apiref
api_name:
- AmbientAttributes.moveSizeTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 406d48772e85a55ab82241518d499182931cc2fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525182"
---
# <a name="ambientattributesmovesizeto"></a><span data-ttu-id="1b3a7-105">AmbientAttributes.moveSizeTo</span><span class="sxs-lookup"><span data-stu-id="1b3a7-105">AmbientAttributes.moveSizeTo</span></span>

<span data-ttu-id="1b3a7-106">La méthode **moveSizeTo** déplace le contrôle et spécifie une nouvelle taille pour le contrôle dans le nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-106">The **moveSizeTo** method moves the control and specifies a new size for the control in the new location.</span></span> <span data-ttu-id="1b3a7-107">Le contrôle se déplace et se redimensionne de manière animée sur la période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-107">The control moves and resizes in an animated fashion over the specified time period.</span></span>

``` syntax
        elementID.moveSizeTo(newX, newY, newWidth, newHeight, moveTime, fSlide)
```

## <a name="parameters"></a><span data-ttu-id="1b3a7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b3a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b3a7-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*</span><span class="sxs-lookup"><span data-stu-id="1b3a7-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*</span></span>
</dt> <dd>

<span data-ttu-id="1b3a7-110">**Nombre** (**long**) spécifiant la nouvelle valeur de l’attribut de **gauche** du contrôle.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-110">**Number** (**long**) specifying the new value for the **left** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="1b3a7-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*</span><span class="sxs-lookup"><span data-stu-id="1b3a7-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*</span></span>
</dt> <dd>

<span data-ttu-id="1b3a7-112">**Nombre** (**long**) spécifiant la nouvelle valeur de l’attribut **Top** du contrôle.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-112">**Number** (**long**) specifying the new value for the **top** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="1b3a7-113"><span id="newWidth"></span><span id="newwidth"></span><span id="NEWWIDTH"></span>*newWidth*</span><span class="sxs-lookup"><span data-stu-id="1b3a7-113"><span id="newWidth"></span><span id="newwidth"></span><span id="NEWWIDTH"></span>*newWidth*</span></span>
</dt> <dd>

<span data-ttu-id="1b3a7-114">**Nombre** (**long**) spécifiant la nouvelle valeur de l’attribut **Width** du contrôle.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-114">**Number** (**long**) specifying the new value for the **width** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="1b3a7-115"><span id="newHeight"></span><span id="newheight"></span><span id="NEWHEIGHT"></span>*newHeight*</span><span class="sxs-lookup"><span data-stu-id="1b3a7-115"><span id="newHeight"></span><span id="newheight"></span><span id="NEWHEIGHT"></span>*newHeight*</span></span>
</dt> <dd>

<span data-ttu-id="1b3a7-116">**Nombre** (**long**) spécifiant la nouvelle valeur de l’attribut **Height** du contrôle.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-116">**Number** (**long**) specifying the new value for the **height** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="1b3a7-117"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*</span><span class="sxs-lookup"><span data-stu-id="1b3a7-117"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*</span></span>
</dt> <dd>

<span data-ttu-id="1b3a7-118">**Nombre** (**long**) spécifiant la durée, en millisecondes, nécessaire au déplacement du contrôle vers son nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-118">**Number** (**long**) specifying the time, in milliseconds, that it takes for the control to move to its new location.</span></span>

</dd> <dt>

<span data-ttu-id="1b3a7-119"><span id="fSlide"></span><span id="fslide"></span><span id="FSLIDE"></span>*fSlide*</span><span class="sxs-lookup"><span data-stu-id="1b3a7-119"><span id="fSlide"></span><span id="fslide"></span><span id="FSLIDE"></span>*fSlide*</span></span>
</dt> <dd>

<span data-ttu-id="1b3a7-120">**Valeur booléenne** qui spécifie le type de mouvement créé lors du déplacement du contrôle.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-120">**Boolean** specifying the type of motion created when moving the control.</span></span>



| <span data-ttu-id="1b3a7-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b3a7-121">Value</span></span> | <span data-ttu-id="1b3a7-122">Description</span><span class="sxs-lookup"><span data-stu-id="1b3a7-122">Description</span></span>                                                             |
|-------|-------------------------------------------------------------------------|
| <span data-ttu-id="1b3a7-123">true</span><span class="sxs-lookup"><span data-stu-id="1b3a7-123">true</span></span>  | <span data-ttu-id="1b3a7-124">Motion est non linéaire (mouvement coulissant qui accélère et ralentit).</span><span class="sxs-lookup"><span data-stu-id="1b3a7-124">Motion is non-linear (sliding motion that accelerates and decelerates).</span></span> |
| <span data-ttu-id="1b3a7-125">false</span><span class="sxs-lookup"><span data-stu-id="1b3a7-125">false</span></span> | <span data-ttu-id="1b3a7-126">Motion est linéaire.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-126">Motion is linear.</span></span>                                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b3a7-127">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1b3a7-127">Return Value</span></span>

<span data-ttu-id="1b3a7-128">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-128">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b3a7-129">Notes</span><span class="sxs-lookup"><span data-stu-id="1b3a7-129">Remarks</span></span>

<span data-ttu-id="1b3a7-130">Le mouvement du contrôle peut être linéaire ou non linéaire.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-130">The motion of the control can be linear or non-linear.</span></span> <span data-ttu-id="1b3a7-131">Le mouvement linéaire signifie que le contrôle se déplace à une vitesse constante jusqu’à son nouvel emplacement, en démarrant et en arrêt brutalement.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-131">Linear motion means the control moves at a constant speed to its new location, starting and stopping abruptly.</span></span> <span data-ttu-id="1b3a7-132">Lorsque vous spécifiez un mouvement non linéaire, un mouvement coulissant est créé, ce qui accélère la valeur zéro au début du mouvement et ralentit vers la valeur zéro à la fin, en partant d’un arrêt lisse.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-132">When non-linear motion is specified, a sliding motion is created that accelerates from zero at the beginning of the motion and decelerates back to zero at the end, coming to a smooth stop.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b3a7-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b3a7-133">Requirements</span></span>



| <span data-ttu-id="1b3a7-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b3a7-134">Requirement</span></span> | <span data-ttu-id="1b3a7-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b3a7-135">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="1b3a7-136">Version</span><span class="sxs-lookup"><span data-stu-id="1b3a7-136">Version</span></span><br/> | <span data-ttu-id="1b3a7-137">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="1b3a7-137">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1b3a7-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b3a7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b3a7-139">**Attributs ambiants**</span><span class="sxs-lookup"><span data-stu-id="1b3a7-139">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="1b3a7-140">**AmbientAttributes. Height**</span><span class="sxs-lookup"><span data-stu-id="1b3a7-140">**AmbientAttributes.height**</span></span>](ambientattributes-height.md)
</dt> <dt>

[<span data-ttu-id="1b3a7-141">**AmbientAttributes. Left**</span><span class="sxs-lookup"><span data-stu-id="1b3a7-141">**AmbientAttributes.left**</span></span>](ambientattributes-left.md)
</dt> <dt>

[<span data-ttu-id="1b3a7-142">**AmbientAttributes.top**</span><span class="sxs-lookup"><span data-stu-id="1b3a7-142">**AmbientAttributes.top**</span></span>](ambientattributes-top.md)
</dt> <dt>

[<span data-ttu-id="1b3a7-143">**AmbientAttributes. Width**</span><span class="sxs-lookup"><span data-stu-id="1b3a7-143">**AmbientAttributes.width**</span></span>](ambientattributes-width.md)
</dt> </dl>

 

 





