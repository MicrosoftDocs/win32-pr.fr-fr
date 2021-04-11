---
description: Génère une matrice de projection orthographique de gauche.
ms.assetid: 67bec4a3-2126-4f5a-9301-97faa6dc6e84
title: D3DXMatrixOrthoLH, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0b49e6008b52f7060075688730c72f5f5d3f725a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211911"
---
# <a name="d3dxmatrixortholh-function-d3dx10mathh"></a><span data-ttu-id="d57ed-103">D3DXMatrixOrthoLH, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="d57ed-103">D3DXMatrixOrthoLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="d57ed-104">Génère une matrice de projection orthographique de gauche.</span><span class="sxs-lookup"><span data-stu-id="d57ed-104">Builds a left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d57ed-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d57ed-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="d57ed-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d57ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d57ed-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d57ed-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d57ed-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d57ed-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d57ed-109">Pointeur vers le [**D3DXMATRIX**](d3d10-d3dxmatrix.md)résultant.</span><span class="sxs-lookup"><span data-stu-id="d57ed-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="d57ed-110">*w* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d57ed-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d57ed-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d57ed-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d57ed-112">Largeur du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="d57ed-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d57ed-113">*h* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d57ed-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d57ed-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d57ed-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d57ed-115">Hauteur du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="d57ed-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d57ed-116">*Zn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d57ed-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d57ed-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d57ed-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d57ed-118">Valeur z minimale du volume de la vue, appelée z-near.</span><span class="sxs-lookup"><span data-stu-id="d57ed-118">Minimum z-value of the view volume which is referred to as z-near.</span></span>

</dd> <dt>

<span data-ttu-id="d57ed-119">*ZF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d57ed-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d57ed-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d57ed-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d57ed-121">Valeur z maximale du volume de la vue, appelée z-Far.</span><span class="sxs-lookup"><span data-stu-id="d57ed-121">Maximum z-value of the view volume which is referred to as z-far.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d57ed-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d57ed-122">Return value</span></span>

<span data-ttu-id="d57ed-123">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d57ed-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d57ed-124">Pointeur vers le [**D3DXMATRIX**](d3d10-d3dxmatrix.md)résultant.</span><span class="sxs-lookup"><span data-stu-id="d57ed-124">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d57ed-125">Notes</span><span class="sxs-lookup"><span data-stu-id="d57ed-125">Remarks</span></span>

<span data-ttu-id="d57ed-126">Tous les paramètres de la fonction D3DXMatrixOrthoLH sont des distances dans l’espace de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="d57ed-126">All the parameters of the D3DXMatrixOrthoLH function are distances in camera space.</span></span> <span data-ttu-id="d57ed-127">Les paramètres décrivent les dimensions du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="d57ed-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="d57ed-128">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="d57ed-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d57ed-129">De cette façon, la fonction D3DXMatrixOrthoLH peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="d57ed-129">In this way, the D3DXMatrixOrthoLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="d57ed-130">Cette fonction utilise la formule suivante pour calculer la matrice retournée.</span><span class="sxs-lookup"><span data-stu-id="d57ed-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zf-zn)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="d57ed-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d57ed-131">Requirements</span></span>



| <span data-ttu-id="d57ed-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d57ed-132">Requirement</span></span> | <span data-ttu-id="d57ed-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="d57ed-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d57ed-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="d57ed-134">Header</span></span><br/>  | <dl> <span data-ttu-id="d57ed-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d57ed-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d57ed-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d57ed-136">Library</span></span><br/> | <dl> <span data-ttu-id="d57ed-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d57ed-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d57ed-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d57ed-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d57ed-139">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="d57ed-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
