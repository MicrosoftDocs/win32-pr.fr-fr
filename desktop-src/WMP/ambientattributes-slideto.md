---
title: AmbientAttributes.slideTo
description: La méthode slideTo déplace le contrôle vers un nouvel emplacement. Le contrôle se déplace de manière non linéaire sur la période spécifiée.
ms.assetid: 06dd610b-cb58-4b60-9f4b-8929c54c3c33
keywords:
- Lecteur Windows Media AmbientAttributes. slideTo
topic_type:
- apiref
api_name:
- AmbientAttributes.slideTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deb214046ace59094b6bd5c362dfa716b9fceb57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528980"
---
# <a name="ambientattributesslideto"></a><span data-ttu-id="22c42-105">AmbientAttributes.slideTo</span><span class="sxs-lookup"><span data-stu-id="22c42-105">AmbientAttributes.slideTo</span></span>

<span data-ttu-id="22c42-106">La méthode **slideTo** déplace le contrôle vers un nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="22c42-106">The **slideTo** method moves the control to a new location.</span></span> <span data-ttu-id="22c42-107">Le contrôle se déplace de manière non linéaire sur la période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="22c42-107">The control moves in a non-linear fashion over the specified time period.</span></span>

``` syntax
        elementID.slideTo(newX, newY, moveTime)
```

## <a name="parameters"></a><span data-ttu-id="22c42-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22c42-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22c42-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*</span><span class="sxs-lookup"><span data-stu-id="22c42-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*</span></span>
</dt> <dd>

<span data-ttu-id="22c42-110">**Nombre** (**long**) spécifiant la nouvelle valeur de l’attribut de **gauche** du contrôle.</span><span class="sxs-lookup"><span data-stu-id="22c42-110">**Number** (**long**) specifying the new value for the **left** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="22c42-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*</span><span class="sxs-lookup"><span data-stu-id="22c42-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*</span></span>
</dt> <dd>

<span data-ttu-id="22c42-112">**Nombre** (**long**) spécifiant la nouvelle valeur de l’attribut **Top** du contrôle.</span><span class="sxs-lookup"><span data-stu-id="22c42-112">**Number** (**long**) specifying the new value for the **top** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="22c42-113"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*</span><span class="sxs-lookup"><span data-stu-id="22c42-113"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*</span></span>
</dt> <dd>

<span data-ttu-id="22c42-114">**Nombre** (**long**) spécifiant la durée, en millisecondes, nécessaire au déplacement du contrôle vers son nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="22c42-114">**Number** (**long**) specifying the time, in milliseconds, that it takes for the control to move to its new location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22c42-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="22c42-115">Return Value</span></span>

<span data-ttu-id="22c42-116">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="22c42-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="22c42-117">Notes</span><span class="sxs-lookup"><span data-stu-id="22c42-117">Remarks</span></span>

<span data-ttu-id="22c42-118">Cette méthode est différente de **MoveTo**, qui crée un mouvement linéaire lors du déplacement du contrôle.</span><span class="sxs-lookup"><span data-stu-id="22c42-118">This method is different from **moveTo**, which creates a linear motion when moving the control.</span></span> <span data-ttu-id="22c42-119">Le mouvement non linéaire créé par cette méthode est un mouvement coulissant qui accélère à partir d’une vitesse nulle au début du mouvement et ralentit à zéro à la fin, en arrivant à un arrêt sans heurts.</span><span class="sxs-lookup"><span data-stu-id="22c42-119">The non-linear motion created by this method is a sliding motion that accelerates from a speed of zero at the beginning of the motion and decelerates back to zero at the end, coming to a smooth stop.</span></span>

## <a name="requirements"></a><span data-ttu-id="22c42-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22c42-120">Requirements</span></span>



| <span data-ttu-id="22c42-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22c42-121">Requirement</span></span> | <span data-ttu-id="22c42-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="22c42-122">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="22c42-123">Version</span><span class="sxs-lookup"><span data-stu-id="22c42-123">Version</span></span><br/> | <span data-ttu-id="22c42-124">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="22c42-124">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="22c42-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22c42-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22c42-126">**Attributs ambiants**</span><span class="sxs-lookup"><span data-stu-id="22c42-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="22c42-127">**AmbientAttributes. Left**</span><span class="sxs-lookup"><span data-stu-id="22c42-127">**AmbientAttributes.left**</span></span>](ambientattributes-left.md)
</dt> <dt>

[<span data-ttu-id="22c42-128">**AmbientAttributes. moveTo**</span><span class="sxs-lookup"><span data-stu-id="22c42-128">**AmbientAttributes.moveTo**</span></span>](ambientattributes-moveto.md)
</dt> <dt>

[<span data-ttu-id="22c42-129">**AmbientAttributes.top**</span><span class="sxs-lookup"><span data-stu-id="22c42-129">**AmbientAttributes.top**</span></span>](ambientattributes-top.md)
</dt> </dl>

 

 





