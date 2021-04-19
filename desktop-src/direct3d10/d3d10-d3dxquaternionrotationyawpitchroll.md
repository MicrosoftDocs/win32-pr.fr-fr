---
description: Génère un Quaternion avec le lacet, le tangage et le roulis donnés.
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
ms.openlocfilehash: 7d894be61f5f22322f83c4e4a6c6a724de4b9da4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537275"
---
# <a name="d3dxquaternionrotationyawpitchroll-function-d3dx10mathh"></a><span data-ttu-id="51b9c-103">D3DXQuaternionRotationYawPitchRoll, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="51b9c-103">D3DXQuaternionRotationYawPitchRoll function (D3DX10Math.h)</span></span>

<span data-ttu-id="51b9c-104">Génère un Quaternion avec le lacet, le tangage et le roulis donnés.</span><span class="sxs-lookup"><span data-stu-id="51b9c-104">Builds a quaternion with the given yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="51b9c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51b9c-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationYawPitchRoll(
  _Inout_ D3DXQUATERNION *pOut,
  _In_    FLOAT          Yaw,
  _In_    FLOAT          Pitch,
  _In_    FLOAT          Roll
);
```



## <a name="parameters"></a><span data-ttu-id="51b9c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51b9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51b9c-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="51b9c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="51b9c-108">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="51b9c-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="51b9c-109">Pointeur vers le [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="51b9c-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="51b9c-110">*Lacet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="51b9c-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51b9c-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="51b9c-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="51b9c-112">Lacet autour de l’axe y, en radians.</span><span class="sxs-lookup"><span data-stu-id="51b9c-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="51b9c-113">*Espacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="51b9c-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51b9c-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="51b9c-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="51b9c-115">Hauteur autour de l’axe x, en radians.</span><span class="sxs-lookup"><span data-stu-id="51b9c-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="51b9c-116">*Roll* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="51b9c-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51b9c-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="51b9c-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="51b9c-118">Tourner autour de l’axe z, en radians.</span><span class="sxs-lookup"><span data-stu-id="51b9c-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51b9c-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="51b9c-119">Return value</span></span>

<span data-ttu-id="51b9c-120">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="51b9c-120">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="51b9c-121">Pointeur vers une structure D3DXQUATERNION avec le lacet, le tangage et le roulis spécifiés.</span><span class="sxs-lookup"><span data-stu-id="51b9c-121">Pointer to a D3DXQUATERNION structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="51b9c-122">Notes</span><span class="sxs-lookup"><span data-stu-id="51b9c-122">Remarks</span></span>

<span data-ttu-id="51b9c-123">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="51b9c-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="51b9c-124">De cette façon, la fonction D3DXQuaternionRotationYawPitchRoll peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="51b9c-124">In this way, the D3DXQuaternionRotationYawPitchRoll function can be used as a parameter for another function.</span></span>

<span data-ttu-id="51b9c-125">Utilisez [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="51b9c-125">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="51b9c-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51b9c-126">Requirements</span></span>



| <span data-ttu-id="51b9c-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51b9c-127">Requirement</span></span> | <span data-ttu-id="51b9c-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="51b9c-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51b9c-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="51b9c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="51b9c-130"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="51b9c-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="51b9c-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="51b9c-131">Library</span></span><br/> | <dl> <span data-ttu-id="51b9c-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="51b9c-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="51b9c-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51b9c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51b9c-134">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="51b9c-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
