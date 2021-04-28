---
description: 'D3DXVec4Normalize, fonction (D3dx9math. h) : retourne la version normalisée d’un vecteur 4D.'
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
ms.openlocfilehash: 78984c393d7caf259b4c310a31e01ed8fcbd4d47
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097657"
---
# <a name="d3dxvec4normalize-function-d3dx9mathh"></a><span data-ttu-id="897b0-103">D3DXVec4Normalize, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="897b0-103">D3DXVec4Normalize function (D3dx9math.h)</span></span>

<span data-ttu-id="897b0-104">Retourne la version normalisée d’un vecteur 4D.</span><span class="sxs-lookup"><span data-stu-id="897b0-104">Returns the normalized version of a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="897b0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="897b0-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Normalize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="897b0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="897b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="897b0-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="897b0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="897b0-108">Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="897b0-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="897b0-109">Pointeur vers la structure [**D3DXVECTOR4**](d3dxvector4.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="897b0-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="897b0-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="897b0-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="897b0-111">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="897b0-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="897b0-112">Pointeur vers la structure [**D3DXVECTOR4**](d3dxvector4.md) source.</span><span class="sxs-lookup"><span data-stu-id="897b0-112">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="897b0-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="897b0-113">Return value</span></span>

<span data-ttu-id="897b0-114">Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="897b0-114">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="897b0-115">Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) qui est la version normalisée du vecteur.</span><span class="sxs-lookup"><span data-stu-id="897b0-115">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="897b0-116">Notes </span><span class="sxs-lookup"><span data-stu-id="897b0-116">Remarks</span></span>

<span data-ttu-id="897b0-117">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="897b0-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="897b0-118">De cette façon, la fonction **D3DXVec4Normalize** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="897b0-118">In this way, the **D3DXVec4Normalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="897b0-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="897b0-119">Requirements</span></span>



| <span data-ttu-id="897b0-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="897b0-120">Requirement</span></span> | <span data-ttu-id="897b0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="897b0-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="897b0-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="897b0-122">Header</span></span><br/>  | <dl> <span data-ttu-id="897b0-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="897b0-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="897b0-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="897b0-124">Library</span></span><br/> | <dl> <span data-ttu-id="897b0-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="897b0-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="897b0-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="897b0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="897b0-127">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="897b0-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




