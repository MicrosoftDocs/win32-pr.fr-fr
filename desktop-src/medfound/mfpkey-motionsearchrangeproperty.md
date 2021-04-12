---
description: Spécifie la plage utilisée dans les recherches de mouvement.
ms.assetid: b2026f47-ac39-4276-8359-c939b202f00c
title: MFPKEY_MOTIONSEARCHRANGE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c557ea1a462192434222e425dccb8b9a0e291986
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202347"
---
# <a name="mfpkey_motionsearchrange-property"></a><span data-ttu-id="0084f-103">MFPKEY \_ propriété MOTIONSEARCHRANGE</span><span class="sxs-lookup"><span data-stu-id="0084f-103">MFPKEY\_MOTIONSEARCHRANGE Property</span></span>

<span data-ttu-id="0084f-104">Spécifie la plage utilisée dans les recherches de mouvement.</span><span class="sxs-lookup"><span data-stu-id="0084f-104">Specifies the range used in motion searches.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="0084f-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="0084f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="0084f-106">\_wszWMVCMotionSearchRange g</span><span class="sxs-lookup"><span data-stu-id="0084f-106">g\_wszWMVCMotionSearchRange</span></span>

## <a name="data-type"></a><span data-ttu-id="0084f-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="0084f-107">Data Type</span></span>

<span data-ttu-id="0084f-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="0084f-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="0084f-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="0084f-109">Default Value</span></span>

<span data-ttu-id="0084f-110">0</span><span class="sxs-lookup"><span data-stu-id="0084f-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="0084f-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0084f-111">Remarks</span></span>

<span data-ttu-id="0084f-112">Cette propriété peut être définie sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="0084f-112">This property may be set to one of the following values.</span></span> <span data-ttu-id="0084f-113">H indique une plage horizontale et une plage verticale.</span><span class="sxs-lookup"><span data-stu-id="0084f-113">H denotes horizontal range and V denotes vertical range.</span></span> <span data-ttu-id="0084f-114">Toutes les plages sont indiquées en pixels.</span><span class="sxs-lookup"><span data-stu-id="0084f-114">All ranges are given in pixels.</span></span>



| <span data-ttu-id="0084f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0084f-115">Value</span></span> | <span data-ttu-id="0084f-116">Plage</span><span class="sxs-lookup"><span data-stu-id="0084f-116">Range</span></span>                                |
|-------|--------------------------------------|
| <span data-ttu-id="0084f-117">0</span><span class="sxs-lookup"><span data-stu-id="0084f-117">0</span></span>     | <span data-ttu-id="0084f-118">+ 63.75/-64 H, + 31.75/-32.0 V</span><span class="sxs-lookup"><span data-stu-id="0084f-118">+63.75/-64.0 H, +31.75/-32.0 V</span></span>       |
| <span data-ttu-id="0084f-119">1</span><span class="sxs-lookup"><span data-stu-id="0084f-119">1</span></span>     | <span data-ttu-id="0084f-120">+ 127.75/-128.0 H, + 63.75/-64 V</span><span class="sxs-lookup"><span data-stu-id="0084f-120">+127.75/-128.0 H, +63.75/-64.0 V</span></span>     |
| <span data-ttu-id="0084f-121">2</span><span class="sxs-lookup"><span data-stu-id="0084f-121">2</span></span>     | <span data-ttu-id="0084f-122">+511,75/-512,0 H, +127,75/-128,0 V</span><span class="sxs-lookup"><span data-stu-id="0084f-122">+511.75/-512.0 H, +127.75/-128.0 V</span></span>   |
| <span data-ttu-id="0084f-123">3</span><span class="sxs-lookup"><span data-stu-id="0084f-123">3</span></span>     | <span data-ttu-id="0084f-124">+ 1023.75/-1024.0 H, + 255.75/-256.0 V</span><span class="sxs-lookup"><span data-stu-id="0084f-124">+1023.75/-1024.0 H, +255.75/-256.0 V</span></span> |
| <span data-ttu-id="0084f-125">-1</span><span class="sxs-lookup"><span data-stu-id="0084f-125">-1</span></span>    | <span data-ttu-id="0084f-126">Bloc macro-adaptative (automatique)</span><span class="sxs-lookup"><span data-stu-id="0084f-126">Macroblock-adaptive (automatic)</span></span>      |



 

<span data-ttu-id="0084f-127">Cette propriété contrôle la taille de la zone Frame dans laquelle le codec recherchera un élément pouvant avoir un mouvement entre les frames.</span><span class="sxs-lookup"><span data-stu-id="0084f-127">This property controls the size of the frame area that the codec will search for an element that may have exhibited motion between frames.</span></span> <span data-ttu-id="0084f-128">Une plus grande fenêtre de recherche permet de trouver un mouvement plus rapide, mais elle nécessite plus de temps processeur.</span><span class="sxs-lookup"><span data-stu-id="0084f-128">A larger search window will help find faster motion but will require more CPU time.</span></span> <span data-ttu-id="0084f-129">Les exigences de l’UC sont approximativement doublées à chaque niveau.</span><span class="sxs-lookup"><span data-stu-id="0084f-129">The CPU requirements are approximately doubled at each level.</span></span>

<span data-ttu-id="0084f-130">Le mode automatique (-1) sélectionne dynamiquement le mode le plus efficace.</span><span class="sxs-lookup"><span data-stu-id="0084f-130">The automatic mode (-1) will dynamically select the most efficient mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="0084f-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0084f-131">Requirements</span></span>



| <span data-ttu-id="0084f-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0084f-132">Requirement</span></span> | <span data-ttu-id="0084f-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="0084f-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0084f-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0084f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0084f-135">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0084f-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0084f-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0084f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0084f-137">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0084f-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0084f-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="0084f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="0084f-139"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0084f-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0084f-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0084f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0084f-141">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0084f-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




