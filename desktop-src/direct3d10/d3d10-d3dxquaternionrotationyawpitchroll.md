---
description: 'D3DXQuaternionRotationYawPitchRoll, fonction (D3DX10Math. h) : génère un Quaternion avec le lacet, le tangage et le roulis donnés.'
ms.assetid: c929d9d4-b9cb-4de6-86c1-26fec3617846
title: D3DXQuaternionRotationYawPitchRoll, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationYawPitchRoll
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cefcf9a927cee0d8f7c83ff42ae6ca4fc699bb09
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108747"
---
# <a name="d3dxquaternionrotationyawpitchroll-function-d3dx10mathh"></a><span data-ttu-id="e5b36-103">D3DXQuaternionRotationYawPitchRoll, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="e5b36-103">D3DXQuaternionRotationYawPitchRoll function (D3DX10Math.h)</span></span>

<span data-ttu-id="e5b36-104">Génère un Quaternion avec le lacet, le tangage et le roulis donnés.</span><span class="sxs-lookup"><span data-stu-id="e5b36-104">Builds a quaternion with the given yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5b36-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5b36-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationYawPitchRoll(
  _Inout_ D3DXQUATERNION *pOut,
  _In_    FLOAT          Yaw,
  _In_    FLOAT          Pitch,
  _In_    FLOAT          Roll
);
```



## <a name="parameters"></a><span data-ttu-id="e5b36-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5b36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5b36-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e5b36-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5b36-108">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e5b36-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e5b36-109">Pointeur vers le [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="e5b36-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e5b36-110">*Lacet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5b36-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5b36-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5b36-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5b36-112">Lacet autour de l’axe y, en radians.</span><span class="sxs-lookup"><span data-stu-id="e5b36-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="e5b36-113">*Espacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5b36-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5b36-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5b36-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5b36-115">Hauteur autour de l’axe x, en radians.</span><span class="sxs-lookup"><span data-stu-id="e5b36-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="e5b36-116">*Roll* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5b36-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5b36-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5b36-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5b36-118">Tourner autour de l’axe z, en radians.</span><span class="sxs-lookup"><span data-stu-id="e5b36-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5b36-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e5b36-119">Return value</span></span>

<span data-ttu-id="e5b36-120">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e5b36-120">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e5b36-121">Pointeur vers une structure D3DXQUATERNION avec le lacet, le tangage et le roulis spécifiés.</span><span class="sxs-lookup"><span data-stu-id="e5b36-121">Pointer to a D3DXQUATERNION structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5b36-122">Notes </span><span class="sxs-lookup"><span data-stu-id="e5b36-122">Remarks</span></span>

<span data-ttu-id="e5b36-123">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="e5b36-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="e5b36-124">De cette façon, la fonction D3DXQuaternionRotationYawPitchRoll peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="e5b36-124">In this way, the D3DXQuaternionRotationYawPitchRoll function can be used as a parameter for another function.</span></span>

<span data-ttu-id="e5b36-125">Utilisez [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="e5b36-125">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5b36-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5b36-126">Requirements</span></span>



| <span data-ttu-id="e5b36-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e5b36-127">Requirement</span></span> | <span data-ttu-id="e5b36-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5b36-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5b36-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="e5b36-129">Header</span></span><br/>  | <dl> <span data-ttu-id="e5b36-130"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5b36-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="e5b36-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e5b36-131">Library</span></span><br/> | <dl> <span data-ttu-id="e5b36-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5b36-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e5b36-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5b36-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5b36-134">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="e5b36-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
