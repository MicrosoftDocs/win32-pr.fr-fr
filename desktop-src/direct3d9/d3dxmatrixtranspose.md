---
description: Retourne la permutation de matrice d’une matrice.
ms.assetid: 0ba9682f-3dd6-48b2-82b1-6e34e8ce5452
title: D3DXMatrixTranspose, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 700fc023cd15227c2cf26cd5bdcab51dc0ae3297
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531516"
---
# <a name="d3dxmatrixtranspose-function-d3dx9mathh"></a><span data-ttu-id="b3869-103">D3DXMatrixTranspose, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="b3869-103">D3DXMatrixTranspose function (D3dx9math.h)</span></span>

<span data-ttu-id="b3869-104">Retourne la permutation de matrice d’une matrice.</span><span class="sxs-lookup"><span data-stu-id="b3869-104">Returns the matrix transpose of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3869-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3869-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="b3869-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3869-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3869-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b3869-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3869-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b3869-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b3869-109">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="b3869-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b3869-110">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3869-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3869-111">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="b3869-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b3869-112">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="b3869-112">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3869-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b3869-113">Return value</span></span>

<span data-ttu-id="b3869-114">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b3869-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b3869-115">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est la permutation de matrice de la matrice.</span><span class="sxs-lookup"><span data-stu-id="b3869-115">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the matrix transpose of the matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3869-116">Notes</span><span class="sxs-lookup"><span data-stu-id="b3869-116">Remarks</span></span>

<span data-ttu-id="b3869-117">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="b3869-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="b3869-118">De cette façon, la fonction **D3DXMatrixTranspose** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="b3869-118">In this way, the **D3DXMatrixTranspose** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3869-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3869-119">Requirements</span></span>



| <span data-ttu-id="b3869-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3869-120">Requirement</span></span> | <span data-ttu-id="b3869-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3869-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3869-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="b3869-122">Header</span></span><br/>  | <dl> <span data-ttu-id="b3869-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3869-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b3869-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b3869-124">Library</span></span><br/> | <dl> <span data-ttu-id="b3869-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3869-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b3869-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3869-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3869-127">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="b3869-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




