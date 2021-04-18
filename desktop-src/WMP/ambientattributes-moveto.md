---
title: AmbientAttributes. moveTo
description: La méthode moveTo déplace le contrôle vers un nouvel emplacement à une vitesse linéaire.
ms.assetid: 8670aa7b-a5c1-4d93-9f48-452bc53e65e6
keywords:
- AmbientAttributes. moveTo lecteur Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.moveTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af481526c0923c527bb14aa4700a6c6fe5ea3613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540420"
---
# <a name="ambientattributesmoveto"></a><span data-ttu-id="fe6bb-104">AmbientAttributes. moveTo</span><span class="sxs-lookup"><span data-stu-id="fe6bb-104">AmbientAttributes.moveTo</span></span>

<span data-ttu-id="fe6bb-105">La méthode **MoveTo** déplace le contrôle vers un nouvel emplacement à une vitesse linéaire.</span><span class="sxs-lookup"><span data-stu-id="fe6bb-105">The **moveTo** method moves the control to a new location at a linear speed.</span></span>

``` syntax
        elementID.moveTo(newLeft, newTop, time)
```

## <a name="parameters"></a><span data-ttu-id="fe6bb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe6bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe6bb-107"><span id="newLeft"></span><span id="newleft"></span><span id="NEWLEFT"></span>*newLeft*</span><span class="sxs-lookup"><span data-stu-id="fe6bb-107"><span id="newLeft"></span><span id="newleft"></span><span id="NEWLEFT"></span>*newLeft*</span></span>
</dt> <dd>

<span data-ttu-id="fe6bb-108">**Nombre** (**long**) spécifiant la nouvelle valeur de l’attribut de **gauche** du contrôle.</span><span class="sxs-lookup"><span data-stu-id="fe6bb-108">**Number** (**long**) specifying the new value for the **left** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="fe6bb-109"><span id="newTop"></span><span id="newtop"></span><span id="NEWTOP"></span>*newTop*</span><span class="sxs-lookup"><span data-stu-id="fe6bb-109"><span id="newTop"></span><span id="newtop"></span><span id="NEWTOP"></span>*newTop*</span></span>
</dt> <dd>

<span data-ttu-id="fe6bb-110">**Nombre** (**long**) spécifiant la nouvelle valeur de l’attribut **Top** du contrôle.</span><span class="sxs-lookup"><span data-stu-id="fe6bb-110">**Number** (**long**) specifying the new value for the **top** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="fe6bb-111"><span id="time"></span><span id="TIME"></span>*simultanément*</span><span class="sxs-lookup"><span data-stu-id="fe6bb-111"><span id="time"></span><span id="TIME"></span>*time*</span></span>
</dt> <dd>

<span data-ttu-id="fe6bb-112">**Nombre** (**long**) spécifiant la durée, en millisecondes, nécessaire au déplacement du contrôle vers son nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="fe6bb-112">**Number** (**long**) specifying the time, in milliseconds, that it takes for the control to move to its new location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe6bb-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fe6bb-113">Return Value</span></span>

<span data-ttu-id="fe6bb-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="fe6bb-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe6bb-115">Notes</span><span class="sxs-lookup"><span data-stu-id="fe6bb-115">Remarks</span></span>

<span data-ttu-id="fe6bb-116">Cette méthode est utile pour les éléments de sous- **affichage** animés (par exemple, si l’utilisateur clique sur une barre d’État et les contrôles déroulants).</span><span class="sxs-lookup"><span data-stu-id="fe6bb-116">This method is useful for animated **SUBVIEW** elements (for example, if the user clicks a tray and the controls slide down).</span></span>

<span data-ttu-id="fe6bb-117">Cette méthode crée un mouvement linéaire lors du déplacement du contrôle.</span><span class="sxs-lookup"><span data-stu-id="fe6bb-117">This method creates a linear motion when moving the control.</span></span> <span data-ttu-id="fe6bb-118">Cela diffère de **slideTo**, qui crée un mouvement non linéaire.</span><span class="sxs-lookup"><span data-stu-id="fe6bb-118">This differs from **slideTo**, which creates a non-linear motion.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe6bb-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe6bb-119">Requirements</span></span>



| <span data-ttu-id="fe6bb-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe6bb-120">Requirement</span></span> | <span data-ttu-id="fe6bb-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe6bb-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="fe6bb-122">Version</span><span class="sxs-lookup"><span data-stu-id="fe6bb-122">Version</span></span><br/> | <span data-ttu-id="fe6bb-123">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="fe6bb-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fe6bb-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe6bb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe6bb-125">**Attributs ambiants**</span><span class="sxs-lookup"><span data-stu-id="fe6bb-125">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="fe6bb-126">**AmbientAttributes. Left**</span><span class="sxs-lookup"><span data-stu-id="fe6bb-126">**AmbientAttributes.left**</span></span>](ambientattributes-left.md)
</dt> <dt>

[<span data-ttu-id="fe6bb-127">**AmbientAttributes.slideTo**</span><span class="sxs-lookup"><span data-stu-id="fe6bb-127">**AmbientAttributes.slideTo**</span></span>](ambientattributes-slideto.md)
</dt> <dt>

[<span data-ttu-id="fe6bb-128">**AmbientAttributes.top**</span><span class="sxs-lookup"><span data-stu-id="fe6bb-128">**AmbientAttributes.top**</span></span>](ambientattributes-top.md)
</dt> </dl>

 

 





