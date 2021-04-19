---
description: Construit un plan à partir de trois points.
ms.assetid: 13d5ce6b-0046-441b-b826-f34f4fe16979
title: D3DXPlaneFromPoints, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPoints
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c537915c56cdbbfb33228b0c5a5ea3f2acc2baff
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529588"
---
# <a name="d3dxplanefrompoints-function-d3dx9mathh"></a><span data-ttu-id="a185f-103">D3DXPlaneFromPoints, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="a185f-103">D3DXPlaneFromPoints function (D3dx9math.h)</span></span>

<span data-ttu-id="a185f-104">Construit un plan à partir de trois points.</span><span class="sxs-lookup"><span data-stu-id="a185f-104">Constructs a plane from three points.</span></span>

## <a name="syntax"></a><span data-ttu-id="a185f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a185f-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPoints(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="a185f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a185f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a185f-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a185f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a185f-108">Type : **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="a185f-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="a185f-109">Pointeur vers la structure [**D3DXPLANE**](d3dxplane.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="a185f-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a185f-110">*pV1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a185f-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a185f-111">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a185f-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a185f-112">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , définissant l’un des points utilisés pour construire le plan.</span><span class="sxs-lookup"><span data-stu-id="a185f-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="a185f-113">*pV2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a185f-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a185f-114">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a185f-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a185f-115">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , définissant l’un des points utilisés pour construire le plan.</span><span class="sxs-lookup"><span data-stu-id="a185f-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="a185f-116">*pV3* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a185f-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a185f-117">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a185f-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a185f-118">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , définissant l’un des points utilisés pour construire le plan.</span><span class="sxs-lookup"><span data-stu-id="a185f-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a185f-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a185f-119">Return value</span></span>

<span data-ttu-id="a185f-120">Type : **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="a185f-120">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="a185f-121">Pointeur vers la structure [**D3DXPLANE**](d3dxplane.md) construite à partir des points donnés.</span><span class="sxs-lookup"><span data-stu-id="a185f-121">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure constructed from the given points.</span></span>

## <a name="remarks"></a><span data-ttu-id="a185f-122">Notes</span><span class="sxs-lookup"><span data-stu-id="a185f-122">Remarks</span></span>

<span data-ttu-id="a185f-123">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="a185f-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="a185f-124">De cette façon, la fonction **D3DXPlaneFromPoints** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="a185f-124">In this way, the **D3DXPlaneFromPoints** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a185f-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a185f-125">Requirements</span></span>



| <span data-ttu-id="a185f-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a185f-126">Requirement</span></span> | <span data-ttu-id="a185f-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="a185f-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a185f-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="a185f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="a185f-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a185f-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a185f-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a185f-130">Library</span></span><br/> | <dl> <span data-ttu-id="a185f-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a185f-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a185f-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a185f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a185f-133">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="a185f-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="a185f-134">**D3DXPlaneFromPointNormal**</span><span class="sxs-lookup"><span data-stu-id="a185f-134">**D3DXPlaneFromPointNormal**</span></span>](d3dxplanefrompointnormal.md)
</dt> </dl>

 

 




