---
description: Détermine le produit croisé en quatre dimensions.
ms.assetid: 10b965c9-7ed7-450c-86a0-114f068c888f
title: D3DXVec4Cross, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Cross
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 91e6e5662bff503ba96d96f135f98e60cf15c8fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211800"
---
# <a name="d3dxvec4cross-function-d3dx9mathh"></a><span data-ttu-id="0c98f-103">D3DXVec4Cross, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="0c98f-103">D3DXVec4Cross function (D3dx9math.h)</span></span>

<span data-ttu-id="0c98f-104">Détermine le produit croisé en quatre dimensions.</span><span class="sxs-lookup"><span data-stu-id="0c98f-104">Determines the cross-product in four dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c98f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c98f-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Cross(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="0c98f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c98f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c98f-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0c98f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c98f-108">Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="0c98f-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="0c98f-109">Pointeur vers la structure [**D3DXVECTOR4**](d3dxvector4.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="0c98f-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0c98f-110">*pV1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0c98f-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c98f-111">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="0c98f-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="0c98f-112">Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) source.</span><span class="sxs-lookup"><span data-stu-id="0c98f-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0c98f-113">*pV2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0c98f-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c98f-114">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="0c98f-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="0c98f-115">Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) source.</span><span class="sxs-lookup"><span data-stu-id="0c98f-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0c98f-116">*pV3* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0c98f-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c98f-117">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="0c98f-117">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="0c98f-118">Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) source.</span><span class="sxs-lookup"><span data-stu-id="0c98f-118">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c98f-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0c98f-119">Return value</span></span>

<span data-ttu-id="0c98f-120">Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="0c98f-120">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="0c98f-121">Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) qui est le produit croisé.</span><span class="sxs-lookup"><span data-stu-id="0c98f-121">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the cross product.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c98f-122">Notes</span><span class="sxs-lookup"><span data-stu-id="0c98f-122">Remarks</span></span>

<span data-ttu-id="0c98f-123">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="0c98f-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="0c98f-124">De cette façon, la fonction **D3DXVec4Cross** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="0c98f-124">In this way, the **D3DXVec4Cross** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c98f-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c98f-125">Requirements</span></span>



| <span data-ttu-id="0c98f-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c98f-126">Requirement</span></span> | <span data-ttu-id="0c98f-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c98f-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c98f-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="0c98f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="0c98f-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c98f-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0c98f-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0c98f-130">Library</span></span><br/> | <dl> <span data-ttu-id="0c98f-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c98f-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0c98f-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c98f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c98f-133">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="0c98f-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="0c98f-134">**D3DXVec4Dot**</span><span class="sxs-lookup"><span data-stu-id="0c98f-134">**D3DXVec4Dot**</span></span>](d3dxvec4dot.md)
</dt> </dl>

 

 




