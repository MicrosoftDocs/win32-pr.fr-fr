---
description: Crée une matrice d’identité.
ms.assetid: 0dd6d4fb-284c-4d01-9a85-63aa08e71723
title: D3DXMatrixIdentity, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 10dffa12a379754006ca65d1239be96632a68b93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953798"
---
# <a name="d3dxmatrixidentity-function"></a><span data-ttu-id="2359f-103">D3DXMatrixIdentity fonction)</span><span class="sxs-lookup"><span data-stu-id="2359f-103">D3DXMatrixIdentity function</span></span>

<span data-ttu-id="2359f-104">Crée une matrice d’identité.</span><span class="sxs-lookup"><span data-stu-id="2359f-104">Creates an identity matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="2359f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2359f-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixIdentity(
  _Inout_ D3DXMATRIX *pOut
);
```



## <a name="parameters"></a><span data-ttu-id="2359f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2359f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2359f-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2359f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2359f-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2359f-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2359f-109">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="2359f-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2359f-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2359f-110">Return value</span></span>

<span data-ttu-id="2359f-111">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2359f-111">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2359f-112">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) qui est la matrice d’identité.</span><span class="sxs-lookup"><span data-stu-id="2359f-112">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the identity matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="2359f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="2359f-113">Remarks</span></span>

<span data-ttu-id="2359f-114">La matrice d’identité est une matrice dans laquelle tous les coefficients sont 0, à l’exception des \[ coefficients 1, 1, 2 \] \[ \] \[ 3, 3 \] \[ 4, 4 \] , qui sont définis sur 1.</span><span class="sxs-lookup"><span data-stu-id="2359f-114">The identity matrix is a matrix in which all coefficients are 0 except the \[1,1\]\[2,2\]\[3,3\]\[4,4\] coefficients, which are set to 1.</span></span> <span data-ttu-id="2359f-115">La matrice d’identité est spéciale dans le cas où elle est appliquée aux sommets, mais elle n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="2359f-115">The identity matrix is special in that when it is applied to vertices, they are unchanged.</span></span> <span data-ttu-id="2359f-116">La matrice d’identité est utilisée comme point de départ pour les matrices qui modifient les valeurs de vertex pour créer des rotations, des translations et d’autres transformations qui peuvent être représentées par une matrice 4 X4.</span><span class="sxs-lookup"><span data-stu-id="2359f-116">The identity matrix is used as the starting point for matrices that will modify vertex values to create rotations, translations, and any other transformations that can be represented by a 4 x4 matrix.</span></span>

<span data-ttu-id="2359f-117">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="2359f-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="2359f-118">De cette façon, la fonction **D3DXMatrixIdentity** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="2359f-118">In this way, the **D3DXMatrixIdentity** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2359f-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2359f-119">Requirements</span></span>



| <span data-ttu-id="2359f-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2359f-120">Requirement</span></span> | <span data-ttu-id="2359f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="2359f-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2359f-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="2359f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="2359f-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2359f-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2359f-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2359f-124">Library</span></span><br/> | <dl> <span data-ttu-id="2359f-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2359f-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2359f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2359f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2359f-127">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="2359f-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2359f-128">**D3DXMatrixIsIdentity**</span><span class="sxs-lookup"><span data-stu-id="2359f-128">**D3DXMatrixIsIdentity**</span></span>](d3dxmatrixisidentity.md)
</dt> </dl>

 

 




