---
description: D3DXVec4Transform, fonction (D3DX10Math. h)-transforme un vecteur 4D par une matrice donnée.
ms.assetid: ccbf33bc-1f94-4cf8-b048-220d54516e00
title: D3DXVec4Transform, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Transform
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 737e1901a514a3940790ce83c7e9bc1f6f471371
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102917"
---
# <a name="d3dxvec4transform-function-d3dx10mathh"></a><span data-ttu-id="55700-103">D3DXVec4Transform, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="55700-103">D3DXVec4Transform function (D3DX10Math.h)</span></span>

<span data-ttu-id="55700-104">Transforme un vecteur 4D par une matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="55700-104">Transforms a 4D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="55700-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55700-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="55700-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55700-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55700-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="55700-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="55700-108">Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="55700-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="55700-109">Pointeur vers le [**D3DXVECTOR4**](d3d10-d3dxvector4.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="55700-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="55700-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="55700-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55700-111">Type : **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="55700-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="55700-112">Pointeur vers la structure D3DXVECTOR4 source.</span><span class="sxs-lookup"><span data-stu-id="55700-112">Pointer to the source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="55700-113">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="55700-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55700-114">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="55700-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="55700-115">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="55700-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55700-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="55700-116">Return value</span></span>

<span data-ttu-id="55700-117">Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="55700-117">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="55700-118">Pointeur vers une structure D3DXVECTOR4 qui est le vecteur 4D transformé.</span><span class="sxs-lookup"><span data-stu-id="55700-118">Pointer to a D3DXVECTOR4 structure that is the transformed 4D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="55700-119">Notes </span><span class="sxs-lookup"><span data-stu-id="55700-119">Remarks</span></span>

<span data-ttu-id="55700-120">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="55700-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="55700-121">De cette façon, la fonction D3DXVec4Transform peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="55700-121">In this way, the D3DXVec4Transform function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="55700-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55700-122">Requirements</span></span>



| <span data-ttu-id="55700-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55700-123">Requirement</span></span> | <span data-ttu-id="55700-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="55700-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55700-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="55700-125">Header</span></span><br/> | <dl> <span data-ttu-id="55700-126"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="55700-126"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55700-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55700-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55700-128">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="55700-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
