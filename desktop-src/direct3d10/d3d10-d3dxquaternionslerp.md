---
description: 'Fonction D3DXQuaternionSlerp (D3DX10Math. h) : interpole entre deux quaternions, à l’aide d’une interpolation linéaire sphérique.'
ms.assetid: 487e1df1-bf20-49cb-ad14-61fcf1300904
title: D3DXQuaternionSlerp, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSlerp
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 04cd3d82e4ca4e3f3357ab0114b57602f7e8a543
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103117"
---
# <a name="d3dxquaternionslerp-function-d3dx10mathh"></a><span data-ttu-id="1f19f-103">D3DXQuaternionSlerp, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="1f19f-103">D3DXQuaternionSlerp function (D3DX10Math.h)</span></span>

<span data-ttu-id="1f19f-104">Effectue une interpolation entre deux quaternions, en utilisant une interpolation linéaire sphérique.</span><span class="sxs-lookup"><span data-stu-id="1f19f-104">Interpolates between two quaternions, using spherical linear interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f19f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f19f-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSlerp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="1f19f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f19f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f19f-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1f19f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f19f-108">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="1f19f-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1f19f-109">Pointeur vers le [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="1f19f-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1f19f-110">*pQ1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1f19f-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f19f-111">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="1f19f-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1f19f-112">Pointeur vers une structure D3DXQUATERNION source.</span><span class="sxs-lookup"><span data-stu-id="1f19f-112">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="1f19f-113">*pQ2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1f19f-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f19f-114">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="1f19f-114">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1f19f-115">Pointeur vers une structure D3DXQUATERNION source.</span><span class="sxs-lookup"><span data-stu-id="1f19f-115">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="1f19f-116">*t* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1f19f-116">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f19f-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f19f-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f19f-118">Paramètre qui indique la distance à interpoler entre les quaternions.</span><span class="sxs-lookup"><span data-stu-id="1f19f-118">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f19f-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1f19f-119">Return value</span></span>

<span data-ttu-id="1f19f-120">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="1f19f-120">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1f19f-121">Pointeur vers une structure D3DXQUATERNION qui est le résultat de l’interpolation.</span><span class="sxs-lookup"><span data-stu-id="1f19f-121">Pointer to a D3DXQUATERNION structure that is the result of the interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f19f-122">Notes </span><span class="sxs-lookup"><span data-stu-id="1f19f-122">Remarks</span></span>

<span data-ttu-id="1f19f-123">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="1f19f-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1f19f-124">De cette façon, la fonction D3DXQuaternionSlerp peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="1f19f-124">In this way, the D3DXQuaternionSlerp function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1f19f-125">Utilisez [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="1f19f-125">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f19f-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f19f-126">Requirements</span></span>



| <span data-ttu-id="1f19f-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f19f-127">Requirement</span></span> | <span data-ttu-id="1f19f-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f19f-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f19f-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="1f19f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="1f19f-130"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f19f-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="1f19f-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1f19f-131">Library</span></span><br/> | <dl> <span data-ttu-id="1f19f-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f19f-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1f19f-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f19f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f19f-134">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="1f19f-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
