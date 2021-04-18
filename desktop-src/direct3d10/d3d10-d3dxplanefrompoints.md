---
description: Construit un plan à partir de trois points.
ms.assetid: 0e77af1b-cedf-482c-8398-10becb398a2c
title: D3DXPlaneFromPoints, fonction (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eed4426492f05b2bfe3c762915edb8fdc21dc789
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525907"
---
# <a name="d3dxplanefrompoints-function-d3dx10mathh"></a><span data-ttu-id="76e45-103">D3DXPlaneFromPoints, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="76e45-103">D3DXPlaneFromPoints function (D3DX10Math.h)</span></span>

<span data-ttu-id="76e45-104">Construit un plan à partir de trois points.</span><span class="sxs-lookup"><span data-stu-id="76e45-104">Constructs a plane from three points.</span></span>

## <a name="syntax"></a><span data-ttu-id="76e45-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76e45-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPoints(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="76e45-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="76e45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76e45-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="76e45-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="76e45-108">Type : **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="76e45-108">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="76e45-109">Pointeur vers le [**D3DXPLANE**](d3d10-d3dxplane.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="76e45-109">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="76e45-110">*pV1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="76e45-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76e45-111">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="76e45-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="76e45-112">Pointeur vers un [**D3DXVECTOR3**](d3d10-d3dxvector3.md), définissant l’un des points utilisés pour construire le plan.</span><span class="sxs-lookup"><span data-stu-id="76e45-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="76e45-113">*pV2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="76e45-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76e45-114">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="76e45-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="76e45-115">Pointeur vers une structure D3DXVECTOR3, définissant l’un des points utilisés pour construire le plan.</span><span class="sxs-lookup"><span data-stu-id="76e45-115">Pointer to a D3DXVECTOR3 structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="76e45-116">*pV3* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="76e45-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76e45-117">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="76e45-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="76e45-118">Pointeur vers une structure D3DXVECTOR3, définissant l’un des points utilisés pour construire le plan.</span><span class="sxs-lookup"><span data-stu-id="76e45-118">Pointer to a D3DXVECTOR3 structure, defining one of the points used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76e45-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="76e45-119">Return value</span></span>

<span data-ttu-id="76e45-120">Type : **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="76e45-120">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="76e45-121">Pointeur vers la structure D3DXPLANE construite à partir des points donnés.</span><span class="sxs-lookup"><span data-stu-id="76e45-121">Pointer to the D3DXPLANE structure constructed from the given points.</span></span>

## <a name="remarks"></a><span data-ttu-id="76e45-122">Notes</span><span class="sxs-lookup"><span data-stu-id="76e45-122">Remarks</span></span>

<span data-ttu-id="76e45-123">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="76e45-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="76e45-124">De cette façon, la fonction D3DXPlaneFromPoints peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="76e45-124">In this way, the D3DXPlaneFromPoints function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="76e45-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76e45-125">Requirements</span></span>



| <span data-ttu-id="76e45-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76e45-126">Requirement</span></span> | <span data-ttu-id="76e45-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="76e45-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76e45-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="76e45-128">Header</span></span><br/>  | <dl> <span data-ttu-id="76e45-129"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="76e45-129"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="76e45-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="76e45-130">Library</span></span><br/> | <dl> <span data-ttu-id="76e45-131"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76e45-131"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="76e45-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76e45-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76e45-133">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="76e45-133">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
