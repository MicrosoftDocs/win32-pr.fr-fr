---
description: Fait pivoter un Quaternion à propos d’un axe arbitraire.
ms.assetid: 9673ef89-458f-4a25-960e-8f03179e78ba
title: D3DXQuaternionRotationAxis, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationAxis
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 739f128ca1a56eed15ebc2528036875eaf2bb9b8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522612"
---
# <a name="d3dxquaternionrotationaxis-function-d3dx10mathh"></a><span data-ttu-id="ebb9b-103">D3DXQuaternionRotationAxis, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="ebb9b-103">D3DXQuaternionRotationAxis function (D3DX10Math.h)</span></span>

<span data-ttu-id="ebb9b-104">Fait pivoter un Quaternion à propos d’un axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="ebb9b-104">Rotates a quaternion about an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebb9b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebb9b-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationAxis(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_          FLOAT          Angle
);
```



## <a name="parameters"></a><span data-ttu-id="ebb9b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebb9b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebb9b-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ebb9b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebb9b-108">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="ebb9b-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ebb9b-109">Pointeur vers le [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="ebb9b-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ebb9b-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ebb9b-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebb9b-111">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ebb9b-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ebb9b-112">Pointeur vers le [**D3DXVECTOR3**](d3d10-d3dxvector3.md) qui identifie l’axe sur lequel pivoter le Quaternion.</span><span class="sxs-lookup"><span data-stu-id="ebb9b-112">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that identifies the axis about which to rotate the quaternion.</span></span>

</dd> <dt>

<span data-ttu-id="ebb9b-113">*Angle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ebb9b-113">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebb9b-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ebb9b-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ebb9b-115">Angle de rotation, en radians.</span><span class="sxs-lookup"><span data-stu-id="ebb9b-115">Angle of rotation, in radians.</span></span> <span data-ttu-id="ebb9b-116">Les angles sont mesurés dans le sens des aiguilles d’une montre sur l’axe de rotation vers l’origine.</span><span class="sxs-lookup"><span data-stu-id="ebb9b-116">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebb9b-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ebb9b-117">Return value</span></span>

<span data-ttu-id="ebb9b-118">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="ebb9b-118">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ebb9b-119">Pointeur vers une structure D3DXQUATERNION pivotée autour de l’axe spécifié.</span><span class="sxs-lookup"><span data-stu-id="ebb9b-119">Pointer to a D3DXQUATERNION structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebb9b-120">Notes</span><span class="sxs-lookup"><span data-stu-id="ebb9b-120">Remarks</span></span>

<span data-ttu-id="ebb9b-121">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="ebb9b-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="ebb9b-122">De cette façon, la fonction D3DXQuaternionRotationAxis peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="ebb9b-122">In this way, the D3DXQuaternionRotationAxis function can be used as a parameter for another function.</span></span>

<span data-ttu-id="ebb9b-123">Utilisez [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="ebb9b-123">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebb9b-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebb9b-124">Requirements</span></span>



| <span data-ttu-id="ebb9b-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebb9b-125">Requirement</span></span> | <span data-ttu-id="ebb9b-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebb9b-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebb9b-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="ebb9b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ebb9b-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebb9b-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="ebb9b-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ebb9b-129">Library</span></span><br/> | <dl> <span data-ttu-id="ebb9b-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ebb9b-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ebb9b-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebb9b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebb9b-132">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="ebb9b-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
