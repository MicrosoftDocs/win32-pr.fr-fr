---
description: Retourne un vecteur 2D composé des plus grands composants de deux vecteurs 2D.
ms.assetid: 5eb5141b-d611-4c6b-a3e3-c7ad8f223657
title: D3DXVec2Maximize, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Maximize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ffd5fbc98e653a6bbaffa7d3cec16b13695365b2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394112"
---
# <a name="d3dxvec2maximize-function"></a><span data-ttu-id="2db20-103">D3DXVec2Maximize fonction)</span><span class="sxs-lookup"><span data-stu-id="2db20-103">D3DXVec2Maximize function</span></span>

<span data-ttu-id="2db20-104">Retourne un vecteur 2D composé des plus grands composants de deux vecteurs 2D.</span><span class="sxs-lookup"><span data-stu-id="2db20-104">Returns a 2D vector that is made up of the largest components of two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="2db20-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2db20-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Maximize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="2db20-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2db20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2db20-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2db20-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2db20-108">Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="2db20-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="2db20-109">Pointeur vers la structure [**D3DXVECTOR2**](d3dxvector2.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="2db20-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2db20-110">*pV1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2db20-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2db20-111">Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="2db20-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="2db20-112">Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) source.</span><span class="sxs-lookup"><span data-stu-id="2db20-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2db20-113">*pV2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2db20-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2db20-114">Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="2db20-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="2db20-115">Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) source.</span><span class="sxs-lookup"><span data-stu-id="2db20-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2db20-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2db20-116">Return value</span></span>

<span data-ttu-id="2db20-117">Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="2db20-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="2db20-118">Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) composée des plus grands composants des deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="2db20-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is made up of the largest components of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="2db20-119">Notes</span><span class="sxs-lookup"><span data-stu-id="2db20-119">Remarks</span></span>

<span data-ttu-id="2db20-120">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="2db20-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="2db20-121">De cette façon, la fonction **D3DXVec2Maximize** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="2db20-121">In this way, the **D3DXVec2Maximize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2db20-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2db20-122">Requirements</span></span>



| <span data-ttu-id="2db20-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2db20-123">Requirement</span></span> | <span data-ttu-id="2db20-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="2db20-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2db20-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="2db20-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2db20-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2db20-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2db20-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2db20-127">Library</span></span><br/> | <dl> <span data-ttu-id="2db20-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2db20-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2db20-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2db20-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2db20-130">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="2db20-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2db20-131">**D3DXVec2Minimize**</span><span class="sxs-lookup"><span data-stu-id="2db20-131">**D3DXVec2Minimize**</span></span>](d3dxvec2minimize.md)
</dt> </dl>

 

 




