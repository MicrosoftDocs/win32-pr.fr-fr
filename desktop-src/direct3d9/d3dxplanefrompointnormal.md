---
description: Construit un plan à partir d’un point et d’un normal.
ms.assetid: af396bbb-09b7-492f-a25f-9c950da7e605
title: D3DXPlaneFromPointNormal, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8eeb8ea3a1725e0bf615be888d8e862c97730a2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529587"
---
# <a name="d3dxplanefrompointnormal-function-d3dx9mathh"></a><span data-ttu-id="c60a7-103">D3DXPlaneFromPointNormal, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c60a7-103">D3DXPlaneFromPointNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="c60a7-104">Construit un plan à partir d’un point et d’un normal.</span><span class="sxs-lookup"><span data-stu-id="c60a7-104">Constructs a plane from a point and a normal.</span></span>

## <a name="syntax"></a><span data-ttu-id="c60a7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c60a7-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a><span data-ttu-id="c60a7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c60a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c60a7-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c60a7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c60a7-108">Type : **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="c60a7-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="c60a7-109">Pointeur vers la structure [**D3DXPLANE**](d3dxplane.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="c60a7-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c60a7-110">*PPoint* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c60a7-110">*pPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c60a7-111">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c60a7-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c60a7-112">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , définissant le point utilisé pour construire le plan.</span><span class="sxs-lookup"><span data-stu-id="c60a7-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining the point used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="c60a7-113">*pNormal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c60a7-113">*pNormal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c60a7-114">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c60a7-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c60a7-115">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , définissant le normal utilisé pour construire le plan.</span><span class="sxs-lookup"><span data-stu-id="c60a7-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining the normal used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c60a7-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c60a7-116">Return value</span></span>

<span data-ttu-id="c60a7-117">Type : **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="c60a7-117">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="c60a7-118">Pointeur vers la structure [**D3DXPLANE**](d3dxplane.md) construite à partir du point et du normal.</span><span class="sxs-lookup"><span data-stu-id="c60a7-118">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure constructed from the point and the normal.</span></span>

## <a name="remarks"></a><span data-ttu-id="c60a7-119">Notes</span><span class="sxs-lookup"><span data-stu-id="c60a7-119">Remarks</span></span>

<span data-ttu-id="c60a7-120">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="c60a7-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c60a7-121">De cette façon, la fonction **D3DXPlaneFromPointNormal** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="c60a7-121">In this way, the **D3DXPlaneFromPointNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c60a7-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c60a7-122">Requirements</span></span>



| <span data-ttu-id="c60a7-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c60a7-123">Requirement</span></span> | <span data-ttu-id="c60a7-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="c60a7-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c60a7-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="c60a7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c60a7-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c60a7-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c60a7-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c60a7-127">Library</span></span><br/> | <dl> <span data-ttu-id="c60a7-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c60a7-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c60a7-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c60a7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c60a7-130">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="c60a7-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c60a7-131">**D3DXPlaneFromPoints**</span><span class="sxs-lookup"><span data-stu-id="c60a7-131">**D3DXPlaneFromPoints**</span></span>](d3dxplanefrompoints.md)
</dt> </dl>

 

 




