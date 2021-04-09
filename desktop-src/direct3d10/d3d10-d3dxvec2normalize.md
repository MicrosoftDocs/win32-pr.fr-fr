---
description: Retourne la version normalisée d’un vecteur 2D.
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
ms.openlocfilehash: e2894a86c0aa0c2ef6b45a41664b2d0cca1427c1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870166"
---
# <a name="d3dxvec2normalize-function-d3dx10mathh"></a><span data-ttu-id="656b6-103">D3DXVec2Normalize, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="656b6-103">D3DXVec2Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="656b6-104">Retourne la version normalisée d’un vecteur 2D.</span><span class="sxs-lookup"><span data-stu-id="656b6-104">Returns the normalized version of a 2D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="656b6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="656b6-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Normalize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="656b6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="656b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="656b6-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="656b6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="656b6-108">Type : **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="656b6-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="656b6-109">Pointeur vers le [**D3DXVECTOR2**](d3d10-d3dxvector2.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="656b6-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="656b6-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="656b6-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="656b6-111">Type : **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="656b6-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="656b6-112">Pointeur vers la structure D3DXVECTOR2 source.</span><span class="sxs-lookup"><span data-stu-id="656b6-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="656b6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="656b6-113">Return value</span></span>

<span data-ttu-id="656b6-114">Type : **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="656b6-114">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="656b6-115">Pointeur vers une structure D3DXVECTOR2 qui est la version normalisée du vecteur.</span><span class="sxs-lookup"><span data-stu-id="656b6-115">Pointer to a D3DXVECTOR2 structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="656b6-116">Notes</span><span class="sxs-lookup"><span data-stu-id="656b6-116">Remarks</span></span>

<span data-ttu-id="656b6-117">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="656b6-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="656b6-118">De cette façon, la fonction D3DXVec2Normalize peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="656b6-118">In this way, the D3DXVec2Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="656b6-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="656b6-119">Requirements</span></span>



| <span data-ttu-id="656b6-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="656b6-120">Requirement</span></span> | <span data-ttu-id="656b6-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="656b6-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="656b6-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="656b6-122">Header</span></span><br/>  | <dl> <span data-ttu-id="656b6-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="656b6-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="656b6-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="656b6-124">Library</span></span><br/> | <dl> <span data-ttu-id="656b6-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="656b6-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="656b6-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="656b6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="656b6-127">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="656b6-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
