---
description: Effectue une interpolation entre deux quaternions, en utilisant une interpolation linéaire sphérique.
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
ms.openlocfilehash: 07f673d33b8f105e808fbae380a06942e2a69be4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043140"
---
# <a name="d3dxquaternionslerp-function-d3dx10mathh"></a><span data-ttu-id="1583c-103">D3DXQuaternionSlerp, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="1583c-103">D3DXQuaternionSlerp function (D3DX10Math.h)</span></span>

<span data-ttu-id="1583c-104">Effectue une interpolation entre deux quaternions, en utilisant une interpolation linéaire sphérique.</span><span class="sxs-lookup"><span data-stu-id="1583c-104">Interpolates between two quaternions, using spherical linear interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1583c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1583c-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSlerp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="1583c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1583c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1583c-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1583c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1583c-108">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="1583c-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1583c-109">Pointeur vers le [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="1583c-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1583c-110">*pQ1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1583c-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1583c-111">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="1583c-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1583c-112">Pointeur vers une structure D3DXQUATERNION source.</span><span class="sxs-lookup"><span data-stu-id="1583c-112">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="1583c-113">*pQ2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1583c-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1583c-114">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="1583c-114">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1583c-115">Pointeur vers une structure D3DXQUATERNION source.</span><span class="sxs-lookup"><span data-stu-id="1583c-115">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="1583c-116">*t* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1583c-116">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1583c-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1583c-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1583c-118">Paramètre qui indique la distance à interpoler entre les quaternions.</span><span class="sxs-lookup"><span data-stu-id="1583c-118">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1583c-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1583c-119">Return value</span></span>

<span data-ttu-id="1583c-120">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="1583c-120">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1583c-121">Pointeur vers une structure D3DXQUATERNION qui est le résultat de l’interpolation.</span><span class="sxs-lookup"><span data-stu-id="1583c-121">Pointer to a D3DXQUATERNION structure that is the result of the interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="1583c-122">Notes</span><span class="sxs-lookup"><span data-stu-id="1583c-122">Remarks</span></span>

<span data-ttu-id="1583c-123">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="1583c-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1583c-124">De cette façon, la fonction D3DXQuaternionSlerp peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="1583c-124">In this way, the D3DXQuaternionSlerp function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1583c-125">Utilisez [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="1583c-125">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="1583c-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1583c-126">Requirements</span></span>



| <span data-ttu-id="1583c-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1583c-127">Requirement</span></span> | <span data-ttu-id="1583c-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="1583c-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1583c-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="1583c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="1583c-130"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1583c-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="1583c-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1583c-131">Library</span></span><br/> | <dl> <span data-ttu-id="1583c-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1583c-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1583c-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1583c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1583c-134">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="1583c-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
