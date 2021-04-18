---
description: Effectue une interpolation linéaire entre deux vecteurs 2D.
ms.assetid: f8e9e6be-9696-4a4a-a6c8-c021985decaa
title: D3DXVec2Lerp, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Lerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b08b767993143db3057985140b97854b9203d2b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522945"
---
# <a name="d3dxvec2lerp-function"></a><span data-ttu-id="7c0ad-103">D3DXVec2Lerp fonction)</span><span class="sxs-lookup"><span data-stu-id="7c0ad-103">D3DXVec2Lerp function</span></span>

<span data-ttu-id="7c0ad-104">Effectue une interpolation linéaire entre deux vecteurs 2D.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-104">Performs a linear interpolation between two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c0ad-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c0ad-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Lerp(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="7c0ad-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c0ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c0ad-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7c0ad-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c0ad-108">Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="7c0ad-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="7c0ad-109">Pointeur vers la structure [**D3DXVECTOR2**](d3dxvector2.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7c0ad-110">*pV1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7c0ad-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c0ad-111">Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="7c0ad-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="7c0ad-112">Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) source.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7c0ad-113">*pV2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7c0ad-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c0ad-114">Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="7c0ad-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="7c0ad-115">Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) source.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7c0ad-116"> \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7c0ad-116">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c0ad-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c0ad-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c0ad-118">Paramètre qui interpole de manière linéaire entre les vecteurs.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-118">Parameter that linearly interpolates between the vectors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c0ad-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7c0ad-119">Return value</span></span>

<span data-ttu-id="7c0ad-120">Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="7c0ad-120">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="7c0ad-121">Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) qui est le résultat de l’interpolation linéaire.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-121">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the linear interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c0ad-122">Notes</span><span class="sxs-lookup"><span data-stu-id="7c0ad-122">Remarks</span></span>

<span data-ttu-id="7c0ad-123">Cette fonction effectue l’interpolation linéaire basée sur la formule suivante : v1 + s (V2-V1).</span><span class="sxs-lookup"><span data-stu-id="7c0ad-123">This function performs the linear interpolation based on the following formula: V1 + s(V2-V1).</span></span>

<span data-ttu-id="7c0ad-124">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="7c0ad-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="7c0ad-125">De cette façon, la fonction **D3DXVec2Lerp** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-125">In this way, the **D3DXVec2Lerp** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c0ad-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c0ad-126">Requirements</span></span>



| <span data-ttu-id="7c0ad-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c0ad-127">Requirement</span></span> | <span data-ttu-id="7c0ad-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c0ad-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c0ad-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c0ad-129">Header</span></span><br/>  | <dl> <span data-ttu-id="7c0ad-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c0ad-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7c0ad-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7c0ad-131">Library</span></span><br/> | <dl> <span data-ttu-id="7c0ad-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c0ad-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7c0ad-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c0ad-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c0ad-134">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="7c0ad-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
