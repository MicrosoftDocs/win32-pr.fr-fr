---
description: Crée une matrice qui pivote autour de l’axe x.
ms.assetid: 45a2668d-787f-4354-882a-94a72edaa543
title: D3DXMatrixRotationX, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c1d3dd85a4cd0e5f9e668856a4d6d2f87bbdf108
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394051"
---
# <a name="d3dxmatrixrotationx-function-d3dx9mathh"></a><span data-ttu-id="168e4-103">D3DXMatrixRotationX, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="168e4-103">D3DXMatrixRotationX function (D3dx9math.h)</span></span>

<span data-ttu-id="168e4-104">Crée une matrice qui pivote autour de l’axe x.</span><span class="sxs-lookup"><span data-stu-id="168e4-104">Builds a matrix that rotates around the x-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="168e4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="168e4-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationX(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="168e4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="168e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="168e4-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="168e4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="168e4-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="168e4-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="168e4-109">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="168e4-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="168e4-110">*Angle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="168e4-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="168e4-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="168e4-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="168e4-112">Angle de rotation en radians.</span><span class="sxs-lookup"><span data-stu-id="168e4-112">Angle of rotation in radians.</span></span> <span data-ttu-id="168e4-113">Les angles sont mesurés dans le sens des aiguilles d’une montre sur l’axe de rotation vers l’origine.</span><span class="sxs-lookup"><span data-stu-id="168e4-113">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="168e4-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="168e4-114">Return value</span></span>

<span data-ttu-id="168e4-115">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="168e4-115">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="168e4-116">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) pivotée autour de l’axe x.</span><span class="sxs-lookup"><span data-stu-id="168e4-116">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the x-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="168e4-117">Notes</span><span class="sxs-lookup"><span data-stu-id="168e4-117">Remarks</span></span>

<span data-ttu-id="168e4-118">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="168e4-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="168e4-119">De cette façon, la fonction **D3DXMatrixRotationX** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="168e4-119">In this way, the **D3DXMatrixRotationX** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="168e4-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="168e4-120">Requirements</span></span>



| <span data-ttu-id="168e4-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="168e4-121">Requirement</span></span> | <span data-ttu-id="168e4-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="168e4-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="168e4-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="168e4-123">Header</span></span><br/>  | <dl> <span data-ttu-id="168e4-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="168e4-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="168e4-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="168e4-125">Library</span></span><br/> | <dl> <span data-ttu-id="168e4-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="168e4-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="168e4-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="168e4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="168e4-128">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="168e4-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="168e4-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="168e4-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="168e4-130">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="168e4-130">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="168e4-131">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="168e4-131">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="168e4-132">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="168e4-132">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="168e4-133">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="168e4-133">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
