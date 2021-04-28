---
description: 'D3DXMatrixInverse, fonction (D3DX10Math. h) : calcule l’inverse d’une matrice.'
ms.assetid: 928a201b-814d-41cc-bfab-d2f8a12addeb
title: D3DXMatrixInverse, fonction (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6b42cf0ae3f9ee1154d385600b00a2dcb10c4fd9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113197"
---
# <a name="d3dxmatrixinverse-function-d3dx10mathh"></a><span data-ttu-id="039e7-103">D3DXMatrixInverse, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="039e7-103">D3DXMatrixInverse function (D3DX10Math.h)</span></span>

<span data-ttu-id="039e7-104">Calcule l’inverse d’une matrice.</span><span class="sxs-lookup"><span data-stu-id="039e7-104">Calculates the inverse of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="039e7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="039e7-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixInverse(
  _Inout_       D3DXMATRIX *pOut,
  _Inout_       FLOAT      *pDeterminant,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="039e7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="039e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="039e7-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="039e7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="039e7-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="039e7-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="039e7-109">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="039e7-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="039e7-110">*pDeterminant* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="039e7-110">*pDeterminant* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="039e7-111">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="039e7-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="039e7-112">Pointeur vers une valeur FLOAT contenant le déterminant de la matrice.</span><span class="sxs-lookup"><span data-stu-id="039e7-112">Pointer to a FLOAT value containing the determinant of the matrix.</span></span> <span data-ttu-id="039e7-113">Si le déterminant n’est pas nécessaire, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="039e7-113">If the determinant is not needed, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="039e7-114">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="039e7-114">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="039e7-115">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="039e7-115">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="039e7-116">Pointeur vers la structure D3DXMATRIX source.</span><span class="sxs-lookup"><span data-stu-id="039e7-116">Pointer to the source D3DXMATRIX structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="039e7-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="039e7-117">Return value</span></span>

<span data-ttu-id="039e7-118">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="039e7-118">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="039e7-119">Pointeur vers une structure D3DXMATRIX qui est l’inverse de la matrice.</span><span class="sxs-lookup"><span data-stu-id="039e7-119">Pointer to a D3DXMATRIX structure that is the inverse of the matrix.</span></span> <span data-ttu-id="039e7-120">Si la matrice d’inversion échoue, la **valeur null** est retournée.</span><span class="sxs-lookup"><span data-stu-id="039e7-120">If matrix inversion fails, **NULL** is returned.</span></span>

<span data-ttu-id="039e7-121">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="039e7-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="039e7-122">De cette façon, la fonction D3DXMatrixInverse peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="039e7-122">In this way, the D3DXMatrixInverse function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="039e7-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="039e7-123">Requirements</span></span>



| <span data-ttu-id="039e7-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="039e7-124">Requirement</span></span> | <span data-ttu-id="039e7-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="039e7-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="039e7-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="039e7-126">Header</span></span><br/>  | <dl> <span data-ttu-id="039e7-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="039e7-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="039e7-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="039e7-128">Library</span></span><br/> | <dl> <span data-ttu-id="039e7-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="039e7-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="039e7-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="039e7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="039e7-131">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="039e7-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
