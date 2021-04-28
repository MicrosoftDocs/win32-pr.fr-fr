---
description: 'D3DXMatrixPerspectiveFovLH, fonction (D3DX10Math. h) : génère une matrice de projection de perspective à gauche basée sur un champ de vue.'
ms.assetid: 35ee12d6-0a58-4b00-ac8f-82f82215f02e
title: D3DXMatrixPerspectiveFovLH, fonction (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cea1bec170664993332b1cde1de375c416209209
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113087"
---
# <a name="d3dxmatrixperspectivefovlh-function-d3dx10mathh"></a><span data-ttu-id="d426c-103">D3DXMatrixPerspectiveFovLH, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="d426c-103">D3DXMatrixPerspectiveFovLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="d426c-104">Crée une matrice de projection de perspective pour un système gaucher en fonction d’un champ de vue.</span><span class="sxs-lookup"><span data-stu-id="d426c-104">Builds a left-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="d426c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d426c-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="d426c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d426c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d426c-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d426c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d426c-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d426c-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d426c-109">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="d426c-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d426c-110">*fovY* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d426c-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d426c-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d426c-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d426c-112">Champ de vue sur l’axe y, en radians.</span><span class="sxs-lookup"><span data-stu-id="d426c-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="d426c-113">*Aspect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d426c-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d426c-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d426c-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d426c-115">Proportions, défini en tant que largeur d’espace de vue divisée par la hauteur.</span><span class="sxs-lookup"><span data-stu-id="d426c-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="d426c-116">*Zn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d426c-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d426c-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d426c-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d426c-118">Valeur Z du plan de vue proche.</span><span class="sxs-lookup"><span data-stu-id="d426c-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="d426c-119">*ZF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d426c-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d426c-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d426c-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d426c-121">Valeur Z du plan d’affichage Far.</span><span class="sxs-lookup"><span data-stu-id="d426c-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d426c-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d426c-122">Return value</span></span>

<span data-ttu-id="d426c-123">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d426c-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d426c-124">Pointeur vers une structure D3DXMATRIX qui est une matrice de projection de perspective de gauche.</span><span class="sxs-lookup"><span data-stu-id="d426c-124">Pointer to a D3DXMATRIX structure that is a left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="d426c-125">Notes </span><span class="sxs-lookup"><span data-stu-id="d426c-125">Remarks</span></span>

<span data-ttu-id="d426c-126">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="d426c-126">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d426c-127">De cette façon, la fonction D3DXMatrixPerspectiveFovLH peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="d426c-127">In this way, the D3DXMatrixPerspectiveFovLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="d426c-128">Cette fonction calcule la matrice retournée comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="d426c-128">This function computes the returned matrix as shown:</span></span>


```
xScale     0          0               0
0        yScale       0               0
0          0       zf/(zf-zn)         1
0          0       -zn*zf/(zf-zn)     0
where:
yScale = cot(fovY/2)

xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="d426c-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d426c-129">Requirements</span></span>



| <span data-ttu-id="d426c-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d426c-130">Requirement</span></span> | <span data-ttu-id="d426c-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="d426c-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d426c-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="d426c-132">Header</span></span><br/>  | <dl> <span data-ttu-id="d426c-133"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d426c-133"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d426c-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d426c-134">Library</span></span><br/> | <dl> <span data-ttu-id="d426c-135"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d426c-135"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d426c-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d426c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d426c-137">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="d426c-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
