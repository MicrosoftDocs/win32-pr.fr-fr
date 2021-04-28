---
description: 'D3DXMatrixTranspose, fonction (D3DX10Math. h) : retourne la permutation de matrice d’une matrice.'
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
ms.openlocfilehash: e20fd8a29ba3f9adec7134a011f8f470c60f7011
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108857"
---
# <a name="d3dxmatrixtranspose-function-d3dx10mathh"></a><span data-ttu-id="55578-103">D3DXMatrixTranspose, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="55578-103">D3DXMatrixTranspose function (D3DX10Math.h)</span></span>

<span data-ttu-id="55578-104">Retourne la permutation de matrice d’une matrice.</span><span class="sxs-lookup"><span data-stu-id="55578-104">Returns the matrix transpose of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="55578-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55578-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="55578-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55578-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55578-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="55578-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="55578-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="55578-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="55578-109">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="55578-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="55578-110">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="55578-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55578-111">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="55578-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="55578-112">Pointeur vers la structure D3DXMATRIX source.</span><span class="sxs-lookup"><span data-stu-id="55578-112">Pointer to the source D3DXMATRIX structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55578-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="55578-113">Return value</span></span>

<span data-ttu-id="55578-114">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="55578-114">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="55578-115">Pointeur vers la structure D3DXMATRIX qui est la permutation de matrice de la matrice.</span><span class="sxs-lookup"><span data-stu-id="55578-115">Pointer to the D3DXMATRIX structure that is the matrix transpose of the matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="55578-116">Notes </span><span class="sxs-lookup"><span data-stu-id="55578-116">Remarks</span></span>

<span data-ttu-id="55578-117">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="55578-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="55578-118">De cette façon, la fonction D3DXMatrixTranspose peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="55578-118">In this way, the D3DXMatrixTranspose function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="55578-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55578-119">Requirements</span></span>



| <span data-ttu-id="55578-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55578-120">Requirement</span></span> | <span data-ttu-id="55578-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="55578-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55578-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="55578-122">Header</span></span><br/>  | <dl> <span data-ttu-id="55578-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="55578-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="55578-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="55578-124">Library</span></span><br/> | <dl> <span data-ttu-id="55578-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55578-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="55578-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55578-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55578-127">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="55578-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
