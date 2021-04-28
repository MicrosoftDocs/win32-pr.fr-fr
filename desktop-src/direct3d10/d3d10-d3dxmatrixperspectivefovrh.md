---
description: 'D3DXMatrixPerspectiveFovRH, fonction (D3DX10Math. h) : génère une matrice de projection de perspective à droite reposant sur un champ de vue.'
ms.assetid: a75e6666-e6c0-4a54-bc88-835fa012542f
title: D3DXMatrixPerspectiveFovRH, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveFovRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 38d48789bab9b968b6bcf657459c408abdba774b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109107"
---
# <a name="d3dxmatrixperspectivefovrh-function-d3dx10mathh"></a><span data-ttu-id="5ff38-103">D3DXMatrixPerspectiveFovRH, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="5ff38-103">D3DXMatrixPerspectiveFovRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="5ff38-104">Crée une matrice de projection de perspective pour un système droitier en fonction d’un champ de vue.</span><span class="sxs-lookup"><span data-stu-id="5ff38-104">Builds a right-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ff38-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ff38-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="5ff38-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ff38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ff38-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5ff38-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ff38-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="5ff38-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5ff38-109">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="5ff38-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5ff38-110">*fovY* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ff38-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ff38-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ff38-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ff38-112">Champ de vue sur l’axe y, en radians.</span><span class="sxs-lookup"><span data-stu-id="5ff38-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="5ff38-113">*Aspect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ff38-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ff38-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ff38-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ff38-115">Proportions, défini en tant que largeur d’espace de vue divisée par la hauteur.</span><span class="sxs-lookup"><span data-stu-id="5ff38-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="5ff38-116">*Zn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ff38-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ff38-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ff38-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ff38-118">Valeur Z du plan de vue proche.</span><span class="sxs-lookup"><span data-stu-id="5ff38-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="5ff38-119">*ZF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ff38-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ff38-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ff38-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ff38-121">Valeur Z du plan d’affichage Far.</span><span class="sxs-lookup"><span data-stu-id="5ff38-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ff38-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5ff38-122">Return value</span></span>

<span data-ttu-id="5ff38-123">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="5ff38-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5ff38-124">Pointeur vers une structure D3DXMATRIX qui est une matrice de projection de perspective à droite.</span><span class="sxs-lookup"><span data-stu-id="5ff38-124">Pointer to a D3DXMATRIX structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ff38-125">Notes </span><span class="sxs-lookup"><span data-stu-id="5ff38-125">Remarks</span></span>

<span data-ttu-id="5ff38-126">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="5ff38-126">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="5ff38-127">De cette façon, la fonction D3DXMatrixPerspectiveFovRH peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="5ff38-127">In this way, the D3DXMatrixPerspectiveFovRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="5ff38-128">Cette fonction calcule la matrice retournée comme indiqué.</span><span class="sxs-lookup"><span data-stu-id="5ff38-128">This function computes the returned matrix as shown.</span></span>


```
xScale     0          0              0
0        yScale       0              0
0          0      zf/(zn-zf)        -1
0          0      zn*zf/(zn-zf)      0
where:
yScale = cot(fovY/2)
    
xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="5ff38-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ff38-129">Requirements</span></span>



| <span data-ttu-id="5ff38-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ff38-130">Requirement</span></span> | <span data-ttu-id="5ff38-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ff38-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ff38-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ff38-132">Header</span></span><br/>  | <dl> <span data-ttu-id="5ff38-133"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ff38-133"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="5ff38-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5ff38-134">Library</span></span><br/> | <dl> <span data-ttu-id="5ff38-135"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ff38-135"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5ff38-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ff38-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ff38-137">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="5ff38-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
