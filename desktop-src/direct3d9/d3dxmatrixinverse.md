---
description: 'D3DXMatrixInverse, fonction (D3dx9math. h) : calcule l’inverse d’une matrice.'
ms.assetid: b8cad5c5-caa5-4426-b045-1770f8806b6b
title: D3DXMatrixInverse, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixInverse
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0109481beaea282a785564c081e498fe4c7571b6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098147"
---
# <a name="d3dxmatrixinverse-function-d3dx9mathh"></a><span data-ttu-id="72dff-103">D3DXMatrixInverse, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="72dff-103">D3DXMatrixInverse function (D3dx9math.h)</span></span>

<span data-ttu-id="72dff-104">Calcule l’inverse d’une matrice.</span><span class="sxs-lookup"><span data-stu-id="72dff-104">Calculates the inverse of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="72dff-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72dff-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixInverse(
  _Inout_       D3DXMATRIX *pOut,
  _Inout_       FLOAT      *pDeterminant,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="72dff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72dff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72dff-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="72dff-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="72dff-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="72dff-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="72dff-109">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="72dff-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="72dff-110">*pDeterminant* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="72dff-110">*pDeterminant* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="72dff-111">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="72dff-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="72dff-112">Pointeur vers une valeur FLOAT contenant le déterminant de la matrice.</span><span class="sxs-lookup"><span data-stu-id="72dff-112">Pointer to a FLOAT value containing the determinant of the matrix.</span></span> <span data-ttu-id="72dff-113">Si le déterminant n’est pas nécessaire, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="72dff-113">If the determinant is not needed, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="72dff-114">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="72dff-114">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72dff-115">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="72dff-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="72dff-116">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="72dff-116">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72dff-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="72dff-117">Return value</span></span>

<span data-ttu-id="72dff-118">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="72dff-118">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="72dff-119">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) qui est l’inverse de la matrice.</span><span class="sxs-lookup"><span data-stu-id="72dff-119">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the inverse of the matrix.</span></span> <span data-ttu-id="72dff-120">Si la matrice d’inversion échoue, la **valeur null** est retournée.</span><span class="sxs-lookup"><span data-stu-id="72dff-120">If matrix inversion fails, **NULL** is returned.</span></span>

<span data-ttu-id="72dff-121">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="72dff-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="72dff-122">De cette façon, la fonction **D3DXMatrixInverse** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="72dff-122">In this way, the **D3DXMatrixInverse** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="72dff-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72dff-123">Requirements</span></span>



| <span data-ttu-id="72dff-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72dff-124">Requirement</span></span> | <span data-ttu-id="72dff-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="72dff-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="72dff-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="72dff-126">Header</span></span><br/>  | <dl> <span data-ttu-id="72dff-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="72dff-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="72dff-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="72dff-128">Library</span></span><br/> | <dl> <span data-ttu-id="72dff-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72dff-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="72dff-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72dff-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72dff-131">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="72dff-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
