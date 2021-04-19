---
description: Calcule le produit scalaire d’un plan et d’un vecteur 3D. Le paramètre w du vecteur est supposé être 0.
ms.assetid: 7aba1e94-6531-4c07-83b0-6100805e8bbd
title: D3DXPlaneDotNormal, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDotNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 28903fc8ce0073e4014ae6ce75df636222ce32f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529589"
---
# <a name="d3dxplanedotnormal-function"></a><span data-ttu-id="43fcd-104">D3DXPlaneDotNormal fonction)</span><span class="sxs-lookup"><span data-stu-id="43fcd-104">D3DXPlaneDotNormal function</span></span>

<span data-ttu-id="43fcd-105">Calcule le produit scalaire d’un plan et d’un vecteur 3D.</span><span class="sxs-lookup"><span data-stu-id="43fcd-105">Computes the dot product of a plane and a 3D vector.</span></span> <span data-ttu-id="43fcd-106">Le paramètre w du vecteur est supposé être 0.</span><span class="sxs-lookup"><span data-stu-id="43fcd-106">The w parameter of the vector is assumed to be 0.</span></span>

## <a name="syntax"></a><span data-ttu-id="43fcd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43fcd-107">Syntax</span></span>


```C++
FLOAT D3DXPlaneDotNormal(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="43fcd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43fcd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43fcd-109">*pp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="43fcd-109">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43fcd-110">Type : **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="43fcd-110">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="43fcd-111">Pointeur vers une structure [**D3DXPLANE**](d3dxplane.md) source.</span><span class="sxs-lookup"><span data-stu-id="43fcd-111">Pointer to a source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="43fcd-112">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="43fcd-112">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43fcd-113">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="43fcd-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="43fcd-114">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) source.</span><span class="sxs-lookup"><span data-stu-id="43fcd-114">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43fcd-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="43fcd-115">Return value</span></span>

<span data-ttu-id="43fcd-116">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43fcd-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43fcd-117">Produit scalaire du plan et du vecteur 3D.</span><span class="sxs-lookup"><span data-stu-id="43fcd-117">The dot product of the plane and 3D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="43fcd-118">Notes</span><span class="sxs-lookup"><span data-stu-id="43fcd-118">Remarks</span></span>

<span data-ttu-id="43fcd-119">Avec un plan (a, b, c, d) et un vecteur 3D (x, y, z), la valeur de retour de cette fonction est un \* x + b \* y + c \* z + d \* 0.</span><span class="sxs-lookup"><span data-stu-id="43fcd-119">Given a plane (a, b, c, d) and a 3D vector (x, y, z) the return value of this function is a\*x + b\*y + c\*z + d\*0.</span></span> <span data-ttu-id="43fcd-120">La fonction **D3DXPlaneDotNormal** est utile pour calculer l’angle entre la normale du plan et une autre normale.</span><span class="sxs-lookup"><span data-stu-id="43fcd-120">The **D3DXPlaneDotNormal** function is useful for calculating the angle between the normal of the plane, and another normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="43fcd-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43fcd-121">Requirements</span></span>



| <span data-ttu-id="43fcd-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43fcd-122">Requirement</span></span> | <span data-ttu-id="43fcd-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="43fcd-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="43fcd-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="43fcd-124">Header</span></span><br/>  | <dl> <span data-ttu-id="43fcd-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="43fcd-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="43fcd-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="43fcd-126">Library</span></span><br/> | <dl> <span data-ttu-id="43fcd-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43fcd-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="43fcd-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43fcd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43fcd-129">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="43fcd-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="43fcd-130">**D3DXPlaneDot**</span><span class="sxs-lookup"><span data-stu-id="43fcd-130">**D3DXPlaneDot**</span></span>](d3dxplanedot.md)
</dt> <dt>

[<span data-ttu-id="43fcd-131">**D3DXPlaneDotCoord**</span><span class="sxs-lookup"><span data-stu-id="43fcd-131">**D3DXPlaneDotCoord**</span></span>](d3dxplanedotcoord.md)
</dt> </dl>

 

 
