---
description: 'D3DXVec2Normalize, fonction (D3dx9math. h) : retourne la version normalisée d’un vecteur 2D.'
ms.assetid: 2796a5d1-cb1c-4093-87f2-a2ad43279d91
title: D3DXVec2Normalize, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Normalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3322981be5c266bee20a61e85302cb22538a7b0d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097967"
---
# <a name="d3dxvec2normalize-function-d3dx9mathh"></a><span data-ttu-id="5f85e-103">D3DXVec2Normalize, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="5f85e-103">D3DXVec2Normalize function (D3dx9math.h)</span></span>

<span data-ttu-id="5f85e-104">Retourne la version normalisée d’un vecteur 2D.</span><span class="sxs-lookup"><span data-stu-id="5f85e-104">Returns the normalized version of a 2D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f85e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f85e-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Normalize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="5f85e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f85e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f85e-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5f85e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f85e-108">Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="5f85e-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="5f85e-109">Pointeur vers la structure [**D3DXVECTOR2**](d3dxvector2.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="5f85e-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5f85e-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f85e-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f85e-111">Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="5f85e-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="5f85e-112">Pointeur vers la structure [**D3DXVECTOR2**](d3dxvector2.md) source.</span><span class="sxs-lookup"><span data-stu-id="5f85e-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f85e-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5f85e-113">Return value</span></span>

<span data-ttu-id="5f85e-114">Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="5f85e-114">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="5f85e-115">Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) qui est la version normalisée du vecteur.</span><span class="sxs-lookup"><span data-stu-id="5f85e-115">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f85e-116">Notes </span><span class="sxs-lookup"><span data-stu-id="5f85e-116">Remarks</span></span>

<span data-ttu-id="5f85e-117">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="5f85e-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="5f85e-118">De cette façon, la fonction **D3DXVec2Normalize** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="5f85e-118">In this way, the **D3DXVec2Normalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f85e-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f85e-119">Requirements</span></span>



| <span data-ttu-id="5f85e-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f85e-120">Requirement</span></span> | <span data-ttu-id="5f85e-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f85e-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f85e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="5f85e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="5f85e-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f85e-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5f85e-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5f85e-124">Library</span></span><br/> | <dl> <span data-ttu-id="5f85e-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f85e-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5f85e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f85e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f85e-127">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="5f85e-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




