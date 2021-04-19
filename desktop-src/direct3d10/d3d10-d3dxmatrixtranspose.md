---
description: Retourne la permutation de matrice d’une matrice.
ms.assetid: 934b17cc-39c4-425c-839b-69e080f0efd7
title: D3DXMatrixTranspose, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTranspose
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0ecc93a560e15b8f0abe4337b866efc292c9355e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523855"
---
# <a name="d3dxmatrixtranspose-function-d3dx10mathh"></a><span data-ttu-id="a1728-103">D3DXMatrixTranspose, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="a1728-103">D3DXMatrixTranspose function (D3DX10Math.h)</span></span>

<span data-ttu-id="a1728-104">Retourne la permutation de matrice d’une matrice.</span><span class="sxs-lookup"><span data-stu-id="a1728-104">Returns the matrix transpose of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1728-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1728-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="a1728-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a1728-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1728-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a1728-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1728-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1728-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a1728-109">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="a1728-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a1728-110">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a1728-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1728-111">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a1728-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a1728-112">Pointeur vers la structure D3DXMATRIX source.</span><span class="sxs-lookup"><span data-stu-id="a1728-112">Pointer to the source D3DXMATRIX structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1728-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a1728-113">Return value</span></span>

<span data-ttu-id="a1728-114">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1728-114">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a1728-115">Pointeur vers la structure D3DXMATRIX qui est la permutation de matrice de la matrice.</span><span class="sxs-lookup"><span data-stu-id="a1728-115">Pointer to the D3DXMATRIX structure that is the matrix transpose of the matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1728-116">Notes</span><span class="sxs-lookup"><span data-stu-id="a1728-116">Remarks</span></span>

<span data-ttu-id="a1728-117">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="a1728-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="a1728-118">De cette façon, la fonction D3DXMatrixTranspose peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="a1728-118">In this way, the D3DXMatrixTranspose function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1728-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1728-119">Requirements</span></span>



| <span data-ttu-id="a1728-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1728-120">Requirement</span></span> | <span data-ttu-id="a1728-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1728-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1728-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="a1728-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a1728-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1728-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="a1728-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a1728-124">Library</span></span><br/> | <dl> <span data-ttu-id="a1728-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1728-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a1728-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1728-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1728-127">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="a1728-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
