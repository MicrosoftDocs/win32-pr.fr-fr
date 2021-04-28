---
description: 'D3DXMatrixRotationYawPitchRoll, fonction (D3DX10Math. h) : crée une matrice avec un lacet, un tangage et un rouleau spécifiés.'
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
ms.openlocfilehash: ae00865c45878159dbf86a6f829e9d1cf50337e3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108947"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx10mathh"></a><span data-ttu-id="996f5-103">D3DXMatrixRotationYawPitchRoll, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="996f5-103">D3DXMatrixRotationYawPitchRoll function (D3DX10Math.h)</span></span>

<span data-ttu-id="996f5-104">Crée une matrice avec un lacet, un tangage et un roulis spécifiés.</span><span class="sxs-lookup"><span data-stu-id="996f5-104">Builds a matrix with a specified yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="996f5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="996f5-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationYawPitchRoll(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Yaw,
  _In_    FLOAT      Pitch,
  _In_    FLOAT      Roll
);
```



## <a name="parameters"></a><span data-ttu-id="996f5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="996f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="996f5-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="996f5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="996f5-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="996f5-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="996f5-109">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="996f5-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="996f5-110">*Lacet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="996f5-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="996f5-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="996f5-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="996f5-112">Lacet autour de l’axe y, en radians.</span><span class="sxs-lookup"><span data-stu-id="996f5-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="996f5-113">*Espacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="996f5-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="996f5-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="996f5-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="996f5-115">Hauteur autour de l’axe x, en radians.</span><span class="sxs-lookup"><span data-stu-id="996f5-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="996f5-116">*Roll* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="996f5-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="996f5-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="996f5-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="996f5-118">Tourner autour de l’axe z, en radians.</span><span class="sxs-lookup"><span data-stu-id="996f5-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="996f5-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="996f5-119">Return value</span></span>

<span data-ttu-id="996f5-120">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="996f5-120">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="996f5-121">Pointeur vers une structure D3DXMATRIX avec le lacet, le tangage et le roulis spécifiés.</span><span class="sxs-lookup"><span data-stu-id="996f5-121">Pointer to a D3DXMATRIX structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="996f5-122">Notes </span><span class="sxs-lookup"><span data-stu-id="996f5-122">Remarks</span></span>

<span data-ttu-id="996f5-123">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="996f5-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="996f5-124">De cette façon, la fonction D3DXMatrixRotationYawPitchRoll peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="996f5-124">In this way, the D3DXMatrixRotationYawPitchRoll function can be used as a parameter for another function.</span></span>

<span data-ttu-id="996f5-125">L’ordre des transformations est le premier, puis le tangage, puis le lacet.</span><span class="sxs-lookup"><span data-stu-id="996f5-125">The order of transformations is roll first, then pitch, then yaw.</span></span> <span data-ttu-id="996f5-126">Par rapport à l’axe de coordonnées local de l’objet, cette valeur est équivalente à la rotation autour de l’axe z, suivie d’une rotation autour de l’axe x, suivie d’une rotation autour de l’axe y, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="996f5-126">Relative to the object's local coordinate axis, this is equivalent to rotation around the z-axis, followed by rotation around the x-axis, followed by rotation around the y-axis, as shown in the following illustration.</span></span>

![illustration du rouleau, du tangage et du lacet comme rotations autour des trois axes](images/pitchyawroll.png)

## <a name="requirements"></a><span data-ttu-id="996f5-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="996f5-128">Requirements</span></span>



| <span data-ttu-id="996f5-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="996f5-129">Requirement</span></span> | <span data-ttu-id="996f5-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="996f5-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="996f5-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="996f5-131">Header</span></span><br/>  | <dl> <span data-ttu-id="996f5-132"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="996f5-132"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="996f5-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="996f5-133">Library</span></span><br/> | <dl> <span data-ttu-id="996f5-134"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="996f5-134"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="996f5-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="996f5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="996f5-136">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="996f5-136">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
