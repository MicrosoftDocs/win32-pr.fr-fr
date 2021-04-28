---
description: D3DXVec2Transform, fonction (D3DX10Math. h)-transforme un vecteur 2D par une matrice donnée.
ms.assetid: 4b57eb7f-fae9-48ac-a806-510da75d25a6
title: D3DXVec2Transform, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Transform
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b1d8eed447b56e6f379ffe96cbbcb4820fbdaf14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108357"
---
# <a name="d3dxvec2transform-function-d3dx10mathh"></a><span data-ttu-id="cc50b-103">D3DXVec2Transform, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="cc50b-103">D3DXVec2Transform function (D3DX10Math.h)</span></span>

<span data-ttu-id="cc50b-104">Transforme un vecteur 2D par une matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="cc50b-104">Transforms a 2D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc50b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc50b-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec2Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="cc50b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc50b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc50b-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cc50b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc50b-108">Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="cc50b-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="cc50b-109">Pointeur vers la structure [**D3DXVECTOR4**](d3d10-d3dxvector4.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="cc50b-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="cc50b-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc50b-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc50b-111">Type : **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="cc50b-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="cc50b-112">Pointeur vers le [**D3DXVECTOR2**](d3d10-d3dxvector2.md)source.</span><span class="sxs-lookup"><span data-stu-id="cc50b-112">Pointer to the source [**D3DXVECTOR2**](d3d10-d3dxvector2.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc50b-113">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc50b-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc50b-114">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="cc50b-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="cc50b-115">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="cc50b-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc50b-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cc50b-116">Return value</span></span>

<span data-ttu-id="cc50b-117">Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="cc50b-117">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="cc50b-118">Pointeur vers une structure D3DXVECTOR4 qui est le vecteur transformé.</span><span class="sxs-lookup"><span data-stu-id="cc50b-118">Pointer to a D3DXVECTOR4 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc50b-119">Notes </span><span class="sxs-lookup"><span data-stu-id="cc50b-119">Remarks</span></span>

<span data-ttu-id="cc50b-120">Cette fonction transforme le vecteur pV (x, y, 0, 1) par la matrice pM.</span><span class="sxs-lookup"><span data-stu-id="cc50b-120">This function transforms the vector pV (x, y, 0, 1) by the matrix pM.</span></span>

<span data-ttu-id="cc50b-121">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="cc50b-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="cc50b-122">De cette façon, la fonction D3DXVec2Transform peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="cc50b-122">In this way, the D3DXVec2Transform function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc50b-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc50b-123">Requirements</span></span>



| <span data-ttu-id="cc50b-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc50b-124">Requirement</span></span> | <span data-ttu-id="cc50b-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc50b-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc50b-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc50b-126">Header</span></span><br/>  | <dl> <span data-ttu-id="cc50b-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc50b-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="cc50b-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cc50b-128">Library</span></span><br/> | <dl> <span data-ttu-id="cc50b-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc50b-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cc50b-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc50b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc50b-131">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="cc50b-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
