---
description: Calcule le produit de deux fonctions représentées à l’aide de SH (f et g).
ms.assetid: 632400a4-2ac9-438d-85f7-869101f350c8
title: D3DXSHMultiply2, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply2
- D3DXSHMultiply3
- D3DXSHMultiply4
- D3DXSHMultiply5
- D3DXSHMultiply6
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: f7b9adaf5caf7b4b2d35035fd5c2a916298b0c8c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106543025"
---
# <a name="d3dxshmultiply2-function-d3dx9mathh"></a><span data-ttu-id="addcc-103">D3DXSHMultiply2, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="addcc-103">D3DXSHMultiply2 function (D3dx9math.h)</span></span>

<span data-ttu-id="addcc-104">Calcule le produit de deux fonctions représentées à l’aide de SH (f et g).</span><span class="sxs-lookup"><span data-stu-id="addcc-104">Computes the product of two functions represented using SH (f and g).</span></span>

## <a name="syntax"></a><span data-ttu-id="addcc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="addcc-105">Syntax</span></span>


```C++
FLOAT* D3DXSHMultiply2(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a><span data-ttu-id="addcc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="addcc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="addcc-107">*moue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="addcc-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="addcc-108">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="addcc-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="addcc-109">Le pointeur vers la fonction de base Ylms de sortie est stocké à l \* l + m + l.</span><span class="sxs-lookup"><span data-stu-id="addcc-109">Pointer to the output SH coefficients - basis function Ylm is stored at l\*l + m+l.</span></span>

</dd> <dt>

<span data-ttu-id="addcc-110">*PF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="addcc-110">*pF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="addcc-111">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="addcc-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="addcc-112">Entrée SH coeffs pour la fonction First.</span><span class="sxs-lookup"><span data-stu-id="addcc-112">Input SH coeffs for first function.</span></span>

</dd> <dt>

<span data-ttu-id="addcc-113">*PG* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="addcc-113">*pG* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="addcc-114">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="addcc-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="addcc-115">Second jeu d’entrées SH coeffs.</span><span class="sxs-lookup"><span data-stu-id="addcc-115">Second set of input SH coeffs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="addcc-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="addcc-116">Return value</span></span>

<span data-ttu-id="addcc-117">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="addcc-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="addcc-118">Pointeur vers les coefficients de sortie SH.</span><span class="sxs-lookup"><span data-stu-id="addcc-118">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="addcc-119">Notes</span><span class="sxs-lookup"><span data-stu-id="addcc-119">Remarks</span></span>

<span data-ttu-id="addcc-120">L’ordre est un nombre compris entre 2 et 6 inclus.</span><span class="sxs-lookup"><span data-stu-id="addcc-120">The order is a number between 2 and 6 inclusive.</span></span> <span data-ttu-id="addcc-121">En fait, cette page documente plusieurs fonctions : D3DXSHMultiply2, D3DXSHMultiply3,... D3DXSHMultiply6.</span><span class="sxs-lookup"><span data-stu-id="addcc-121">So this page actually documents several functions: D3DXSHMultiply2, D3DXSHMultiply3, ... D3DXSHMultiply6.</span></span>

<span data-ttu-id="addcc-122">Calcule le produit de deux fonctions représentées à l’aide de SH (f et g), où *moue* \[ i \] = int (y \_ i (s) \* f (s) \* g (s)), où y \_ i (s) est la fonction énième base, f (s) et g (s) sont des fonctions SH (Sum \_ i (y \_ i) \* c \_ ).</span><span class="sxs-lookup"><span data-stu-id="addcc-122">Computes the product of two functions represented using SH (f and g), where *pOut*\[i\] = int(y\_i(s) \* f(s) \* g(s)), where y\_i(s) is the ith SH basis function, f(s) and g(s) are SH functions (sum\_i(y\_i(s)\*c\_i)).</span></span> <span data-ttu-id="addcc-123">L’ordre O détermine les longueurs des tableaux, où il doit toujours y avoir un coefficient O ^ 2.</span><span class="sxs-lookup"><span data-stu-id="addcc-123">The order O determines the lengths of the arrays, where there should always be O^2 coefficients.</span></span> <span data-ttu-id="addcc-124">En général, le produit de deux fonctions SH de Order O génère une fonction SH de Order 2 \* O-1, mais les résultats sont tronqués.</span><span class="sxs-lookup"><span data-stu-id="addcc-124">In general the product of two SH functions of order O generates an SH function of order 2\*O - 1, but the results are truncated.</span></span> <span data-ttu-id="addcc-125">Cela signifie que le produit est en mode muet (f \* g = = g \* f) mais n’associe pas (f \* (g \* h) ! = (f \* g) \* h.</span><span class="sxs-lookup"><span data-stu-id="addcc-125">This means that the product commutes (f\*g == g\*f) but doesn't associate (f\*(g\*h) != (f\*g)\*h.</span></span>

## <a name="requirements"></a><span data-ttu-id="addcc-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="addcc-126">Requirements</span></span>



| <span data-ttu-id="addcc-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="addcc-127">Requirement</span></span> | <span data-ttu-id="addcc-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="addcc-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="addcc-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="addcc-129">Header</span></span><br/> | <dl> <span data-ttu-id="addcc-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="addcc-130"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="addcc-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="addcc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="addcc-132">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="addcc-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
