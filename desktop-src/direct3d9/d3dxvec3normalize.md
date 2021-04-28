---
description: 'D3DXVec3Normalize, fonction (D3dx9math. h) : retourne la version normalisée d’un vecteur 3D.'
ms.assetid: 7bb8302e-8af2-4328-9b46-bc9f5a009f56
title: D3DXVec3Normalize, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Normalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f39890a92bbff9d27a1150e76092d865dc36c089
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097827"
---
# <a name="d3dxvec3normalize-function-d3dx9mathh"></a><span data-ttu-id="c78c7-103">D3DXVec3Normalize, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c78c7-103">D3DXVec3Normalize function (D3dx9math.h)</span></span>

<span data-ttu-id="c78c7-104">Retourne la version normalisée d’un vecteur 3D.</span><span class="sxs-lookup"><span data-stu-id="c78c7-104">Returns the normalized version of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="c78c7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c78c7-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Normalize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="c78c7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c78c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c78c7-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c78c7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c78c7-108">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c78c7-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c78c7-109">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="c78c7-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c78c7-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c78c7-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c78c7-111">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c78c7-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c78c7-112">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) source.</span><span class="sxs-lookup"><span data-stu-id="c78c7-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c78c7-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c78c7-113">Return value</span></span>

<span data-ttu-id="c78c7-114">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c78c7-114">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c78c7-115">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) qui est la version normalisée du vecteur spécifié.</span><span class="sxs-lookup"><span data-stu-id="c78c7-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the normalized version of the specified vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="c78c7-116">Notes </span><span class="sxs-lookup"><span data-stu-id="c78c7-116">Remarks</span></span>

<span data-ttu-id="c78c7-117">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="c78c7-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c78c7-118">De cette façon, la fonction **D3DXVec3Normalize** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="c78c7-118">In this way, the **D3DXVec3Normalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c78c7-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c78c7-119">Requirements</span></span>



| <span data-ttu-id="c78c7-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c78c7-120">Requirement</span></span> | <span data-ttu-id="c78c7-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c78c7-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c78c7-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c78c7-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c78c7-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c78c7-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c78c7-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c78c7-124">Library</span></span><br/> | <dl> <span data-ttu-id="c78c7-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c78c7-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c78c7-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c78c7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c78c7-127">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="c78c7-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




