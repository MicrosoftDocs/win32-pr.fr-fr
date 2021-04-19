---
description: Calcule le produit scalaire d’un plan et d’un vecteur 4D.
ms.assetid: e6232ca8-52cc-472d-8bdb-4f8dfc520d4f
title: D3DXPlaneDot, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b6f33e591df364151a7090e5b4a9dd0773f5788a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532182"
---
# <a name="d3dxplanedot-function"></a><span data-ttu-id="e3b40-103">D3DXPlaneDot fonction)</span><span class="sxs-lookup"><span data-stu-id="e3b40-103">D3DXPlaneDot function</span></span>

<span data-ttu-id="e3b40-104">Calcule le produit scalaire d’un plan et d’un vecteur 4D.</span><span class="sxs-lookup"><span data-stu-id="e3b40-104">Computes the dot product of a plane and a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3b40-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3b40-105">Syntax</span></span>


```C++
FLOAT D3DXPlaneDot(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="e3b40-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3b40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3b40-107">*pp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e3b40-107">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b40-108">Type : **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="e3b40-108">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="e3b40-109">Pointeur vers une structure [**D3DXPLANE**](d3dxplane.md) source.</span><span class="sxs-lookup"><span data-stu-id="e3b40-109">Pointer to a source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e3b40-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e3b40-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b40-111">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="e3b40-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="e3b40-112">Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="e3b40-112">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3b40-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e3b40-113">Return value</span></span>

<span data-ttu-id="e3b40-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3b40-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3b40-115">Produit scalaire des vecteurs de plan et 4D.</span><span class="sxs-lookup"><span data-stu-id="e3b40-115">The dot product of the plane and 4D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3b40-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e3b40-116">Remarks</span></span>

<span data-ttu-id="e3b40-117">Avec un plan (a, b, c, d) et un vecteur 4D (x, y, z, w), la valeur de retour de cette fonction est un \* x + b \* y + c \* z + d \* w.</span><span class="sxs-lookup"><span data-stu-id="e3b40-117">Given a plane (a, b, c, d) and a 4D vector (x, y, z, w) the return value of this function is a\*x + b\*y + c\*z + d\*w.</span></span> <span data-ttu-id="e3b40-118">La fonction **D3DXPlaneDot** est utile pour déterminer la relation du plan avec une coordonnée homogène.</span><span class="sxs-lookup"><span data-stu-id="e3b40-118">The **D3DXPlaneDot** function is useful for determining the plane's relationship with a homogeneous coordinate.</span></span> <span data-ttu-id="e3b40-119">Par exemple, cette fonction peut être utilisée pour déterminer si une coordonnée particulière est sur un plan particulier, ou sur le côté d’un plan particulier qui se trouve une coordonnée particulière.</span><span class="sxs-lookup"><span data-stu-id="e3b40-119">For example, this function could be used to determine if a particular coordinate is on a particular plane, or on which side of a particular plane a particular coordinate lies.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3b40-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3b40-120">Requirements</span></span>



| <span data-ttu-id="e3b40-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3b40-121">Requirement</span></span> | <span data-ttu-id="e3b40-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3b40-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3b40-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e3b40-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e3b40-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3b40-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e3b40-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e3b40-125">Library</span></span><br/> | <dl> <span data-ttu-id="e3b40-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3b40-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e3b40-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3b40-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3b40-128">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="e3b40-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e3b40-129">**D3DXPlaneDotCoord**</span><span class="sxs-lookup"><span data-stu-id="e3b40-129">**D3DXPlaneDotCoord**</span></span>](d3dxplanedotcoord.md)
</dt> <dt>

[<span data-ttu-id="e3b40-130">**D3DXPlaneDotNormal**</span><span class="sxs-lookup"><span data-stu-id="e3b40-130">**D3DXPlaneDotNormal**</span></span>](d3dxplanedotnormal.md)
</dt> </dl>

 

 
