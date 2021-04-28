---
description: 'D3DXVec4Normalize, fonction (D3DX10Math. h) : retourne la version normalisée d’un vecteur 4D.'
ms.assetid: ed3c48cf-4985-4ef3-b733-f8532e3ff6b5
title: D3DXVec4Normalize, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Normalize
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 1577ff3109c2cc3ca547f68f7841ecebb2f03569
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102907"
---
# <a name="d3dxvec4normalize-function-d3dx10mathh"></a><span data-ttu-id="b6c93-103">D3DXVec4Normalize, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="b6c93-103">D3DXVec4Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="b6c93-104">Retourne la version normalisée d’un vecteur 4D.</span><span class="sxs-lookup"><span data-stu-id="b6c93-104">Returns the normalized version of a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6c93-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6c93-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Normalize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="b6c93-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6c93-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6c93-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b6c93-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6c93-108">Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="b6c93-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="b6c93-109">Pointeur vers le [**D3DXVECTOR4**](d3d10-d3dxvector4.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="b6c93-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b6c93-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b6c93-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6c93-111">Type : **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="b6c93-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="b6c93-112">Pointeur vers la structure D3DXVECTOR4 source.</span><span class="sxs-lookup"><span data-stu-id="b6c93-112">Pointer to the source D3DXVECTOR4 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6c93-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b6c93-113">Return value</span></span>

<span data-ttu-id="b6c93-114">Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="b6c93-114">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="b6c93-115">Pointeur vers une structure D3DXVECTOR4 qui est la version normalisée du vecteur.</span><span class="sxs-lookup"><span data-stu-id="b6c93-115">Pointer to a D3DXVECTOR4 structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6c93-116">Notes </span><span class="sxs-lookup"><span data-stu-id="b6c93-116">Remarks</span></span>

<span data-ttu-id="b6c93-117">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="b6c93-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b6c93-118">De cette façon, la fonction D3DXVec4Normalize peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="b6c93-118">In this way, the D3DXVec4Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6c93-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6c93-119">Requirements</span></span>



| <span data-ttu-id="b6c93-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6c93-120">Requirement</span></span> | <span data-ttu-id="b6c93-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6c93-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c93-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6c93-122">Header</span></span><br/> | <dl> <span data-ttu-id="b6c93-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6c93-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6c93-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6c93-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6c93-125">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="b6c93-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
