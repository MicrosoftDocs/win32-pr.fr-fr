---
description: 'D3DXPlaneFromPointNormal, fonction (D3DX10Math. h) : construit un plan à partir d’un point et d’un normal.'
ms.assetid: 93c644d2-ab8c-47a1-9a3b-8b9c6a13178b
title: D3DXPlaneFromPointNormal, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPointNormal
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 519ce82a8d5a8c6adaf22b69047a8d365bd777ac
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108837"
---
# <a name="d3dxplanefrompointnormal-function-d3dx10mathh"></a><span data-ttu-id="8a20e-103">D3DXPlaneFromPointNormal, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="8a20e-103">D3DXPlaneFromPointNormal function (D3DX10Math.h)</span></span>

<span data-ttu-id="8a20e-104">Construit un plan à partir d’un point et d’un normal.</span><span class="sxs-lookup"><span data-stu-id="8a20e-104">Constructs a plane from a point and a normal.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a20e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a20e-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a><span data-ttu-id="8a20e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a20e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a20e-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8a20e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a20e-108">Type : **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="8a20e-108">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="8a20e-109">Pointeur vers le [**D3DXPLANE**](d3d10-d3dxplane.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="8a20e-109">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8a20e-110">*PPoint* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a20e-110">*pPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a20e-111">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8a20e-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="8a20e-112">Pointeur vers un [**D3DXVECTOR3**](d3d10-d3dxvector3.md), définissant le point utilisé pour construire le plan.</span><span class="sxs-lookup"><span data-stu-id="8a20e-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), defining the point used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="8a20e-113">*pNormal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a20e-113">*pNormal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a20e-114">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8a20e-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="8a20e-115">Pointeur vers une structure D3DXVECTOR3, définissant le normal utilisé pour construire le plan.</span><span class="sxs-lookup"><span data-stu-id="8a20e-115">Pointer to a D3DXVECTOR3 structure, defining the normal used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a20e-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8a20e-116">Return value</span></span>

<span data-ttu-id="8a20e-117">Type : **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="8a20e-117">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="8a20e-118">Pointeur vers la structure D3DXPLANE construite à partir du point et du normal.</span><span class="sxs-lookup"><span data-stu-id="8a20e-118">Pointer to the D3DXPLANE structure constructed from the point and the normal.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a20e-119">Notes </span><span class="sxs-lookup"><span data-stu-id="8a20e-119">Remarks</span></span>

<span data-ttu-id="8a20e-120">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="8a20e-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="8a20e-121">De cette façon, la fonction D3DXPlaneFromPointNormal peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="8a20e-121">In this way, the D3DXPlaneFromPointNormal function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a20e-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a20e-122">Requirements</span></span>



| <span data-ttu-id="8a20e-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a20e-123">Requirement</span></span> | <span data-ttu-id="8a20e-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a20e-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a20e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="8a20e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8a20e-126"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a20e-126"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="8a20e-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8a20e-127">Library</span></span><br/> | <dl> <span data-ttu-id="8a20e-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a20e-128"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8a20e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a20e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a20e-130">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="8a20e-130">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
