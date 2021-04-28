---
description: 'D3DXMatrixOrthoOffCenterRH, fonction (D3DX10Math. h) : génère une matrice de projection orthographique personnalisée et droitier.'
ms.assetid: 01d4d61e-de7b-4431-a168-68a50b1d6021
title: D3DXMatrixOrthoOffCenterRH, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoOffCenterRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0b41038021cc34cb02961cb9894415995955404c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113077"
---
# <a name="d3dxmatrixorthooffcenterrh-function-d3dx10mathh"></a><span data-ttu-id="1e99c-103">D3DXMatrixOrthoOffCenterRH, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="1e99c-103">D3DXMatrixOrthoOffCenterRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="1e99c-104">Crée une matrice de projection orthographique personnalisée et droitier.</span><span class="sxs-lookup"><span data-stu-id="1e99c-104">Builds a customized, right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e99c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e99c-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoOffCenterRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="1e99c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e99c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e99c-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1e99c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e99c-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1e99c-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1e99c-109">Pointeur vers le [**D3DXMATRIX**](d3d10-d3dxmatrix.md)résultant.</span><span class="sxs-lookup"><span data-stu-id="1e99c-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e99c-110">*l* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e99c-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e99c-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1e99c-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1e99c-112">Valeur x minimale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="1e99c-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="1e99c-113">*r* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e99c-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e99c-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1e99c-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1e99c-115">Valeur x maximale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="1e99c-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="1e99c-116">*b* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e99c-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e99c-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1e99c-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1e99c-118">Valeur y minimale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="1e99c-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="1e99c-119">*t* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e99c-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e99c-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1e99c-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1e99c-121">Valeur y maximale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="1e99c-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="1e99c-122">*Zn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e99c-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e99c-123">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1e99c-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1e99c-124">Valeur z minimale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="1e99c-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="1e99c-125">*ZF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e99c-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e99c-126">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1e99c-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1e99c-127">Valeur z maximale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="1e99c-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e99c-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1e99c-128">Return value</span></span>

<span data-ttu-id="1e99c-129">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1e99c-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1e99c-130">Pointeur vers le [**D3DXMATRIX**](d3d10-d3dxmatrix.md)résultant.</span><span class="sxs-lookup"><span data-stu-id="1e99c-130">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1e99c-131">Notes </span><span class="sxs-lookup"><span data-stu-id="1e99c-131">Remarks</span></span>

<span data-ttu-id="1e99c-132">La fonction [**D3DXMatrixOrthoRH**](d3d10-d3dxmatrixorthorh.md) est un cas particulier de la fonction D3DXMatrixOrthoOffCenterRH.</span><span class="sxs-lookup"><span data-stu-id="1e99c-132">The [**D3DXMatrixOrthoRH**](d3d10-d3dxmatrixorthorh.md) function is a special case of the D3DXMatrixOrthoOffCenterRH function.</span></span> <span data-ttu-id="1e99c-133">Pour créer la même projection à l’aide de D3DXMatrixOrthoOffCenterRH, utilisez les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="1e99c-133">To create the same projection using D3DXMatrixOrthoOffCenterRH, use the following values:</span></span>

<span data-ttu-id="1e99c-134">l =-w/2,</span><span class="sxs-lookup"><span data-stu-id="1e99c-134">l = -w/2,</span></span>

<span data-ttu-id="1e99c-135">r = w/2,</span><span class="sxs-lookup"><span data-stu-id="1e99c-135">r = w/2,</span></span>

<span data-ttu-id="1e99c-136">b =-h/2 et</span><span class="sxs-lookup"><span data-stu-id="1e99c-136">b = -h/2, and</span></span>

<span data-ttu-id="1e99c-137">t = h/2.</span><span class="sxs-lookup"><span data-stu-id="1e99c-137">t = h/2.</span></span>

<span data-ttu-id="1e99c-138">Tous les paramètres de la fonction D3DXMatrixOrthoOffCenterRH sont des distances dans l’espace de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="1e99c-138">All the parameters of the D3DXMatrixOrthoOffCenterRH function are distances in camera space.</span></span> <span data-ttu-id="1e99c-139">Les paramètres décrivent les dimensions du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="1e99c-139">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="1e99c-140">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="1e99c-140">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1e99c-141">De cette façon, la fonction D3DXMatrixOrthoOffCenterRH peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="1e99c-141">In this way, the D3DXMatrixOrthoOffCenterRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1e99c-142">Cette fonction utilise la formule suivante pour calculer la matrice retournée.</span><span class="sxs-lookup"><span data-stu-id="1e99c-142">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zn-zf)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="1e99c-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e99c-143">Requirements</span></span>



| <span data-ttu-id="1e99c-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e99c-144">Requirement</span></span> | <span data-ttu-id="1e99c-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e99c-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e99c-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="1e99c-146">Header</span></span><br/>  | <dl> <span data-ttu-id="1e99c-147"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e99c-147"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="1e99c-148">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1e99c-148">Library</span></span><br/> | <dl> <span data-ttu-id="1e99c-149"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e99c-149"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1e99c-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e99c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e99c-151">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="1e99c-151">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
