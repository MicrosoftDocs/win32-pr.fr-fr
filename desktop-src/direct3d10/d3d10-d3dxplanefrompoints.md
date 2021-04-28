---
description: 'D3DXPlaneFromPoints, fonction (D3DX10Math. h) : construit un plan à partir de trois points.'
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
ms.openlocfilehash: a3af01df7d1ce66029994226d040544b733a75df
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103317"
---
# <a name="d3dxplanefrompoints-function-d3dx10mathh"></a><span data-ttu-id="6761e-103">D3DXPlaneFromPoints, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="6761e-103">D3DXPlaneFromPoints function (D3DX10Math.h)</span></span>

<span data-ttu-id="6761e-104">Construit un plan à partir de trois points.</span><span class="sxs-lookup"><span data-stu-id="6761e-104">Constructs a plane from three points.</span></span>

## <a name="syntax"></a><span data-ttu-id="6761e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6761e-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPoints(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="6761e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6761e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6761e-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6761e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6761e-108">Type : **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="6761e-108">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="6761e-109">Pointeur vers le [**D3DXPLANE**](d3d10-d3dxplane.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="6761e-109">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6761e-110">*pV1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6761e-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6761e-111">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6761e-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="6761e-112">Pointeur vers un [**D3DXVECTOR3**](d3d10-d3dxvector3.md), définissant l’un des points utilisés pour construire le plan.</span><span class="sxs-lookup"><span data-stu-id="6761e-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="6761e-113">*pV2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6761e-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6761e-114">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6761e-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="6761e-115">Pointeur vers une structure D3DXVECTOR3, définissant l’un des points utilisés pour construire le plan.</span><span class="sxs-lookup"><span data-stu-id="6761e-115">Pointer to a D3DXVECTOR3 structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="6761e-116">*pV3* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6761e-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6761e-117">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6761e-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="6761e-118">Pointeur vers une structure D3DXVECTOR3, définissant l’un des points utilisés pour construire le plan.</span><span class="sxs-lookup"><span data-stu-id="6761e-118">Pointer to a D3DXVECTOR3 structure, defining one of the points used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6761e-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6761e-119">Return value</span></span>

<span data-ttu-id="6761e-120">Type : **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="6761e-120">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="6761e-121">Pointeur vers la structure D3DXPLANE construite à partir des points donnés.</span><span class="sxs-lookup"><span data-stu-id="6761e-121">Pointer to the D3DXPLANE structure constructed from the given points.</span></span>

## <a name="remarks"></a><span data-ttu-id="6761e-122">Notes </span><span class="sxs-lookup"><span data-stu-id="6761e-122">Remarks</span></span>

<span data-ttu-id="6761e-123">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="6761e-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="6761e-124">De cette façon, la fonction D3DXPlaneFromPoints peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="6761e-124">In this way, the D3DXPlaneFromPoints function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6761e-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6761e-125">Requirements</span></span>



| <span data-ttu-id="6761e-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6761e-126">Requirement</span></span> | <span data-ttu-id="6761e-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="6761e-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6761e-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="6761e-128">Header</span></span><br/>  | <dl> <span data-ttu-id="6761e-129"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6761e-129"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="6761e-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6761e-130">Library</span></span><br/> | <dl> <span data-ttu-id="6761e-131"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6761e-131"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6761e-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6761e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6761e-133">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="6761e-133">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
