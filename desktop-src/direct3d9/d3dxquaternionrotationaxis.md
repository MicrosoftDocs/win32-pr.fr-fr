---
description: 'D3DXQuaternionRotationAxis, fonction (D3dx9math. h) : fait pivoter un Quaternion à propos d’un axe arbitraire.'
ms.assetid: 9ff0fe2c-54d6-482c-84e1-f38e3c57d8dd
title: D3DXQuaternionRotationAxis, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a5cbbdc3603b5e2eb7a03f592d44fa88f07ef015
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118017"
---
# <a name="d3dxquaternionrotationaxis-function-d3dx9mathh"></a><span data-ttu-id="30ce4-103">D3DXQuaternionRotationAxis, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="30ce4-103">D3DXQuaternionRotationAxis function (D3dx9math.h)</span></span>

<span data-ttu-id="30ce4-104">Fait pivoter un Quaternion à propos d’un axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="30ce4-104">Rotates a quaternion about an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="30ce4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30ce4-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationAxis(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_          FLOAT          Angle
);
```



## <a name="parameters"></a><span data-ttu-id="30ce4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30ce4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30ce4-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="30ce4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="30ce4-108">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="30ce4-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="30ce4-109">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="30ce4-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="30ce4-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30ce4-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30ce4-111">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="30ce4-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="30ce4-112">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) qui identifie l’axe sur lequel pivoter le Quaternion.</span><span class="sxs-lookup"><span data-stu-id="30ce4-112">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that identifies the axis about which to rotate the quaternion.</span></span>

</dd> <dt>

<span data-ttu-id="30ce4-113">*Angle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30ce4-113">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30ce4-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30ce4-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30ce4-115">Angle de rotation, en radians.</span><span class="sxs-lookup"><span data-stu-id="30ce4-115">Angle of rotation, in radians.</span></span> <span data-ttu-id="30ce4-116">Les angles sont mesurés dans le sens des aiguilles d’une montre sur l’axe de rotation vers l’origine.</span><span class="sxs-lookup"><span data-stu-id="30ce4-116">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30ce4-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="30ce4-117">Return value</span></span>

<span data-ttu-id="30ce4-118">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="30ce4-118">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="30ce4-119">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) pivotée autour de l’axe spécifié.</span><span class="sxs-lookup"><span data-stu-id="30ce4-119">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="30ce4-120">Notes </span><span class="sxs-lookup"><span data-stu-id="30ce4-120">Remarks</span></span>

<span data-ttu-id="30ce4-121">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="30ce4-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="30ce4-122">De cette façon, la fonction **D3DXQuaternionRotationAxis** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="30ce4-122">In this way, the **D3DXQuaternionRotationAxis** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="30ce4-123">Utilisez [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="30ce4-123">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="30ce4-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30ce4-124">Requirements</span></span>



| <span data-ttu-id="30ce4-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30ce4-125">Requirement</span></span> | <span data-ttu-id="30ce4-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="30ce4-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30ce4-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="30ce4-127">Header</span></span><br/>  | <dl> <span data-ttu-id="30ce4-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="30ce4-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="30ce4-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="30ce4-129">Library</span></span><br/> | <dl> <span data-ttu-id="30ce4-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30ce4-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="30ce4-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30ce4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30ce4-132">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="30ce4-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="30ce4-133">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="30ce4-133">**D3DXQuaternionRotationMatrix**</span></span>](d3dxquaternionrotationmatrix.md)
</dt> <dt>

[<span data-ttu-id="30ce4-134">**D3DXQuaternionRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="30ce4-134">**D3DXQuaternionRotationYawPitchRoll**</span></span>](d3dxquaternionrotationyawpitchroll.md)
</dt> </dl>

 

 
