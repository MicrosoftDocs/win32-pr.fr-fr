---
description: 'Fonction D3DXVec4Cross (D3dx9math. h) : détermine le produit croisé en quatre dimensions.'
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
ms.openlocfilehash: e3630a486f6c8fcd456373445bd931d878fdc38e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097687"
---
# <a name="d3dxvec4cross-function-d3dx9mathh"></a><span data-ttu-id="c7fa2-103">D3DXVec4Cross, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c7fa2-103">D3DXVec4Cross function (D3dx9math.h)</span></span>

<span data-ttu-id="c7fa2-104">Détermine le produit croisé en quatre dimensions.</span><span class="sxs-lookup"><span data-stu-id="c7fa2-104">Determines the cross-product in four dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7fa2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7fa2-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Cross(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="c7fa2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7fa2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7fa2-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c7fa2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7fa2-108">Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="c7fa2-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="c7fa2-109">Pointeur vers la structure [**D3DXVECTOR4**](d3dxvector4.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="c7fa2-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c7fa2-110">*pV1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c7fa2-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7fa2-111">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="c7fa2-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="c7fa2-112">Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) source.</span><span class="sxs-lookup"><span data-stu-id="c7fa2-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c7fa2-113">*pV2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c7fa2-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7fa2-114">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="c7fa2-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="c7fa2-115">Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) source.</span><span class="sxs-lookup"><span data-stu-id="c7fa2-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c7fa2-116">*pV3* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c7fa2-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7fa2-117">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="c7fa2-117">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="c7fa2-118">Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) source.</span><span class="sxs-lookup"><span data-stu-id="c7fa2-118">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7fa2-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c7fa2-119">Return value</span></span>

<span data-ttu-id="c7fa2-120">Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="c7fa2-120">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="c7fa2-121">Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) qui est le produit croisé.</span><span class="sxs-lookup"><span data-stu-id="c7fa2-121">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the cross product.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7fa2-122">Notes </span><span class="sxs-lookup"><span data-stu-id="c7fa2-122">Remarks</span></span>

<span data-ttu-id="c7fa2-123">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="c7fa2-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c7fa2-124">De cette façon, la fonction **D3DXVec4Cross** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="c7fa2-124">In this way, the **D3DXVec4Cross** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7fa2-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7fa2-125">Requirements</span></span>



| <span data-ttu-id="c7fa2-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7fa2-126">Requirement</span></span> | <span data-ttu-id="c7fa2-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7fa2-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7fa2-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="c7fa2-128">Header</span></span><br/>  | <dl> <span data-ttu-id="c7fa2-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7fa2-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c7fa2-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c7fa2-130">Library</span></span><br/> | <dl> <span data-ttu-id="c7fa2-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7fa2-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c7fa2-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7fa2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7fa2-133">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="c7fa2-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c7fa2-134">**D3DXVec4Dot**</span><span class="sxs-lookup"><span data-stu-id="c7fa2-134">**D3DXVec4Dot**</span></span>](d3dxvec4dot.md)
</dt> </dl>

 

 




