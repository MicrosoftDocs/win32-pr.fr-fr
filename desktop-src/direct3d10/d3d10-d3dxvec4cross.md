---
description: 'Fonction D3DXVec4Cross (D3DX10Math. h) : détermine le produit croisé en quatre dimensions.'
ms.assetid: 4f728fbd-cf5a-4d2e-ba4f-487616d83f6d
title: D3DXVec4Cross, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Cross
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: e52cc1adb1e48f65599b1bf7179f7953823f1e1c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102947"
---
# <a name="d3dxvec4cross-function-d3dx10mathh"></a><span data-ttu-id="cc36e-103">D3DXVec4Cross, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="cc36e-103">D3DXVec4Cross function (D3DX10Math.h)</span></span>

<span data-ttu-id="cc36e-104">Détermine le produit croisé en quatre dimensions.</span><span class="sxs-lookup"><span data-stu-id="cc36e-104">Determines the cross-product in four dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc36e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc36e-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Cross(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="cc36e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc36e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc36e-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cc36e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc36e-108">Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="cc36e-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="cc36e-109">Pointeur vers le [**D3DXVECTOR4**](d3d10-d3dxvector4.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="cc36e-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="cc36e-110">*pV1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc36e-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc36e-111">Type : **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="cc36e-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="cc36e-112">Pointeur vers une structure D3DXVECTOR4 source.</span><span class="sxs-lookup"><span data-stu-id="cc36e-112">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="cc36e-113">*pV2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc36e-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc36e-114">Type : **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="cc36e-114">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="cc36e-115">Pointeur vers une structure D3DXVECTOR4 source.</span><span class="sxs-lookup"><span data-stu-id="cc36e-115">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="cc36e-116">*pV3* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc36e-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc36e-117">Type : **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="cc36e-117">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="cc36e-118">Pointeur vers une structure D3DXVECTOR4 source.</span><span class="sxs-lookup"><span data-stu-id="cc36e-118">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc36e-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cc36e-119">Return value</span></span>

<span data-ttu-id="cc36e-120">Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="cc36e-120">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="cc36e-121">Pointeur vers une structure D3DXVECTOR4 qui est le produit croisé.</span><span class="sxs-lookup"><span data-stu-id="cc36e-121">Pointer to a D3DXVECTOR4 structure that is the cross product.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc36e-122">Notes </span><span class="sxs-lookup"><span data-stu-id="cc36e-122">Remarks</span></span>

<span data-ttu-id="cc36e-123">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="cc36e-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="cc36e-124">De cette façon, la fonction D3DXVec4Cross peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="cc36e-124">In this way, the D3DXVec4Cross function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc36e-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc36e-125">Requirements</span></span>



| <span data-ttu-id="cc36e-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc36e-126">Requirement</span></span> | <span data-ttu-id="cc36e-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc36e-127">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc36e-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc36e-128">Header</span></span><br/> | <dl> <span data-ttu-id="cc36e-129"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc36e-129"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc36e-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc36e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc36e-131">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="cc36e-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
