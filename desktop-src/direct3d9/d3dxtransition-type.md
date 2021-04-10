---
description: Définit le style de transition entre les valeurs d’une animation de maillage.
ms.assetid: 4416ef28-ba6b-47ca-be7d-831daad619e5
title: Énumération D3DXTRANSITION_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTRANSITION_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 0ca6ef7f9dcee8e865a1cd4089aecd1bc239d5d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953838"
---
# <a name="d3dxtransition_type-enumeration"></a><span data-ttu-id="f9957-103">\_Énumération de type D3DXTRANSITION</span><span class="sxs-lookup"><span data-stu-id="f9957-103">D3DXTRANSITION\_TYPE enumeration</span></span>

<span data-ttu-id="f9957-104">Définit le style de transition entre les valeurs d’une animation de maillage.</span><span class="sxs-lookup"><span data-stu-id="f9957-104">Defines the transition style between values of a mesh animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9957-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9957-105">Syntax</span></span>


```C++
typedef enum D3DXTRANSITION_TYPE { 
  D3DXTRANSITION_LINEAR         = 0x000,
  D3DXTRANSITION_EASEINEASEOUT  = 0x001,
  D3DXTRANSITION_FORCE_DWORD    = 0x7fffffff
} D3DXTRANSITION_TYPE, *LPD3DXTRANSITION_TYPE;
```



## <a name="constants"></a><span data-ttu-id="f9957-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="f9957-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f9957-107"><span id="D3DXTRANSITION_LINEAR"></span><span id="d3dxtransition_linear"></span>**D3DXTRANSITION \_ linéaire**</span><span class="sxs-lookup"><span data-stu-id="f9957-107"><span id="D3DXTRANSITION_LINEAR"></span><span id="d3dxtransition_linear"></span>**D3DXTRANSITION\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="f9957-108">Transition linéaire entre les valeurs.</span><span class="sxs-lookup"><span data-stu-id="f9957-108">Linear transition between values.</span></span>

</dd> <dt>

<span data-ttu-id="f9957-109"><span id="D3DXTRANSITION_EASEINEASEOUT"></span><span id="d3dxtransition_easeineaseout"></span>**D3DXTRANSITION \_ EASEINEASEOUT**</span><span class="sxs-lookup"><span data-stu-id="f9957-109"><span id="D3DXTRANSITION_EASEINEASEOUT"></span><span id="d3dxtransition_easeineaseout"></span>**D3DXTRANSITION\_EASEINEASEOUT**</span></span>
</dt> <dd>

<span data-ttu-id="f9957-110">Transition de spline facile et simplifiée entre les valeurs.</span><span class="sxs-lookup"><span data-stu-id="f9957-110">Ease-in, ease-out spline transition between values.</span></span>

</dd> <dt>

<span data-ttu-id="f9957-111"><span id="D3DXTRANSITION_FORCE_DWORD"></span><span id="d3dxtransition_force_dword"></span>**D3DXTRANSITION \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f9957-111"><span id="D3DXTRANSITION_FORCE_DWORD"></span><span id="d3dxtransition_force_dword"></span>**D3DXTRANSITION\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="f9957-112">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="f9957-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="f9957-113">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f9957-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="f9957-114">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="f9957-114">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9957-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f9957-115">Remarks</span></span>

<span data-ttu-id="f9957-116">Le calcul de la rampe de l’accélération de la facilité d’atténuation est calculé comme suit :</span><span class="sxs-lookup"><span data-stu-id="f9957-116">The calculation for the ramp from ease in to ease out is calculated as follows:</span></span>

<dl> <span data-ttu-id="f9957-117">Q (t) = 2 (x-y) t ³ + 3 (y-x) t ² + x</span><span class="sxs-lookup"><span data-stu-id="f9957-117">Q(t) = 2(x - y)t³ + 3(y - x)t² + x</span></span>  
</dl>

<span data-ttu-id="f9957-118">où la rampe est une fonction Q (t) avec les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="f9957-118">where the ramp is a function Q(t) with the following properties:</span></span>

-   <span data-ttu-id="f9957-119">Q (t) est une spline cubique.</span><span class="sxs-lookup"><span data-stu-id="f9957-119">Q(t) is a cubic spline.</span></span>
-   <span data-ttu-id="f9957-120">Q (t) interpole entre x et y en tant que t compris entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="f9957-120">Q(t) interpolates between x and y as t ranges from 0 to 1.</span></span>
-   <span data-ttu-id="f9957-121">Q (t) est horizontal quand t = 0 et t = 1.</span><span class="sxs-lookup"><span data-stu-id="f9957-121">Q(t) is horizontal when t = 0 and t = 1.</span></span>

<span data-ttu-id="f9957-122">Mathématiquement, cela se traduit par :</span><span class="sxs-lookup"><span data-stu-id="f9957-122">Mathematically, this translates into:</span></span>

<dl> <span data-ttu-id="f9957-123">Q (t) = à ³ + BT ² + CT + D (et par conséquent, Q' (t) = 3At ² + 2Bt + C)</span><span class="sxs-lookup"><span data-stu-id="f9957-123">Q(t) = At³ + Bt² + Ct + D (and therefore, Q'(t) = 3At² + 2Bt + C)</span></span>  
<span data-ttu-id="f9957-124">2a) Q (0) = x</span><span class="sxs-lookup"><span data-stu-id="f9957-124">2a) Q(0) = x</span></span>  
<span data-ttu-id="f9957-125">2b) Q (1) = y</span><span class="sxs-lookup"><span data-stu-id="f9957-125">2b) Q(1) = y</span></span>  
<span data-ttu-id="f9957-126">3A) Q' (0) = 0</span><span class="sxs-lookup"><span data-stu-id="f9957-126">3a) Q'(0) = 0</span></span>  
<span data-ttu-id="f9957-127">3b) Q' (1) = 0</span><span class="sxs-lookup"><span data-stu-id="f9957-127">3b) Q'(1) = 0</span></span>  
</dl>

<span data-ttu-id="f9957-128">Résolution pour A, B, C, D :</span><span class="sxs-lookup"><span data-stu-id="f9957-128">Solving for A, B, C, D:</span></span>

<dl> <span data-ttu-id="f9957-129">D = x (à partir de 2a)</span><span class="sxs-lookup"><span data-stu-id="f9957-129">D = x (from 2a)</span></span>  
<span data-ttu-id="f9957-130">C = 0 (à partir de 3A)</span><span class="sxs-lookup"><span data-stu-id="f9957-130">C = 0 (from 3a)</span></span>  
<span data-ttu-id="f9957-131">3A + 2B = 0 (à partir de 3b)</span><span class="sxs-lookup"><span data-stu-id="f9957-131">3A + 2B = 0 (from 3b)</span></span>  
<span data-ttu-id="f9957-132">A + B = y-x (à partir de 2b et D = x)</span><span class="sxs-lookup"><span data-stu-id="f9957-132">A + B = y - x (from 2b and D = x)</span></span>  
</dl>

<span data-ttu-id="f9957-133">Par conséquent :</span><span class="sxs-lookup"><span data-stu-id="f9957-133">Therefore:</span></span>

<dl> <span data-ttu-id="f9957-134">A = 2 (x-y), B = 3 (y-x), C = 0, D = x</span><span class="sxs-lookup"><span data-stu-id="f9957-134">A = 2(x - y), B = 3(y - x), C = 0, D = x</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="f9957-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9957-135">Requirements</span></span>



| <span data-ttu-id="f9957-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9957-136">Requirement</span></span> | <span data-ttu-id="f9957-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9957-137">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9957-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9957-138">Header</span></span><br/> | <dl> <span data-ttu-id="f9957-139"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9957-139"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9957-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9957-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9957-141">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="f9957-141">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




