---
description: Soustrait deux vecteurs 3D.
ms.assetid: 09e2cede-a0a3-4a5e-a7e1-e7a98cdc433b
title: D3DXVec3Subtract, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Subtract
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 17f41f2fd133db1064e2ba2778eacc139bab01ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211951"
---
# <a name="d3dxvec3subtract-function"></a><span data-ttu-id="874a5-103">D3DXVec3Subtract fonction)</span><span class="sxs-lookup"><span data-stu-id="874a5-103">D3DXVec3Subtract function</span></span>

<span data-ttu-id="874a5-104">Soustrait deux vecteurs 3D.</span><span class="sxs-lookup"><span data-stu-id="874a5-104">Subtracts two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="874a5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="874a5-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Subtract(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="874a5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="874a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="874a5-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="874a5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="874a5-108">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="874a5-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="874a5-109">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="874a5-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="874a5-110">*pV1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="874a5-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="874a5-111">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="874a5-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="874a5-112">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) source.</span><span class="sxs-lookup"><span data-stu-id="874a5-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="874a5-113">*pV2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="874a5-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="874a5-114">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="874a5-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="874a5-115">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) source.</span><span class="sxs-lookup"><span data-stu-id="874a5-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="874a5-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="874a5-116">Return value</span></span>

<span data-ttu-id="874a5-117">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="874a5-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="874a5-118">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) qui est la différence de deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="874a5-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the difference of two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="874a5-119">Notes</span><span class="sxs-lookup"><span data-stu-id="874a5-119">Remarks</span></span>

<span data-ttu-id="874a5-120">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="874a5-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="874a5-121">De cette façon, la fonction **D3DXVec3Subtract** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="874a5-121">In this way, the **D3DXVec3Subtract** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="874a5-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="874a5-122">Requirements</span></span>



| <span data-ttu-id="874a5-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="874a5-123">Requirement</span></span> | <span data-ttu-id="874a5-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="874a5-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="874a5-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="874a5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="874a5-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="874a5-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="874a5-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="874a5-127">Library</span></span><br/> | <dl> <span data-ttu-id="874a5-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="874a5-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="874a5-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="874a5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="874a5-130">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="874a5-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="874a5-131">**D3DXVec3Add**</span><span class="sxs-lookup"><span data-stu-id="874a5-131">**D3DXVec3Add**</span></span>](d3dxvec3add.md)
</dt> <dt>

[<span data-ttu-id="874a5-132">**D3DXVec3Scale**</span><span class="sxs-lookup"><span data-stu-id="874a5-132">**D3DXVec3Scale**</span></span>](d3dxvec3scale.md)
</dt> </dl>

 

 




