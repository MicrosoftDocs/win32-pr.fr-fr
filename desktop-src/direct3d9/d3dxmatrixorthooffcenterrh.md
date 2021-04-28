---
description: 'D3DXMatrixOrthoOffCenterRH, fonction (D3dx9math. h) : génère une matrice de projection orthographique personnalisée et droitier.'
ms.assetid: d6171e28-b138-4ccf-9f12-fb977a30aca1
title: D3DXMatrixOrthoOffCenterRH, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8519dca07a4475ff043491802ae173ecc61c0bd3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107457"
---
# <a name="d3dxmatrixorthooffcenterrh-function-d3dx9mathh"></a><span data-ttu-id="1a839-103">D3DXMatrixOrthoOffCenterRH, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="1a839-103">D3DXMatrixOrthoOffCenterRH function (D3dx9math.h)</span></span>

<span data-ttu-id="1a839-104">Crée une matrice de projection orthographique personnalisée et droitier.</span><span class="sxs-lookup"><span data-stu-id="1a839-104">Builds a customized, right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a839-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a839-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="1a839-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a839-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a839-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1a839-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a839-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1a839-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1a839-109">Pointeur vers le [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)résultant.</span><span class="sxs-lookup"><span data-stu-id="1a839-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a839-110">*l* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a839-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a839-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1a839-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1a839-112">Valeur x minimale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="1a839-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="1a839-113">*r* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a839-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a839-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1a839-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1a839-115">Valeur x maximale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="1a839-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="1a839-116">*b* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a839-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a839-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1a839-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1a839-118">Valeur y minimale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="1a839-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="1a839-119">*t* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a839-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a839-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1a839-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1a839-121">Valeur y maximale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="1a839-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="1a839-122">*Zn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a839-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a839-123">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1a839-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1a839-124">Valeur z minimale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="1a839-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="1a839-125">*ZF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a839-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a839-126">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1a839-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1a839-127">Valeur z maximale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="1a839-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a839-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1a839-128">Return value</span></span>

<span data-ttu-id="1a839-129">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1a839-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1a839-130">Pointeur vers le [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)résultant.</span><span class="sxs-lookup"><span data-stu-id="1a839-130">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1a839-131">Notes </span><span class="sxs-lookup"><span data-stu-id="1a839-131">Remarks</span></span>

<span data-ttu-id="1a839-132">La fonction [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) est un cas particulier de la fonction **D3DXMatrixOrthoOffCenterRH** .</span><span class="sxs-lookup"><span data-stu-id="1a839-132">The [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) function is a special case of the **D3DXMatrixOrthoOffCenterRH** function.</span></span> <span data-ttu-id="1a839-133">Pour créer la même projection à l’aide de **D3DXMatrixOrthoOffCenterRH**, utilisez les valeurs suivantes : l =-w/2, r = w/2, b =-h/2 et t = h/2.</span><span class="sxs-lookup"><span data-stu-id="1a839-133">To create the same projection using **D3DXMatrixOrthoOffCenterRH**, use the following values: l = -w/2, r = w/2, b = -h/2, and t = h/2.</span></span>

<span data-ttu-id="1a839-134">Tous les paramètres de la fonction **D3DXMatrixOrthoOffCenterRH** sont des distances dans l’espace de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="1a839-134">All the parameters of the **D3DXMatrixOrthoOffCenterRH** function are distances in camera space.</span></span> <span data-ttu-id="1a839-135">Les paramètres décrivent les dimensions du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="1a839-135">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="1a839-136">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="1a839-136">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="1a839-137">De cette façon, la fonction **D3DXMatrixOrthoOffCenterRH** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="1a839-137">In this way, the **D3DXMatrixOrthoOffCenterRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1a839-138">Cette fonction utilise la formule suivante pour calculer la matrice retournée.</span><span class="sxs-lookup"><span data-stu-id="1a839-138">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zn-zf)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="1a839-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a839-139">Requirements</span></span>



| <span data-ttu-id="1a839-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a839-140">Requirement</span></span> | <span data-ttu-id="1a839-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a839-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a839-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="1a839-142">Header</span></span><br/>  | <dl> <span data-ttu-id="1a839-143"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a839-143"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1a839-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1a839-144">Library</span></span><br/> | <dl> <span data-ttu-id="1a839-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a839-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1a839-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a839-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a839-147">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="1a839-147">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="1a839-148">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="1a839-148">**D3DXMatrixOrthoRH**</span></span>](d3dxmatrixorthorh.md)
</dt> <dt>

[<span data-ttu-id="1a839-149">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="1a839-149">**D3DXMatrixOrthoLH**</span></span>](d3dxmatrixortholh.md)
</dt> <dt>

[<span data-ttu-id="1a839-150">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="1a839-150">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
