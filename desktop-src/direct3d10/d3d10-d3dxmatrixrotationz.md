---
description: Crée une matrice qui pivote autour de l’axe z.
ms.assetid: a168ea24-0cec-4e1b-a128-e9dadedf190b
title: D3DXMatrixRotationZ, fonction (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3dfe1d3d43e4110c4e7554c75fba3ac89a69ccb3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211902"
---
# <a name="d3dxmatrixrotationz-function-d3dx10mathh"></a><span data-ttu-id="0bb24-103">D3DXMatrixRotationZ, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="0bb24-103">D3DXMatrixRotationZ function (D3DX10Math.h)</span></span>

<span data-ttu-id="0bb24-104">Crée une matrice qui pivote autour de l’axe z.</span><span class="sxs-lookup"><span data-stu-id="0bb24-104">Builds a matrix that rotates around the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bb24-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0bb24-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationZ(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="0bb24-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0bb24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bb24-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0bb24-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0bb24-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0bb24-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0bb24-109">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="0bb24-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0bb24-110">*Angle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0bb24-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bb24-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0bb24-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0bb24-112">Angle de rotation, en radians.</span><span class="sxs-lookup"><span data-stu-id="0bb24-112">Angle of rotation, in radians.</span></span> <span data-ttu-id="0bb24-113">Les angles sont mesurés dans le sens des aiguilles d’une montre à partir de l’axe de rotation (côté positif) vers l’origine.</span><span class="sxs-lookup"><span data-stu-id="0bb24-113">Angles are measured clockwise when viewed from the rotation axis (positive side) toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bb24-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0bb24-114">Return value</span></span>

<span data-ttu-id="0bb24-115">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0bb24-115">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0bb24-116">Pointeur vers une structure D3DXMATRIX pivotée autour de l’axe z.</span><span class="sxs-lookup"><span data-stu-id="0bb24-116">Pointer to a D3DXMATRIX structure rotated around the z-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bb24-117">Notes</span><span class="sxs-lookup"><span data-stu-id="0bb24-117">Remarks</span></span>

<span data-ttu-id="0bb24-118">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="0bb24-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="0bb24-119">De cette façon, la fonction D3DXMatrixRotationZ peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="0bb24-119">In this way, the D3DXMatrixRotationZ function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bb24-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0bb24-120">Requirements</span></span>



| <span data-ttu-id="0bb24-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0bb24-121">Requirement</span></span> | <span data-ttu-id="0bb24-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bb24-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0bb24-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="0bb24-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0bb24-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bb24-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="0bb24-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0bb24-125">Library</span></span><br/> | <dl> <span data-ttu-id="0bb24-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0bb24-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0bb24-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bb24-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bb24-128">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="0bb24-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
