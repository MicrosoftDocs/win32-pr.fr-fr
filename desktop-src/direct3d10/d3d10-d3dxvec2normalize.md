---
description: 'D3DXVec2Normalize, fonction (D3DX10Math. h) : retourne la version normalisée d’un vecteur 2D.'
ms.assetid: fac4f269-2778-4500-af9e-23a0112543b0
title: D3DXVec2Normalize, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Normalize
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: aaa7bde759b9023b69204d6cb39259f0905b9928
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108387"
---
# <a name="d3dxvec2normalize-function-d3dx10mathh"></a><span data-ttu-id="8e846-103">D3DXVec2Normalize, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="8e846-103">D3DXVec2Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="8e846-104">Retourne la version normalisée d’un vecteur 2D.</span><span class="sxs-lookup"><span data-stu-id="8e846-104">Returns the normalized version of a 2D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e846-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e846-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Normalize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="8e846-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e846-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e846-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8e846-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e846-108">Type : **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="8e846-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="8e846-109">Pointeur vers le [**D3DXVECTOR2**](d3d10-d3dxvector2.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="8e846-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8e846-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8e846-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e846-111">Type : **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="8e846-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="8e846-112">Pointeur vers la structure D3DXVECTOR2 source.</span><span class="sxs-lookup"><span data-stu-id="8e846-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e846-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8e846-113">Return value</span></span>

<span data-ttu-id="8e846-114">Type : **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="8e846-114">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="8e846-115">Pointeur vers une structure D3DXVECTOR2 qui est la version normalisée du vecteur.</span><span class="sxs-lookup"><span data-stu-id="8e846-115">Pointer to a D3DXVECTOR2 structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e846-116">Notes </span><span class="sxs-lookup"><span data-stu-id="8e846-116">Remarks</span></span>

<span data-ttu-id="8e846-117">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="8e846-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="8e846-118">De cette façon, la fonction D3DXVec2Normalize peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="8e846-118">In this way, the D3DXVec2Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e846-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e846-119">Requirements</span></span>



| <span data-ttu-id="8e846-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e846-120">Requirement</span></span> | <span data-ttu-id="8e846-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e846-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e846-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="8e846-122">Header</span></span><br/>  | <dl> <span data-ttu-id="8e846-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e846-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="8e846-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8e846-124">Library</span></span><br/> | <dl> <span data-ttu-id="8e846-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e846-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8e846-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e846-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e846-127">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="8e846-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
