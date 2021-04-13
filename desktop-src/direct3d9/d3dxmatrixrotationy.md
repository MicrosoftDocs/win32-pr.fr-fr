---
description: Crée une matrice qui pivote autour de l’axe y.
ms.assetid: 80449e5d-f9bb-48c0-a787-a5e5a9d1c9a3
title: D3DXMatrixRotationY, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationY
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 81e233f3d643e99c829c7d567721e52b9b5d3e82
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323141"
---
# <a name="d3dxmatrixrotationy-function-d3dx9mathh"></a><span data-ttu-id="91784-103">D3DXMatrixRotationY, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="91784-103">D3DXMatrixRotationY function (D3dx9math.h)</span></span>

<span data-ttu-id="91784-104">Crée une matrice qui pivote autour de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="91784-104">Builds a matrix that rotates around the y-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="91784-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91784-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationY(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="91784-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91784-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91784-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="91784-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="91784-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="91784-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="91784-109">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="91784-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="91784-110">*Angle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="91784-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91784-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91784-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91784-112">Angle de rotation en radians.</span><span class="sxs-lookup"><span data-stu-id="91784-112">Angle of rotation in radians.</span></span> <span data-ttu-id="91784-113">Les angles sont mesurés dans le sens des aiguilles d’une montre sur l’axe de rotation vers l’origine.</span><span class="sxs-lookup"><span data-stu-id="91784-113">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91784-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="91784-114">Return value</span></span>

<span data-ttu-id="91784-115">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="91784-115">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="91784-116">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) pivotée autour de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="91784-116">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the y-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="91784-117">Notes</span><span class="sxs-lookup"><span data-stu-id="91784-117">Remarks</span></span>

<span data-ttu-id="91784-118">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="91784-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="91784-119">De cette façon, la fonction **D3DXMatrixRotationY** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="91784-119">In this way, the **D3DXMatrixRotationY** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="91784-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91784-120">Requirements</span></span>



| <span data-ttu-id="91784-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91784-121">Requirement</span></span> | <span data-ttu-id="91784-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="91784-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="91784-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="91784-123">Header</span></span><br/>  | <dl> <span data-ttu-id="91784-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="91784-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="91784-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="91784-125">Library</span></span><br/> | <dl> <span data-ttu-id="91784-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91784-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="91784-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91784-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91784-128">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="91784-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="91784-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="91784-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="91784-130">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="91784-130">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="91784-131">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="91784-131">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="91784-132">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="91784-132">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="91784-133">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="91784-133">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
