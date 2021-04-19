---
description: Retourne un vecteur 2D composé des composants les plus petits de deux vecteurs 2D.
ms.assetid: 6944523e-33dd-456e-9cc2-17760d76c548
title: D3DXVec2Minimize, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Minimize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1914ae9317d686e369f1cb2c7eb36ab54a29845f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523179"
---
# <a name="d3dxvec2minimize-function"></a><span data-ttu-id="2c749-103">D3DXVec2Minimize fonction)</span><span class="sxs-lookup"><span data-stu-id="2c749-103">D3DXVec2Minimize function</span></span>

<span data-ttu-id="2c749-104">Retourne un vecteur 2D composé des composants les plus petits de deux vecteurs 2D.</span><span class="sxs-lookup"><span data-stu-id="2c749-104">Returns a 2D vector that is made up of the smallest components of two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c749-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c749-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Minimize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="2c749-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c749-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c749-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2c749-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c749-108">Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="2c749-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="2c749-109">Pointeur vers la structure [**D3DXVECTOR2**](d3dxvector2.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="2c749-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2c749-110">*pV1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2c749-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c749-111">Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="2c749-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="2c749-112">Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) source.</span><span class="sxs-lookup"><span data-stu-id="2c749-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2c749-113">*pV2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2c749-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c749-114">Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="2c749-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="2c749-115">Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) source.</span><span class="sxs-lookup"><span data-stu-id="2c749-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c749-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2c749-116">Return value</span></span>

<span data-ttu-id="2c749-117">Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="2c749-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="2c749-118">Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) composée des plus petits composants des deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="2c749-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is made up of the smallest components of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c749-119">Notes</span><span class="sxs-lookup"><span data-stu-id="2c749-119">Remarks</span></span>

<span data-ttu-id="2c749-120">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="2c749-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="2c749-121">De cette façon, la fonction **D3DXVec2Minimize** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="2c749-121">In this way, the **D3DXVec2Minimize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c749-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c749-122">Requirements</span></span>



| <span data-ttu-id="2c749-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c749-123">Requirement</span></span> | <span data-ttu-id="2c749-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c749-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c749-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c749-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2c749-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c749-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2c749-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2c749-127">Library</span></span><br/> | <dl> <span data-ttu-id="2c749-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c749-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2c749-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c749-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c749-130">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="2c749-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2c749-131">**D3DXVec2Maximize**</span><span class="sxs-lookup"><span data-stu-id="2c749-131">**D3DXVec2Maximize**</span></span>](d3dxvec2maximize.md)
</dt> </dl>

 

 




