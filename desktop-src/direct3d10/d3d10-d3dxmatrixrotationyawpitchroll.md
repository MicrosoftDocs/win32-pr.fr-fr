---
description: Crée une matrice avec un lacet, un tangage et un roulis spécifiés.
ms.assetid: a3ef2b57-275f-484a-88fc-aaa5e470717c
title: D3DXMatrixRotationYawPitchRoll, fonction (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d65242f49ee94394337f43555c3e154141e3b642
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953978"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx10mathh"></a><span data-ttu-id="eb4a2-103">D3DXMatrixRotationYawPitchRoll, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="eb4a2-103">D3DXMatrixRotationYawPitchRoll function (D3DX10Math.h)</span></span>

<span data-ttu-id="eb4a2-104">Crée une matrice avec un lacet, un tangage et un roulis spécifiés.</span><span class="sxs-lookup"><span data-stu-id="eb4a2-104">Builds a matrix with a specified yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb4a2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb4a2-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationYawPitchRoll(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Yaw,
  _In_    FLOAT      Pitch,
  _In_    FLOAT      Roll
);
```



## <a name="parameters"></a><span data-ttu-id="eb4a2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb4a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb4a2-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="eb4a2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb4a2-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="eb4a2-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="eb4a2-109">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="eb4a2-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="eb4a2-110">*Lacet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb4a2-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb4a2-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb4a2-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb4a2-112">Lacet autour de l’axe y, en radians.</span><span class="sxs-lookup"><span data-stu-id="eb4a2-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="eb4a2-113">*Espacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb4a2-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb4a2-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb4a2-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb4a2-115">Hauteur autour de l’axe x, en radians.</span><span class="sxs-lookup"><span data-stu-id="eb4a2-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="eb4a2-116">*Roll* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb4a2-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb4a2-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb4a2-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb4a2-118">Tourner autour de l’axe z, en radians.</span><span class="sxs-lookup"><span data-stu-id="eb4a2-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb4a2-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb4a2-119">Return value</span></span>

<span data-ttu-id="eb4a2-120">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="eb4a2-120">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="eb4a2-121">Pointeur vers une structure D3DXMATRIX avec le lacet, le tangage et le roulis spécifiés.</span><span class="sxs-lookup"><span data-stu-id="eb4a2-121">Pointer to a D3DXMATRIX structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb4a2-122">Notes</span><span class="sxs-lookup"><span data-stu-id="eb4a2-122">Remarks</span></span>

<span data-ttu-id="eb4a2-123">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="eb4a2-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="eb4a2-124">De cette façon, la fonction D3DXMatrixRotationYawPitchRoll peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="eb4a2-124">In this way, the D3DXMatrixRotationYawPitchRoll function can be used as a parameter for another function.</span></span>

<span data-ttu-id="eb4a2-125">L’ordre des transformations est le premier, puis le tangage, puis le lacet.</span><span class="sxs-lookup"><span data-stu-id="eb4a2-125">The order of transformations is roll first, then pitch, then yaw.</span></span> <span data-ttu-id="eb4a2-126">Par rapport à l’axe de coordonnées local de l’objet, cette valeur est équivalente à la rotation autour de l’axe z, suivie d’une rotation autour de l’axe x, suivie d’une rotation autour de l’axe y, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="eb4a2-126">Relative to the object's local coordinate axis, this is equivalent to rotation around the z-axis, followed by rotation around the x-axis, followed by rotation around the y-axis, as shown in the following illustration.</span></span>

![illustration du rouleau, du tangage et du lacet comme rotations autour des trois axes](images/pitchyawroll.png)

## <a name="requirements"></a><span data-ttu-id="eb4a2-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb4a2-128">Requirements</span></span>



| <span data-ttu-id="eb4a2-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb4a2-129">Requirement</span></span> | <span data-ttu-id="eb4a2-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb4a2-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb4a2-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="eb4a2-131">Header</span></span><br/>  | <dl> <span data-ttu-id="eb4a2-132"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb4a2-132"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="eb4a2-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eb4a2-133">Library</span></span><br/> | <dl> <span data-ttu-id="eb4a2-134"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb4a2-134"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eb4a2-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb4a2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb4a2-136">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="eb4a2-136">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
