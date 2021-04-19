---
description: Détermine le produit de deux matrices.
ms.assetid: 160c801a-6589-4a0d-8e90-7e7a99fbd5f7
title: D3DXMatrixMultiply, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiply
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ea578f54d3f690f01d9280e840cb9ee039d0cdf0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522563"
---
# <a name="d3dxmatrixmultiply-function-d3dx9mathh"></a><span data-ttu-id="068b9-103">D3DXMatrixMultiply, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="068b9-103">D3DXMatrixMultiply function (D3dx9math.h)</span></span>

<span data-ttu-id="068b9-104">Détermine le produit de deux matrices.</span><span class="sxs-lookup"><span data-stu-id="068b9-104">Determines the product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="068b9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="068b9-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiply(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="068b9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="068b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="068b9-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="068b9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="068b9-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="068b9-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="068b9-109">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="068b9-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="068b9-110">*pM1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="068b9-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="068b9-111">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="068b9-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="068b9-112">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="068b9-112">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="068b9-113">*pM2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="068b9-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="068b9-114">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="068b9-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="068b9-115">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="068b9-115">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="068b9-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="068b9-116">Return value</span></span>

<span data-ttu-id="068b9-117">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="068b9-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="068b9-118">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le produit de deux matrices.</span><span class="sxs-lookup"><span data-stu-id="068b9-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="068b9-119">Notes</span><span class="sxs-lookup"><span data-stu-id="068b9-119">Remarks</span></span>

<span data-ttu-id="068b9-120">Le résultat représente la transformation M1 suivie de la transformation m2 (out = M1 \* m2).</span><span class="sxs-lookup"><span data-stu-id="068b9-120">The result represents the transformation M1 followed by the transformation M2 (Out = M1 \* M2).</span></span>

<span data-ttu-id="068b9-121">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="068b9-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="068b9-122">De cette façon, la fonction **D3DXMatrixMultiply** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="068b9-122">In this way, the **D3DXMatrixMultiply** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="068b9-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="068b9-123">Requirements</span></span>



| <span data-ttu-id="068b9-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="068b9-124">Requirement</span></span> | <span data-ttu-id="068b9-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="068b9-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="068b9-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="068b9-126">Header</span></span><br/>  | <dl> <span data-ttu-id="068b9-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="068b9-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="068b9-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="068b9-128">Library</span></span><br/> | <dl> <span data-ttu-id="068b9-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="068b9-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="068b9-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="068b9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="068b9-131">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="068b9-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="068b9-132">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="068b9-132">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




