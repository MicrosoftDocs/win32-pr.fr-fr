---
description: Calcule le produit de deux fonctions d’harmoniques sphériques (f et g). Les deux fonctions sont de l’ordre N = 3.
ms.assetid: 2845f90f-c8a0-4ca9-b2f6-7491a2b4763b
title: D3DXSHMultiply3, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply3
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1e538bf64051f88b8f00a9ff1a183701d161941c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538538"
---
# <a name="d3dxshmultiply3-function"></a><span data-ttu-id="fd2b0-104">D3DXSHMultiply3 fonction)</span><span class="sxs-lookup"><span data-stu-id="fd2b0-104">D3DXSHMultiply3 function</span></span>

<span data-ttu-id="fd2b0-105">Calcule le produit de deux fonctions d’harmoniques sphériques (*f* et *g*).</span><span class="sxs-lookup"><span data-stu-id="fd2b0-105">Computes the product of two spherical harmonics functions (*f* and *g*).</span></span> <span data-ttu-id="fd2b0-106">Les deux fonctions sont de l’ordre N = 3.</span><span class="sxs-lookup"><span data-stu-id="fd2b0-106">Both functions are of order N = 3.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd2b0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd2b0-107">Syntax</span></span>


```C++
FLOAT* D3DXSHMultiply3(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a><span data-ttu-id="fd2b0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd2b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd2b0-109">*moue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd2b0-109">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd2b0-110">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fd2b0-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fd2b0-111">Pointeur vers les coefficients de sortie SH : la fonction de base *Y* LM est stockée à l ² + *m* + l.</span><span class="sxs-lookup"><span data-stu-id="fd2b0-111">Pointer to the output SH coefficients — the basis function *Y* ₗₘ is stored at l² + *m* + l.</span></span> <span data-ttu-id="fd2b0-112">L’ordre *N* détermine la longueur du tableau, où il doit toujours y avoir *N*-efficients ².</span><span class="sxs-lookup"><span data-stu-id="fd2b0-112">The order *N* determines the length of the array, where there should always be *N*² coefficients.</span></span>

</dd> <dt>

<span data-ttu-id="fd2b0-113">*PF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd2b0-113">*pF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd2b0-114">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="fd2b0-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fd2b0-115">Entrées SH d’entrée pour la première fonction.</span><span class="sxs-lookup"><span data-stu-id="fd2b0-115">Input SH coefficients for first function.</span></span>

</dd> <dt>

<span data-ttu-id="fd2b0-116">*PG* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd2b0-116">*pG* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd2b0-117">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="fd2b0-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fd2b0-118">Second jeu de coefficients SH d’entrée.</span><span class="sxs-lookup"><span data-stu-id="fd2b0-118">Second set of input SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd2b0-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fd2b0-119">Return value</span></span>

<span data-ttu-id="fd2b0-120">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fd2b0-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fd2b0-121">Pointeur vers les coefficients de sortie SH.</span><span class="sxs-lookup"><span data-stu-id="fd2b0-121">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd2b0-122">Notes</span><span class="sxs-lookup"><span data-stu-id="fd2b0-122">Remarks</span></span>

<span data-ttu-id="fd2b0-123">Le produit de deux fonctions SH de Order N = 3 génère une fonction SH de commande 2 × *N* -1 = 5, mais les résultats sont tronqués.</span><span class="sxs-lookup"><span data-stu-id="fd2b0-123">The product of two SH functions of order N = 3 generates an SH function of order 2 × *N* - 1 = 5, but the results are truncated.</span></span> <span data-ttu-id="fd2b0-124">Cela signifie que le produit est en mode de lancement ( *f* × *g*  =  *g* × *f* ) mais n’associe pas ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ).</span><span class="sxs-lookup"><span data-stu-id="fd2b0-124">This means that the product commutes ( *f* × *g* = *g* × *f* ) but doesn't associate ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ).</span></span>

<span data-ttu-id="fd2b0-125">Cette fonction utilise l’équation suivante :</span><span class="sxs-lookup"><span data-stu-id="fd2b0-125">This function uses the following equation:</span></span>


```
pOut[i] = int(y_i(s) * f(s) * g(s))
```



<span data-ttu-id="fd2b0-126">où y \_ correspond à la fonction énième base et où f (s) et g (s) utilisent la fonction SH suivante :</span><span class="sxs-lookup"><span data-stu-id="fd2b0-126">where y\_i(s) is the ith SH basis function, and where f(s) and g(s) use the following SH function:</span></span>


```
sum_i(y_i(s)*c_i)
```



## <a name="requirements"></a><span data-ttu-id="fd2b0-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd2b0-127">Requirements</span></span>



| <span data-ttu-id="fd2b0-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd2b0-128">Requirement</span></span> | <span data-ttu-id="fd2b0-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd2b0-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd2b0-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd2b0-130">Header</span></span><br/>  | <dl> <span data-ttu-id="fd2b0-131"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd2b0-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="fd2b0-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fd2b0-132">Library</span></span><br/> | <dl> <span data-ttu-id="fd2b0-133"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd2b0-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fd2b0-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd2b0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd2b0-135">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="fd2b0-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
