---
description: 'D3DXMatrixPerspectiveFovLH, fonction (D3dx9math. h) : génère une matrice de projection de perspective à gauche basée sur un champ de vue.'
ms.assetid: 90328798-f124-4b61-90a9-971946066b02
title: D3DXMatrixPerspectiveFovLH, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveFovLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: eec478fec30567fbf301054ddfa60f1689bfee8e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118347"
---
# <a name="d3dxmatrixperspectivefovlh-function-d3dx9mathh"></a><span data-ttu-id="b1ea6-103">D3DXMatrixPerspectiveFovLH, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="b1ea6-103">D3DXMatrixPerspectiveFovLH function (D3dx9math.h)</span></span>

<span data-ttu-id="b1ea6-104">Crée une matrice de projection de perspective pour un système gaucher en fonction d’un champ de vue.</span><span class="sxs-lookup"><span data-stu-id="b1ea6-104">Builds a left-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1ea6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1ea6-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="b1ea6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1ea6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1ea6-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b1ea6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1ea6-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b1ea6-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b1ea6-109">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="b1ea6-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b1ea6-110">*fovY* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b1ea6-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1ea6-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1ea6-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1ea6-112">Champ de vue sur l’axe y, en radians.</span><span class="sxs-lookup"><span data-stu-id="b1ea6-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="b1ea6-113">*Aspect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b1ea6-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1ea6-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1ea6-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1ea6-115">Proportions, défini en tant que largeur d’espace de vue divisée par la hauteur.</span><span class="sxs-lookup"><span data-stu-id="b1ea6-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="b1ea6-116">*Zn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b1ea6-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1ea6-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1ea6-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1ea6-118">Valeur Z du plan de vue proche.</span><span class="sxs-lookup"><span data-stu-id="b1ea6-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="b1ea6-119">*ZF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b1ea6-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1ea6-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1ea6-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1ea6-121">Valeur Z du plan d’affichage Far.</span><span class="sxs-lookup"><span data-stu-id="b1ea6-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1ea6-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b1ea6-122">Return value</span></span>

<span data-ttu-id="b1ea6-123">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b1ea6-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b1ea6-124">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) qui est une matrice de projection de perspective de gauche.</span><span class="sxs-lookup"><span data-stu-id="b1ea6-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1ea6-125">Notes </span><span class="sxs-lookup"><span data-stu-id="b1ea6-125">Remarks</span></span>

<span data-ttu-id="b1ea6-126">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="b1ea6-126">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="b1ea6-127">De cette façon, la fonction **D3DXMatrixPerspectiveFovLH** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="b1ea6-127">In this way, the **D3DXMatrixPerspectiveFovLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="b1ea6-128">Pour modifier l’axe des proportions, utilisez la formule de calcul : fovY = 2 \* Math. ATAN (Math. Tan (fovY \* 0,5)/aspect).</span><span class="sxs-lookup"><span data-stu-id="b1ea6-128">To change the aspect ratio axis, use the calculation formula: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspect).</span></span> <span data-ttu-id="b1ea6-129">Vous pouvez également ajouter des variables de proportions X et Y dans la structure pour mettre à l’échelle l’espace d’affichage vertical : fovY = 2 \* Math. ATAN (Math. Tan (fovY \* 0,5)/aspecty), aspect = aspectX \* aspect Y.</span><span class="sxs-lookup"><span data-stu-id="b1ea6-129">Alternatively, add X and Y aspect ratio variables in the structure to scale the vertical view space: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspectY), aspect = aspectX \* aspect Y.</span></span>

<span data-ttu-id="b1ea6-130">Cette fonction calcule la matrice retournée comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="b1ea6-130">This function computes the returned matrix as shown:</span></span>


```
xScale     0          0               0
0        yScale       0               0
0          0       zf/(zf-zn)         1
0          0       -zn*zf/(zf-zn)     0
where:
yScale = cot(fovY/2)

xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="b1ea6-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1ea6-131">Requirements</span></span>



| <span data-ttu-id="b1ea6-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1ea6-132">Requirement</span></span> | <span data-ttu-id="b1ea6-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1ea6-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1ea6-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="b1ea6-134">Header</span></span><br/>  | <dl> <span data-ttu-id="b1ea6-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1ea6-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b1ea6-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b1ea6-136">Library</span></span><br/> | <dl> <span data-ttu-id="b1ea6-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1ea6-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b1ea6-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1ea6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1ea6-139">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="b1ea6-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="b1ea6-140">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="b1ea6-140">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="b1ea6-141">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="b1ea6-141">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="b1ea6-142">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="b1ea6-142">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="b1ea6-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="b1ea6-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="b1ea6-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="b1ea6-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
