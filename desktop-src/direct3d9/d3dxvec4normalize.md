---
description: Retourne la version normalisée d’un vecteur 4D.
ms.assetid: e12d5dc7-b26f-41dd-b89d-1df9ba23077a
title: D3DXVec4Normalize, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Normalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 38d97f337711375d1d414eb78fb317672bc7c5cb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043197"
---
# <a name="d3dxvec4normalize-function-d3dx9mathh"></a><span data-ttu-id="28bb2-103">D3DXVec4Normalize, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="28bb2-103">D3DXVec4Normalize function (D3dx9math.h)</span></span>

<span data-ttu-id="28bb2-104">Retourne la version normalisée d’un vecteur 4D.</span><span class="sxs-lookup"><span data-stu-id="28bb2-104">Returns the normalized version of a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="28bb2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28bb2-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Normalize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="28bb2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28bb2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28bb2-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="28bb2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="28bb2-108">Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="28bb2-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="28bb2-109">Pointeur vers la structure [**D3DXVECTOR4**](d3dxvector4.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="28bb2-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="28bb2-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="28bb2-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28bb2-111">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="28bb2-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="28bb2-112">Pointeur vers la structure [**D3DXVECTOR4**](d3dxvector4.md) source.</span><span class="sxs-lookup"><span data-stu-id="28bb2-112">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28bb2-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="28bb2-113">Return value</span></span>

<span data-ttu-id="28bb2-114">Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="28bb2-114">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="28bb2-115">Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) qui est la version normalisée du vecteur.</span><span class="sxs-lookup"><span data-stu-id="28bb2-115">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="28bb2-116">Notes</span><span class="sxs-lookup"><span data-stu-id="28bb2-116">Remarks</span></span>

<span data-ttu-id="28bb2-117">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="28bb2-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="28bb2-118">De cette façon, la fonction **D3DXVec4Normalize** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="28bb2-118">In this way, the **D3DXVec4Normalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="28bb2-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28bb2-119">Requirements</span></span>



| <span data-ttu-id="28bb2-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28bb2-120">Requirement</span></span> | <span data-ttu-id="28bb2-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="28bb2-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28bb2-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="28bb2-122">Header</span></span><br/>  | <dl> <span data-ttu-id="28bb2-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="28bb2-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="28bb2-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="28bb2-124">Library</span></span><br/> | <dl> <span data-ttu-id="28bb2-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28bb2-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="28bb2-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28bb2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28bb2-127">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="28bb2-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




