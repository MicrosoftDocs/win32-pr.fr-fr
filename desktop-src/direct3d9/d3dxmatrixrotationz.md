---
description: Crée une matrice qui pivote autour de l’axe z.
ms.assetid: 73db43e6-3831-4867-8eda-80127b61e169
title: D3DXMatrixRotationZ, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationZ
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 61d94df676016c0e22e7c0842eebe9af05b9ff71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106543031"
---
# <a name="d3dxmatrixrotationz-function-d3dx9mathh"></a><span data-ttu-id="97de5-103">D3DXMatrixRotationZ, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="97de5-103">D3DXMatrixRotationZ function (D3dx9math.h)</span></span>

<span data-ttu-id="97de5-104">Crée une matrice qui pivote autour de l’axe z.</span><span class="sxs-lookup"><span data-stu-id="97de5-104">Builds a matrix that rotates around the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="97de5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97de5-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationZ(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="97de5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97de5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97de5-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="97de5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="97de5-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="97de5-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="97de5-109">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="97de5-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="97de5-110">*Angle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97de5-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97de5-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97de5-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="97de5-112">Angle de rotation, en radians.</span><span class="sxs-lookup"><span data-stu-id="97de5-112">Angle of rotation, in radians.</span></span> <span data-ttu-id="97de5-113">Les angles sont mesurés dans le sens des aiguilles d’une montre à partir de l’axe de rotation (côté positif) vers l’origine.</span><span class="sxs-lookup"><span data-stu-id="97de5-113">Angles are measured clockwise when viewed from the rotation axis (positive side) toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97de5-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="97de5-114">Return value</span></span>

<span data-ttu-id="97de5-115">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="97de5-115">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="97de5-116">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) pivotée autour de l’axe z.</span><span class="sxs-lookup"><span data-stu-id="97de5-116">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the z-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="97de5-117">Notes</span><span class="sxs-lookup"><span data-stu-id="97de5-117">Remarks</span></span>

<span data-ttu-id="97de5-118">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="97de5-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="97de5-119">De cette façon, la fonction **D3DXMatrixRotationZ** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="97de5-119">In this way, the **D3DXMatrixRotationZ** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="97de5-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97de5-120">Requirements</span></span>



| <span data-ttu-id="97de5-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97de5-121">Requirement</span></span> | <span data-ttu-id="97de5-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="97de5-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="97de5-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="97de5-123">Header</span></span><br/>  | <dl> <span data-ttu-id="97de5-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="97de5-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="97de5-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="97de5-125">Library</span></span><br/> | <dl> <span data-ttu-id="97de5-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="97de5-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="97de5-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97de5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97de5-128">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="97de5-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="97de5-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="97de5-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="97de5-130">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="97de5-130">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="97de5-131">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="97de5-131">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="97de5-132">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="97de5-132">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="97de5-133">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="97de5-133">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> </dl>

 

 
