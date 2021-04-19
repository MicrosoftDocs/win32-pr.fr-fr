---
description: Met à l’échelle un vecteur 3D.
ms.assetid: b2483d6e-56e4-4557-a603-d59c0767774d
title: D3DXVec3Scale, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Scale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5357b862b9cf82e458429edea27001163eb9635
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532692"
---
# <a name="d3dxvec3scale-function"></a><span data-ttu-id="89ca8-103">D3DXVec3Scale fonction)</span><span class="sxs-lookup"><span data-stu-id="89ca8-103">D3DXVec3Scale function</span></span>

<span data-ttu-id="89ca8-104">Met à l’échelle un vecteur 3D.</span><span class="sxs-lookup"><span data-stu-id="89ca8-104">Scales a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="89ca8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89ca8-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Scale(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="89ca8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89ca8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89ca8-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="89ca8-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="89ca8-108">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="89ca8-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="89ca8-109">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="89ca8-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="89ca8-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="89ca8-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89ca8-111">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="89ca8-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="89ca8-112">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) source.</span><span class="sxs-lookup"><span data-stu-id="89ca8-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="89ca8-113"> \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="89ca8-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89ca8-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="89ca8-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="89ca8-115">Valeur de mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="89ca8-115">Scaling value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89ca8-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="89ca8-116">Return value</span></span>

<span data-ttu-id="89ca8-117">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="89ca8-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="89ca8-118">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) qui est le vecteur mis à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="89ca8-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the scaled vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="89ca8-119">Notes</span><span class="sxs-lookup"><span data-stu-id="89ca8-119">Remarks</span></span>

<span data-ttu-id="89ca8-120">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="89ca8-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="89ca8-121">De cette façon, la fonction **D3DXVec3Scale** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="89ca8-121">In this way, the **D3DXVec3Scale** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="89ca8-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89ca8-122">Requirements</span></span>



| <span data-ttu-id="89ca8-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89ca8-123">Requirement</span></span> | <span data-ttu-id="89ca8-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="89ca8-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="89ca8-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="89ca8-125">Header</span></span><br/>  | <dl> <span data-ttu-id="89ca8-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="89ca8-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="89ca8-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="89ca8-127">Library</span></span><br/> | <dl> <span data-ttu-id="89ca8-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="89ca8-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="89ca8-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89ca8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89ca8-130">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="89ca8-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="89ca8-131">**D3DXVec3Add**</span><span class="sxs-lookup"><span data-stu-id="89ca8-131">**D3DXVec3Add**</span></span>](d3dxvec3add.md)
</dt> <dt>

[<span data-ttu-id="89ca8-132">**D3DXVec3Subtract**</span><span class="sxs-lookup"><span data-stu-id="89ca8-132">**D3DXVec3Subtract**</span></span>](d3dxvec3subtract.md)
</dt> </dl>

 

 
