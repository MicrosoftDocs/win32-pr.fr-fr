---
description: D3DXVec2Transform, fonction (D3dx9math. h)-transforme un vecteur 2D par une matrice donnée.
ms.assetid: ccde9e34-2d99-4112-a8ed-3820d018b547
title: D3DXVec2Transform, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9b9b0f5ae0e3fda05cd8bdd92ee73b826f81b970
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097947"
---
# <a name="d3dxvec2transform-function-d3dx9mathh"></a><span data-ttu-id="d51ec-103">D3DXVec2Transform, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="d51ec-103">D3DXVec2Transform function (D3dx9math.h)</span></span>

<span data-ttu-id="d51ec-104">Transforme un vecteur 2D par une matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="d51ec-104">Transforms a 2D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d51ec-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d51ec-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec2Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="d51ec-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d51ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d51ec-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d51ec-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d51ec-108">Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="d51ec-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="d51ec-109">Pointeur vers la structure [**D3DXVECTOR4**](d3dxvector4.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="d51ec-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d51ec-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d51ec-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d51ec-111">Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="d51ec-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="d51ec-112">Pointeur vers la structure [**D3DXVECTOR2**](d3dxvector2.md) source.</span><span class="sxs-lookup"><span data-stu-id="d51ec-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d51ec-113">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d51ec-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d51ec-114">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d51ec-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d51ec-115">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="d51ec-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d51ec-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d51ec-116">Return value</span></span>

<span data-ttu-id="d51ec-117">Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="d51ec-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="d51ec-118">Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) qui est le vecteur transformé.</span><span class="sxs-lookup"><span data-stu-id="d51ec-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="d51ec-119">Notes </span><span class="sxs-lookup"><span data-stu-id="d51ec-119">Remarks</span></span>

<span data-ttu-id="d51ec-120">Cette fonction transforme le vecteur *PV* (x, y, 0, 1) par la matrice *PM*.</span><span class="sxs-lookup"><span data-stu-id="d51ec-120">This function transforms the vector *pV* (x, y, 0, 1) by the matrix *pM*.</span></span>

<span data-ttu-id="d51ec-121">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="d51ec-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="d51ec-122">De cette façon, la fonction **D3DXVec2Transform** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="d51ec-122">In this way, the **D3DXVec2Transform** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d51ec-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d51ec-123">Requirements</span></span>



| <span data-ttu-id="d51ec-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d51ec-124">Requirement</span></span> | <span data-ttu-id="d51ec-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="d51ec-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d51ec-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="d51ec-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d51ec-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d51ec-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d51ec-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d51ec-128">Library</span></span><br/> | <dl> <span data-ttu-id="d51ec-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d51ec-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d51ec-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d51ec-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d51ec-131">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="d51ec-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="d51ec-132">**D3DXVec2TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="d51ec-132">**D3DXVec2TransformCoord**</span></span>](d3dxvec2transformcoord.md)
</dt> <dt>

[<span data-ttu-id="d51ec-133">**D3DXVec2TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="d51ec-133">**D3DXVec2TransformNormal**</span></span>](d3dxvec2transformnormal.md)
</dt> </dl>

 

 




