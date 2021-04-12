---
description: Calcule le produit scalaire d’un plan et d’un vecteur 3D. Le paramètre w du vecteur est supposé être 1.
ms.assetid: 634de6bc-b631-493d-a7a6-292a3c3253d6
title: D3DXPlaneDotCoord, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDotCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 99ee9db7df541dcf74867b828a73ede80f11e22b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211682"
---
# <a name="d3dxplanedotcoord-function"></a><span data-ttu-id="d84c8-104">D3DXPlaneDotCoord fonction)</span><span class="sxs-lookup"><span data-stu-id="d84c8-104">D3DXPlaneDotCoord function</span></span>

<span data-ttu-id="d84c8-105">Calcule le produit scalaire d’un plan et d’un vecteur 3D.</span><span class="sxs-lookup"><span data-stu-id="d84c8-105">Computes the dot product of a plane and a 3D vector.</span></span> <span data-ttu-id="d84c8-106">Le paramètre w du vecteur est supposé être 1.</span><span class="sxs-lookup"><span data-stu-id="d84c8-106">The w parameter of the vector is assumed to be 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="d84c8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d84c8-107">Syntax</span></span>


```C++
FLOAT D3DXPlaneDotCoord(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="d84c8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d84c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d84c8-109">*pp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d84c8-109">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d84c8-110">Type : **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="d84c8-110">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="d84c8-111">Pointeur vers une structure [**D3DXPLANE**](d3dxplane.md) source.</span><span class="sxs-lookup"><span data-stu-id="d84c8-111">Pointer to a source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d84c8-112">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d84c8-112">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d84c8-113">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d84c8-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d84c8-114">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) source.</span><span class="sxs-lookup"><span data-stu-id="d84c8-114">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d84c8-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d84c8-115">Return value</span></span>

<span data-ttu-id="d84c8-116">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d84c8-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d84c8-117">Produit scalaire du plan et du vecteur 3D.</span><span class="sxs-lookup"><span data-stu-id="d84c8-117">The dot product of the plane and 3D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="d84c8-118">Notes</span><span class="sxs-lookup"><span data-stu-id="d84c8-118">Remarks</span></span>

<span data-ttu-id="d84c8-119">Avec un plan (a, b, c, d) et un vecteur 3D (x, y, z), la valeur de retour de cette fonction est un \* x + b \* y + c \* z + d \* 1.</span><span class="sxs-lookup"><span data-stu-id="d84c8-119">Given a plane (a, b, c, d) and a 3D vector (x, y, z) the return value of this function is a\*x + b\*y + c\*z + d\*1.</span></span> <span data-ttu-id="d84c8-120">La fonction **D3DXPlaneDotCoord** est utile pour déterminer la relation du plan avec une coordonnée dans l’espace 3D.</span><span class="sxs-lookup"><span data-stu-id="d84c8-120">The **D3DXPlaneDotCoord** function is useful for determining the plane's relationship with a coordinate in 3D space.</span></span>

## <a name="requirements"></a><span data-ttu-id="d84c8-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d84c8-121">Requirements</span></span>



| <span data-ttu-id="d84c8-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d84c8-122">Requirement</span></span> | <span data-ttu-id="d84c8-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="d84c8-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d84c8-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="d84c8-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d84c8-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d84c8-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d84c8-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d84c8-126">Library</span></span><br/> | <dl> <span data-ttu-id="d84c8-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d84c8-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d84c8-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d84c8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d84c8-129">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="d84c8-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="d84c8-130">**D3DXPlaneDot**</span><span class="sxs-lookup"><span data-stu-id="d84c8-130">**D3DXPlaneDot**</span></span>](d3dxplanedot.md)
</dt> <dt>

[<span data-ttu-id="d84c8-131">**D3DXPlaneDotNormal**</span><span class="sxs-lookup"><span data-stu-id="d84c8-131">**D3DXPlaneDotNormal**</span></span>](d3dxplanedotnormal.md)
</dt> </dl>

 

 
