---
description: Crée une matrice avec un lacet, un tangage et un roulis spécifiés.
ms.assetid: efaab508-34ed-4373-a8d0-3bc459d75f39
title: D3DXMatrixRotationYawPitchRoll, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationYawPitchRoll
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2a8d6a531592ce49342dae0d0ecd6b3ace995bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211687"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx9mathh"></a><span data-ttu-id="84bdf-103">D3DXMatrixRotationYawPitchRoll, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="84bdf-103">D3DXMatrixRotationYawPitchRoll function (D3dx9math.h)</span></span>

<span data-ttu-id="84bdf-104">Crée une matrice avec un lacet, un tangage et un roulis spécifiés.</span><span class="sxs-lookup"><span data-stu-id="84bdf-104">Builds a matrix with a specified yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="84bdf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84bdf-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationYawPitchRoll(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Yaw,
  _In_    FLOAT      Pitch,
  _In_    FLOAT      Roll
);
```



## <a name="parameters"></a><span data-ttu-id="84bdf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84bdf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84bdf-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="84bdf-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="84bdf-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="84bdf-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="84bdf-109">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="84bdf-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="84bdf-110">*Lacet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="84bdf-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84bdf-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84bdf-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84bdf-112">Lacet autour de l’axe y, en radians.</span><span class="sxs-lookup"><span data-stu-id="84bdf-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="84bdf-113">*Espacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="84bdf-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84bdf-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84bdf-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84bdf-115">Hauteur autour de l’axe x, en radians.</span><span class="sxs-lookup"><span data-stu-id="84bdf-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="84bdf-116">*Roll* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="84bdf-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84bdf-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84bdf-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84bdf-118">Tourner autour de l’axe z, en radians.</span><span class="sxs-lookup"><span data-stu-id="84bdf-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84bdf-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="84bdf-119">Return value</span></span>

<span data-ttu-id="84bdf-120">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="84bdf-120">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="84bdf-121">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) avec le lacet, le tangage et le roulis spécifiés.</span><span class="sxs-lookup"><span data-stu-id="84bdf-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="84bdf-122">Notes</span><span class="sxs-lookup"><span data-stu-id="84bdf-122">Remarks</span></span>

<span data-ttu-id="84bdf-123">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="84bdf-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="84bdf-124">De cette façon, la fonction **D3DXMatrixRotationYawPitchRoll** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="84bdf-124">In this way, the **D3DXMatrixRotationYawPitchRoll** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="84bdf-125">L’ordre des transformations est le premier, puis le tangage, puis le lacet.</span><span class="sxs-lookup"><span data-stu-id="84bdf-125">The order of transformations is roll first, then pitch, then yaw.</span></span> <span data-ttu-id="84bdf-126">Par rapport à l’axe de coordonnées local de l’objet, cette valeur est équivalente à la rotation autour de l’axe z, suivie d’une rotation autour de l’axe x, suivie d’une rotation autour de l’axe y, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="84bdf-126">Relative to the object's local coordinate axis, this is equivalent to rotation around the z-axis, followed by rotation around the x-axis, followed by rotation around the y-axis, as shown in the following illustration.</span></span>

![illustration du rouleau, du tangage et du lacet comme rotations autour des trois axes](images/pitchyawroll.png)

## <a name="requirements"></a><span data-ttu-id="84bdf-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84bdf-128">Requirements</span></span>



| <span data-ttu-id="84bdf-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84bdf-129">Requirement</span></span> | <span data-ttu-id="84bdf-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="84bdf-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="84bdf-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="84bdf-131">Header</span></span><br/>  | <dl> <span data-ttu-id="84bdf-132"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="84bdf-132"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="84bdf-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="84bdf-133">Library</span></span><br/> | <dl> <span data-ttu-id="84bdf-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="84bdf-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="84bdf-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84bdf-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84bdf-136">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="84bdf-136">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="84bdf-137">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="84bdf-137">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="84bdf-138">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="84bdf-138">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="84bdf-139">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="84bdf-139">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="84bdf-140">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="84bdf-140">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="84bdf-141">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="84bdf-141">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
