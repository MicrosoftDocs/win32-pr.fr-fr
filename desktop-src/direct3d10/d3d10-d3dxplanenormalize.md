---
description: Normalise les coefficients de plan afin que la normale du plan ait une longueur d’unité.
ms.assetid: 52ae36a7-e37b-457a-9832-e62900a85bde
title: D3DXPlaneNormalize, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneNormalize
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 44d5e9d810653b2cdae233dec803383c74563d08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535201"
---
# <a name="d3dxplanenormalize-function-d3dx10mathh"></a><span data-ttu-id="cd0c7-103">D3DXPlaneNormalize, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="cd0c7-103">D3DXPlaneNormalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="cd0c7-104">Normalise les coefficients de plan afin que la normale du plan ait une longueur d’unité.</span><span class="sxs-lookup"><span data-stu-id="cd0c7-104">Normalizes the plane coefficients so that the plane normal has unit length.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd0c7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd0c7-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a><span data-ttu-id="cd0c7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd0c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd0c7-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cd0c7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd0c7-108">Type : **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="cd0c7-108">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="cd0c7-109">Pointeur vers le [**D3DXPLANE**](d3d10-d3dxplane.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="cd0c7-109">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="cd0c7-110">*pp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd0c7-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd0c7-111">Type : **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="cd0c7-111">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="cd0c7-112">Pointeur vers la structure D3DXPLANE source.</span><span class="sxs-lookup"><span data-stu-id="cd0c7-112">Pointer to the source D3DXPLANE structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd0c7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cd0c7-113">Return value</span></span>

<span data-ttu-id="cd0c7-114">Type : **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="cd0c7-114">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="cd0c7-115">Pointeur vers une structure D3DXPLANE qui représente la normale du plan.</span><span class="sxs-lookup"><span data-stu-id="cd0c7-115">Pointer to a D3DXPLANE structure that represents the normal of the plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd0c7-116">Notes</span><span class="sxs-lookup"><span data-stu-id="cd0c7-116">Remarks</span></span>

<span data-ttu-id="cd0c7-117">Cette fonction normalise un plan afin que \| a, b, c \| = = 1.</span><span class="sxs-lookup"><span data-stu-id="cd0c7-117">This function normalizes a plane so that \|a,b,c\| == 1.</span></span>

<span data-ttu-id="cd0c7-118">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="cd0c7-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="cd0c7-119">De cette façon, cette fonction peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="cd0c7-119">In this way, this function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd0c7-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd0c7-120">Requirements</span></span>



| <span data-ttu-id="cd0c7-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd0c7-121">Requirement</span></span> | <span data-ttu-id="cd0c7-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd0c7-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd0c7-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="cd0c7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="cd0c7-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd0c7-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="cd0c7-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cd0c7-125">Library</span></span><br/> | <dl> <span data-ttu-id="cd0c7-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd0c7-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cd0c7-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd0c7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd0c7-128">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="cd0c7-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
