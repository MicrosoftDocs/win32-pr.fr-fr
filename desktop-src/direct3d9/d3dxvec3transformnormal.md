---
description: D3DXVec3TransformNormal, fonction (D3dx9math. h)-transforme le vecteur 3D normal par la matrice donnée.
ms.assetid: aa9531e1-b77a-4aad-8d59-2677908cb978
title: D3DXVec3TransformNormal, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 50fb09a4619be9c3dbcff98bc939d6f99ad33bd4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115617"
---
# <a name="d3dxvec3transformnormal-function-d3dx9mathh"></a><span data-ttu-id="b9352-103">D3DXVec3TransformNormal, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="b9352-103">D3DXVec3TransformNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="b9352-104">Transforme le vecteur 3D normal par la matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="b9352-104">Transforms the 3D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9352-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9352-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormal(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="b9352-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b9352-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9352-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b9352-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9352-108">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="b9352-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b9352-109">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="b9352-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b9352-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b9352-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9352-111">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b9352-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b9352-112">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) source.</span><span class="sxs-lookup"><span data-stu-id="b9352-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b9352-113">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b9352-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9352-114">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="b9352-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b9352-115">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="b9352-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9352-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b9352-116">Return value</span></span>

<span data-ttu-id="b9352-117">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="b9352-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b9352-118">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) qui est le vecteur transformé.</span><span class="sxs-lookup"><span data-stu-id="b9352-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9352-119">Notes </span><span class="sxs-lookup"><span data-stu-id="b9352-119">Remarks</span></span>

<span data-ttu-id="b9352-120">Cette fonction transforme le vecteur (*PV*->x, *PV*->y, *PV*->z, 0) par la matrice vers laquelle pointe *PM*.</span><span class="sxs-lookup"><span data-stu-id="b9352-120">This function transforms the vector (*pV*->x, *pV*->y, *pV*->z, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="b9352-121">Si vous souhaitez transformer un normal, la matrice que vous transmettez à cette fonction doit être la transposer de l’inverse de la matrice que vous utiliseriez pour transformer un point.</span><span class="sxs-lookup"><span data-stu-id="b9352-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="b9352-122">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="b9352-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="b9352-123">De cette façon, la fonction **D3DXVec3TransformNormal** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="b9352-123">In this way, the **D3DXVec3TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9352-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9352-124">Requirements</span></span>



| <span data-ttu-id="b9352-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b9352-125">Requirement</span></span> | <span data-ttu-id="b9352-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9352-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9352-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="b9352-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b9352-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9352-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b9352-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b9352-129">Library</span></span><br/> | <dl> <span data-ttu-id="b9352-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9352-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b9352-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9352-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9352-132">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="b9352-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




